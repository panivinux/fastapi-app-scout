build-and-analyze
succeeded 3 hours ago in 51s
Search logs
4s
Current runner version: '2.328.0'
Runner Image Provisioner
Operating System
Runner Image
GITHUB_TOKEN Permissions
Secret source: Actions
Prepare workflow directory
Prepare all required actions
Getting action download info
Download action repository 'actions/checkout@v4' (SHA:08eba0b27e820071cde6df949e0beb9ba4906955)
Download action repository 'docker/login-action@v3' (SHA:184bdaa0721073962dff0199f1fb9940f07167d1)
Download action repository 'docker/setup-buildx-action@v3' (SHA:e468171a9de216ec08956ac3ada2f0791b6bd435)
Download action repository 'docker/build-push-action@v6' (SHA:263435318d21b8e681c14492fe198d362a7d2c83)
Download action repository 'actions/upload-artifact@v4' (SHA:ea165f8d65b6e75b540449e92b4886f43607fa02)
Complete job name: build-and-analyze
0s
Run actions/checkout@v4
Syncing repository: ***/fastapi-app-scout
Getting Git version info
Temporarily overriding HOME='/home/runner/work/_temp/fdf25d8b-d5ce-4d11-87e3-a1e8aa687030' before making global git config changes
Adding repository directory to the temporary git global config as a safe directory
/usr/bin/git config --global --add safe.directory /home/runner/work/fastapi-app-scout/fastapi-app-scout
Deleting the contents of '/home/runner/work/fastapi-app-scout/fastapi-app-scout'
Initializing the repository
Disabling automatic garbage collection
Setting up auth
Fetching the repository
Determining the checkout info
/usr/bin/git sparse-checkout disable
/usr/bin/git config --local --unset-all extensions.worktreeConfig
Checking out the ref
/usr/bin/git log -1 --format=%H
df21dbd5bff9cad501c6fa452cf010d8ac0a9a08
1s
Run docker/login-action@v3
Logging into Docker Hub...
Login Succeeded!
7s
Run docker/setup-buildx-action@v3
Docker info
Buildx version
Inspecting default docker context
Creating a new builder instance
Booting builder
Inspect builder
BuildKit version
15s
Run docker/build-push-action@v6
GitHub Actions runtime token ACs
Docker info
Proxy configuration
Buildx version
Builder info
/usr/bin/docker buildx build --file ./Dockerfile-single --iidfile /home/runner/work/_temp/docker-actions-toolkit-h3PX6H/build-iidfile-de5596d535.txt --tag ***/fastapi-app-scout:sha-df21dbd5bff9cad501c6fa452cf010d8ac0a9a08 --load --metadata-file /home/runner/work/_temp/docker-actions-toolkit-h3PX6H/build-metadata-4323ba1caa.json .
#0 building with "builder-cbf9b152-9ce9-450f-bef8-cfa00026a0bd" instance using docker-container driver

#1 [internal] load build definition from Dockerfile-single
#1 transferring dockerfile: 589B done
#1 DONE 0.0s

#2 [internal] load metadata for docker.io/library/python:3.11-slim
#2 ...

#3 [auth] library/python:pull token for registry-1.docker.io
#3 DONE 0.0s

#2 [internal] load metadata for docker.io/library/python:3.11-slim
#2 DONE 0.9s

#4 [internal] load .dockerignore
#4 transferring context: 2B done
#4 DONE 0.0s

#5 [internal] load build context
#5 transferring context: 42.04kB 0.0s done
#5 DONE 0.0s

#6 [1/7] FROM docker.io/library/python:3.11-slim@sha256:a0939570b38cddeb861b8e75d20b1c8218b21562b18f301171904b544e8cf228
#6 resolve docker.io/library/python:3.11-slim@sha256:a0939570b38cddeb861b8e75d20b1c8218b21562b18f301171904b544e8cf228 done
#6 sha256:a4aefcec16c5bdc01af2ad1c5341b420d4179f3b825c0dc866367fb43f0d50ac 0B / 250B 0.2s
#6 sha256:a4aefcec16c5bdc01af2ad1c5341b420d4179f3b825c0dc866367fb43f0d50ac 250B / 250B 0.2s done
#6 sha256:11b89692b2085631f6e2407edd8545b033c8e6945837103875d6db484e945b6f 0B / 1.29MB 0.3s
#6 sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3 0B / 29.77MB 0.2s
#6 sha256:764e05fe66b6768e40fa2a21d5108eceb8f3f8f2c32463d72c109c54dde0d5c1 0B / 14.64MB 0.2s
#6 sha256:11b89692b2085631f6e2407edd8545b033c8e6945837103875d6db484e945b6f 1.29MB / 1.29MB 0.3s done
#6 sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3 2.10MB / 29.77MB 0.5s
#6 sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3 6.29MB / 29.77MB 0.6s
#6 sha256:764e05fe66b6768e40fa2a21d5108eceb8f3f8f2c32463d72c109c54dde0d5c1 3.15MB / 14.64MB 0.5s
#6 sha256:764e05fe66b6768e40fa2a21d5108eceb8f3f8f2c32463d72c109c54dde0d5c1 14.64MB / 14.64MB 0.7s done
#6 sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3 12.58MB / 29.77MB 0.9s
#6 sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3 15.73MB / 29.77MB 1.1s
#6 sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3 18.87MB / 29.77MB 1.2s
#6 sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3 24.12MB / 29.77MB 1.4s
#6 sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3 26.21MB / 29.77MB 1.5s
#6 sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3 29.77MB / 29.77MB 1.6s done
#6 extracting sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3
#6 extracting sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3 0.6s done
#6 DONE 2.3s

#6 [1/7] FROM docker.io/library/python:3.11-slim@sha256:a0939570b38cddeb861b8e75d20b1c8218b21562b18f301171904b544e8cf228
#6 extracting sha256:11b89692b2085631f6e2407edd8545b033c8e6945837103875d6db484e945b6f 0.1s done
#6 extracting sha256:764e05fe66b6768e40fa2a21d5108eceb8f3f8f2c32463d72c109c54dde0d5c1
#6 extracting sha256:764e05fe66b6768e40fa2a21d5108eceb8f3f8f2c32463d72c109c54dde0d5c1 0.4s done
#6 DONE 2.8s

#6 [1/7] FROM docker.io/library/python:3.11-slim@sha256:a0939570b38cddeb861b8e75d20b1c8218b21562b18f301171904b544e8cf228
#6 extracting sha256:a4aefcec16c5bdc01af2ad1c5341b420d4179f3b825c0dc866367fb43f0d50ac done
#6 DONE 2.8s

#7 [2/7] RUN useradd -m fastapiuser
#7 DONE 0.2s

#8 [3/7] WORKDIR /app
#8 DONE 0.0s

#9 [4/7] COPY requirements.txt .
#9 DONE 0.0s

#10 [5/7] RUN pip install --no-cache-dir -r requirements.txt
#10 1.511 Collecting fastapi (from -r requirements.txt (line 1))
#10 1.598   Downloading fastapi-0.116.2-py3-none-any.whl.metadata (28 kB)
#10 1.639 Collecting jinja2 (from -r requirements.txt (line 3))
#10 1.658   Downloading jinja2-3.1.6-py3-none-any.whl.metadata (2.9 kB)
#10 1.705 Collecting uvicorn[standard] (from -r requirements.txt (line 2))
#10 1.723   Downloading uvicorn-0.35.0-py3-none-any.whl.metadata (6.5 kB)
#10 1.795 Collecting starlette<0.49.0,>=0.40.0 (from fastapi->-r requirements.txt (line 1))
#10 1.814   Downloading starlette-0.48.0-py3-none-any.whl.metadata (6.3 kB)
#10 2.001 Collecting pydantic!=1.8,!=1.8.1,!=2.0.0,!=2.0.1,!=2.1.0,<3.0.0,>=1.7.4 (from fastapi->-r requirements.txt (line 1))
#10 2.020   Downloading pydantic-2.11.9-py3-none-any.whl.metadata (68 kB)
#10 2.039      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 68.4/68.4 kB 3.5 MB/s eta 0:00:00
#10 2.078 Collecting typing-extensions>=4.8.0 (from fastapi->-r requirements.txt (line 1))
#10 2.097   Downloading typing_extensions-4.15.0-py3-none-any.whl.metadata (3.3 kB)
#10 2.147 Collecting click>=7.0 (from uvicorn[standard]->-r requirements.txt (line 2))
#10 2.168   Downloading click-8.2.1-py3-none-any.whl.metadata (2.5 kB)
#10 2.196 Collecting h11>=0.8 (from uvicorn[standard]->-r requirements.txt (line 2))
#10 2.215   Downloading h11-0.16.0-py3-none-any.whl.metadata (8.3 kB)
#10 2.262 Collecting httptools>=0.6.3 (from uvicorn[standard]->-r requirements.txt (line 2))
#10 2.281   Downloading httptools-0.6.4-cp311-cp311-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (3.6 kB)
#10 2.316 Collecting python-dotenv>=0.13 (from uvicorn[standard]->-r requirements.txt (line 2))
#10 2.335   Downloading python_dotenv-1.1.1-py3-none-any.whl.metadata (24 kB)
#10 2.407 Collecting pyyaml>=5.1 (from uvicorn[standard]->-r requirements.txt (line 2))
#10 2.426   Downloading PyYAML-6.0.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (2.1 kB)
#10 2.484 Collecting uvloop>=0.15.1 (from uvicorn[standard]->-r requirements.txt (line 2))
#10 2.503   Downloading uvloop-0.21.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (4.9 kB)
#10 2.592 Collecting watchfiles>=0.13 (from uvicorn[standard]->-r requirements.txt (line 2))
#10 2.612   Downloading watchfiles-1.1.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (4.9 kB)
#10 2.721 Collecting websockets>=10.4 (from uvicorn[standard]->-r requirements.txt (line 2))
#10 2.740   Downloading websockets-15.0.1-cp311-cp311-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (6.8 kB)
#10 2.809 Collecting MarkupSafe>=2.0 (from jinja2->-r requirements.txt (line 3))
#10 2.827   Downloading MarkupSafe-3.0.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (4.0 kB)
#10 2.867 Collecting annotated-types>=0.6.0 (from pydantic!=1.8,!=1.8.1,!=2.0.0,!=2.0.1,!=2.1.0,<3.0.0,>=1.7.4->fastapi->-r requirements.txt (line 1))
#10 2.885   Downloading annotated_types-0.7.0-py3-none-any.whl.metadata (15 kB)
#10 3.592 Collecting pydantic-core==2.33.2 (from pydantic!=1.8,!=1.8.1,!=2.0.0,!=2.0.1,!=2.1.0,<3.0.0,>=1.7.4->fastapi->-r requirements.txt (line 1))
#10 3.611   Downloading pydantic_core-2.33.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (6.8 kB)
#10 3.643 Collecting typing-inspection>=0.4.0 (from pydantic!=1.8,!=1.8.1,!=2.0.0,!=2.0.1,!=2.1.0,<3.0.0,>=1.7.4->fastapi->-r requirements.txt (line 1))
#10 3.661   Downloading typing_inspection-0.4.1-py3-none-any.whl.metadata (2.6 kB)
#10 3.718 Collecting anyio<5,>=3.6.2 (from starlette<0.49.0,>=0.40.0->fastapi->-r requirements.txt (line 1))
#10 3.737   Downloading anyio-4.10.0-py3-none-any.whl.metadata (4.0 kB)
#10 3.807 Collecting idna>=2.8 (from anyio<5,>=3.6.2->starlette<0.49.0,>=0.40.0->fastapi->-r requirements.txt (line 1))
#10 3.826   Downloading idna-3.10-py3-none-any.whl.metadata (10 kB)
#10 3.853 Collecting sniffio>=1.1 (from anyio<5,>=3.6.2->starlette<0.49.0,>=0.40.0->fastapi->-r requirements.txt (line 1))
#10 3.872   Downloading sniffio-1.3.1-py3-none-any.whl.metadata (3.9 kB)
#10 3.915 Downloading fastapi-0.116.2-py3-none-any.whl (95 kB)
#10 3.923    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 95.7/95.7 kB 13.7 MB/s eta 0:00:00
#10 3.942 Downloading jinja2-3.1.6-py3-none-any.whl (134 kB)
#10 3.950    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 134.9/134.9 kB 22.6 MB/s eta 0:00:00
#10 3.968 Downloading click-8.2.1-py3-none-any.whl (102 kB)
#10 3.972    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 102.2/102.2 kB 51.6 MB/s eta 0:00:00
#10 3.991 Downloading h11-0.16.0-py3-none-any.whl (37 kB)
#10 4.013 Downloading httptools-0.6.4-cp311-cp311-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (459 kB)
#10 4.034    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 459.8/459.8 kB 23.4 MB/s eta 0:00:00
#10 4.053 Downloading MarkupSafe-3.0.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (23 kB)
#10 4.072 Downloading pydantic-2.11.9-py3-none-any.whl (444 kB)
#10 4.077    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 444.9/444.9 kB 128.5 MB/s eta 0:00:00
#10 4.096 Downloading pydantic_core-2.33.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (2.0 MB)
#10 4.120    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.0/2.0 MB 86.8 MB/s eta 0:00:00
#10 4.139 Downloading python_dotenv-1.1.1-py3-none-any.whl (20 kB)
#10 4.159 Downloading PyYAML-6.0.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (762 kB)
#10 4.166    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 763.0/763.0 kB 174.8 MB/s eta 0:00:00
#10 4.186 Downloading starlette-0.48.0-py3-none-any.whl (73 kB)
#10 4.188    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 73.7/73.7 kB 289.9 MB/s eta 0:00:00
#10 4.215 Downloading typing_extensions-4.15.0-py3-none-any.whl (44 kB)
#10 4.217    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 44.6/44.6 kB 198.2 MB/s eta 0:00:00
#10 4.237 Downloading uvloop-0.21.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (4.0 MB)
#10 4.261    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 4.0/4.0 MB 186.2 MB/s eta 0:00:00
#10 4.281 Downloading watchfiles-1.1.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (453 kB)
#10 4.284    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 453.1/453.1 kB 319.3 MB/s eta 0:00:00
#10 4.303 Downloading websockets-15.0.1-cp311-cp311-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (182 kB)
#10 4.306    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 182.3/182.3 kB 287.2 MB/s eta 0:00:00
#10 4.324 Downloading uvicorn-0.35.0-py3-none-any.whl (66 kB)
#10 4.326    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 66.4/66.4 kB 243.1 MB/s eta 0:00:00
#10 4.345 Downloading annotated_types-0.7.0-py3-none-any.whl (13 kB)
#10 4.365 Downloading anyio-4.10.0-py3-none-any.whl (107 kB)
#10 4.367    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 107.2/107.2 kB 215.3 MB/s eta 0:00:00
#10 4.386 Downloading typing_inspection-0.4.1-py3-none-any.whl (14 kB)
#10 4.405 Downloading idna-3.10-py3-none-any.whl (70 kB)
#10 4.407    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 70.4/70.4 kB 300.3 MB/s eta 0:00:00
#10 4.427 Downloading sniffio-1.3.1-py3-none-any.whl (10 kB)
#10 4.537 Installing collected packages: websockets, uvloop, typing-extensions, sniffio, pyyaml, python-dotenv, MarkupSafe, idna, httptools, h11, click, annotated-types, uvicorn, typing-inspection, pydantic-core, jinja2, anyio, watchfiles, starlette, pydantic, fastapi
#10 5.593 Successfully installed MarkupSafe-3.0.2 annotated-types-0.7.0 anyio-4.10.0 click-8.2.1 fastapi-0.116.2 h11-0.16.0 httptools-0.6.4 idna-3.10 jinja2-3.1.6 pydantic-2.11.9 pydantic-core-2.33.2 python-dotenv-1.1.1 pyyaml-6.0.2 sniffio-1.3.1 starlette-0.48.0 typing-extensions-4.15.0 typing-inspection-0.4.1 uvicorn-0.35.0 uvloop-0.21.0 watchfiles-1.1.0 websockets-15.0.1
#10 5.593 WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv
#10 5.715 
#10 5.715 [notice] A new release of pip is available: 24.0 -> 25.2
#10 5.715 [notice] To update, run: pip install --upgrade pip
#10 DONE 5.9s

#11 [6/7] COPY . .
#11 DONE 0.0s

#12 [7/7] RUN chown -R fastapiuser:fastapiuser /app
#12 DONE 0.1s

#13 exporting to docker image format
#13 exporting layers
#13 exporting layers 1.7s done
#13 exporting manifest sha256:159cc3683b94da192134b4837ca2bbfe1af06294661198177428cd3a9fe643ec done
#13 exporting config sha256:d47d43e6c2e77c70089f42e9f98a935a8071d9f516f4ce2102899243163d8778 done
#13 sending tarball
#13 sending tarball 2.9s done
#13 DONE 4.6s

#14 importing to docker
#14 loading layer daf557c4f08e 29.77MB / 29.77MB 2.5s done
#14 loading layer 135aac4d5c9a 1.29MB / 1.29MB 1.7s done
#14 loading layer 49dd736005c7 14.64MB / 14.64MB 1.4s done
#14 loading layer 8d441cbfbc35 250B / 250B 0.8s done
#14 loading layer 05ae1e3b7543 3.31kB / 3.31kB 0.8s done
#14 loading layer f3f5c2efac32 92B / 92B 0.7s done
#14 loading layer bf320ef8f830 174B / 174B 0.7s done
#14 loading layer 334e6c1e8c5e 15.71MB / 15.71MB 0.7s done
#14 loading layer 9ddac07d1d7c 19.85kB / 19.85kB 0.1s done
#14 loading layer 99de79f1235c 19.89kB / 19.89kB 0.0s done
#14 DONE 2.5s

#15 resolving provenance for metadata file
#15 DONE 0.0s
ImageID
Digest
Metadata
Reference
Check build summary support
3s
Run mkdir -p ~/.docker/cli-plugins
[info] fetching release script for tag='v1.18.3' 
[info] using release tag='v1.18.3' version='1.18.3' os='linux' arch='amd64' 
[info] installed /home/runner/.docker/cli-plugins/docker-scout 

      ⢀⢀⢀             ⣀⣀⡤⣔⢖⣖⢽⢝
   ⡠⡢⡣⡣⡣⡣⡣⡣⡢⡀    ⢀⣠⢴⡲⣫⡺⣜⢞⢮⡳⡵⡹⡅
  ⡜⡜⡜⡜⡜⡜⠜⠈⠈        ⠁⠙⠮⣺⡪⡯⣺⡪⡯⣺ 
 ⢘⢜⢜⢜⢜⠜               ⠈⠪⡳⡵⣹⡪⠇ 
 ⠨⡪⡪⡪⠂    ⢀⡤⣖⢽⡹⣝⡝⣖⢤⡀    ⠘⢝⢮⡚       _____                 _   
  ⠱⡱⠁    ⡴⡫⣞⢮⡳⣝⢮⡺⣪⡳⣝⢦    ⠘⡵⠁      / ____| Docker        | |  
   ⠁    ⣸⢝⣕⢗⡵⣝⢮⡳⣝⢮⡺⣪⡳⣣    ⠁      | (___   ___ ___  _   _| |_ 
        ⣗⣝⢮⡳⣝⢮⡳⣝⢮⡳⣝⢮⢮⡳            \___ \ / __/ _ \| | | | __|
   ⢀    ⢱⡳⡵⣹⡪⡳⣝⢮⡳⣝⢮⡳⡣⡏    ⡀       ____) | (_| (_) | |_| | |_ 
  ⢀⢾⠄    ⠫⣞⢮⡺⣝⢮⡳⣝⢮⡳⣝⠝    ⢠⢣⢂     |_____/ \___\___/ \__,_|\__|
  ⡼⣕⢗⡄    ⠈⠓⠝⢮⡳⣝⠮⠳⠙     ⢠⢢⢣⢣  
 ⢰⡫⡮⡳⣝⢦⡀              ⢀⢔⢕⢕⢕⢕⠅ 
 ⡯⣎⢯⡺⣪⡳⣝⢖⣄⣀        ⡀⡠⡢⡣⡣⡣⡣⡣⡃  
⢸⢝⢮⡳⣝⢮⡺⣪⡳⠕⠗⠉⠁    ⠘⠜⡜⡜⡜⡜⡜⡜⠜⠈   
⡯⡳⠳⠝⠊⠓⠉             ⠈⠈⠈⠈      



version: v1.18.3 (go1.24.6 - linux/amd64)
git commit: aa68fc25c596bea659d54867443238fd30218d23
14s
Run echo "🔍 Ejecutando análisis de vulnerabilidades con Docker Scout..."
🔍 Ejecutando análisis de vulnerabilidades con Docker Scout...
    ...Storing image for indexing
    ✓ Image stored for indexing
    ...Indexing
    ✓ Indexed 147 packages
    ✗ Detected 11 vulnerable packages with a total of 23 vulnerabilities
    ✓ Report written to json
==== Resumen de vulnerabilidades detectadas ====
    ...Storing image for indexing
    ✓ Image stored for indexing
    ...Indexing
    ✓ Indexed 147 packages
    ✗ Detected 11 vulnerable packages with a total of 23 vulnerabilities
    ✓ Report written to json
1s
Run actions/upload-artifact@v4
With the provided path, there will be 1 file uploaded
Artifact name is valid!
Root directory input is valid!
Beginning upload of artifact content to blob storage
Uploaded bytes 287
Finished uploading artifact content to blob storage!
SHA256 digest of uploaded artifact zip is c68f067140ca1299f2b133fa2711981d3b473c5343dc40a917b37c576f0c7c92
Finalizing artifact upload
Artifact docker-scout-report.zip successfully finalized. Artifact ID 4048225463
Artifact docker-scout-report has been successfully uploaded! Final size is 287 bytes. Artifact ID is 4048225463
Artifact download URL: https://github.com/***/fastapi-app-scout/actions/runs/17836320239/artifacts/4048225463
1s
Post job cleanup.
Generating build summary
Removing temp folder /home/runner/work/_temp/docker-actions-toolkit-h3PX6H
Post cache
1s
Post job cleanup.
Removing builder
Cleaning up certificates
Post cache
1s
Post job cleanup.
/usr/bin/docker logout 
Removing login credentials for https://index.docker.io/v1/
Post cache
0s
Post job cleanup.
/usr/bin/git version
git version 2.51.0
Temporarily overriding HOME='/home/runner/work/_temp/9ab4a237-90b1-4a72-a8d4-1f162bccc4b8' before making global git config changes
Adding repository directory to the temporary git global config as a safe directory
/usr/bin/git config --global --add safe.directory /home/runner/work/fastapi-app-scout/fastapi-app-scout
/usr/bin/git config --local --name-only --get-regexp core\.sshCommand
/usr/bin/git submodule foreach --recursive sh -c "git config --local --name-only --get-regexp 'core\.sshCommand' && git config --local --unset-all 'core.sshCommand' || :"
/usr/bin/git config --local --name-only --get-regexp http\.https\:\/\/github\.com\/\.extraheader
http.https://github.com/.extraheader
/usr/bin/git config --local --unset-all http.https://github.com/.extraheader
/usr/bin/git submodule foreach --recursive sh -c "git config --local --name-only --get-regexp 'http\.https\:\/\/github\.com\/\.extraheader' && git config --local --unset-all 'http.https://github.com/.extraheader' || :"
0s
Cleaning up orphan processes

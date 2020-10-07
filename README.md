# yank_tutorial
## 0. Overview 
[Yank](http://getyank.org/latest/)는 [openmm MD 패키지](http://openmm.org/)를 이용해서 **absolute binding free energy** 계산을 쉽게 수행할 수 있도록 해주는 패키지이다. 
### 0.1. 장점
        1. 복잡한 시스템 셋팅을 하나의 yaml 파일에서 할 수 있도록 간소화 해준다. 
        2. simulation이 converge 되었는지 자동으로 판별하는 기능을 가지고 있다. 
        3. CUDA engine을 이용해서 상당히 빠르다.
        
### 0.2. 단점
        1. atom이 몇 개 변화하는 relative binding free energy 계산은 불가능하다.  
        2. 원하는 추가적인 restraint를 넣는 것이 쉽지 않다. 
        3. ... maybe more? ...

## 1. Yank의 설치
conda를 이용해서 쉽게 설치할 수 있다.
다른 패키지와의 충돌을 피하기 위해서 가상환경을 생성하여 설치하는 것을 추천한다.
만일 가상환경 이름을 yank_env 라고 정했다고 가정하면 다음과 같이 명령을 실행시키면 된다. 
    
    conda create -n yank_env python 
    conda config --add channels omnia --add channels conda-forge
    conda install -c omnia yank yank-examples
    
설치가 끝난후 가상환경을 activate 한 후에 해당 가상환경에서 yank를 실행시킨다. 
 
    conda activate yank_env
    
어떤 위치에 yank가 설치되었는지를 which 명령어로 확인한 후에 해당 binary를 slurm에서 사용한다. 

    which yank
    

## 2. Quick start 
* 

## 3. Options


## 4. Theory
    
****
* misc
> For Linux 64, Open MPI is built with CUDA awareness but this support is disabled by default.
To enable it, please set the environmental variable OMPI_MCA_opal_cuda_support=true before
launching your MPI processes. Equivalently, you can set the MCA parameter in the command line:
mpiexec --mca opal_cuda_support 1 ...

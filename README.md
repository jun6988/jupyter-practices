miniconda & jupyter 설치하는법
miniconda 다운로드

microsoft terminal 다운로드

https://windowsterminalthemes.dev/ 에서 원하는 theme 다운로드

환경변수 -> 시스템변수에서 miniconda script 파일까지 추가

miniconda01

(관리자권한 powershell에서) Set-ExecutionPolicy RemoteSigned

(conda prompt에서) conda init powershell

(다운받은 terminal에서) conda config --set auto_activate_base False

conda activate <<< (다음 실행할때는 conda activate mldl-env)
conda env list
conda create -n mldl-env python=3.8 <<<< 가상환경 설치 (install은 경로가 아닌 어느 가상환경에 설치할것인지가 중요)
conda install numpy
conda install pandas
conda install matplotlib
conda install jupyter
conda install scikit-learn
conda list

pip install mglearn

conda install graphviz
pip install graphviz ---> (환경변수에서 시스템변수 추가) C:\Users\BIT\miniconda3\envs\mldl-env\Lib\site-packages\graphviz

conda install tensorflow
conda install seaborn

자연어 토크나이징
conda install -c anaconda nltk
conda install -c conda-forge spacy-model-en_core_web_sm

한글 토크나이징
(시스템변수에서) 새로만들기 -> 변수 JAVA_HOME 추가 -> 경로는 C:\Program Files\Java\jdk-12.0.1
-> (환경변수편집에서) 새로만들기 -> 변수 %JAVA_HOME%\bin 추가
-> (mldl-env들어가서) conda install -c conda-forge jpype1 -> pip install konlpy
-> (Terminal, notebook 다 끄고 다시실행)

conda install -c conda-forge wordcloud

(원하는 경로로 간다음) jupyter notebook <<<< jupyter 실행

jupyter 기본사용법
편집모드

ctrl + 엔터 = 현재 행 실행
shift + 엔터 = 현재 행 실행하고 다음 행 생성
커맨드모드

dd = 현재 행 삭제
a = (현재 행 기준) 앞쪽에 새 행 생성
b = (현재 행 기준) 뒤쪽에 새 행 생성

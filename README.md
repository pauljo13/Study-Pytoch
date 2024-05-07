# Study-PyToch
## day 1
### PyToch
파이토치(PyToch)는 딥러닝 모델을 구축하고 훈련시키는 데 사용되는 오픈 소스 딥러닝 프레임워크입니다.
 1. 동적 그래프(Dynamic Computational Graph) :
    - 파이토치는 동적 그래프를 사용하여 딥러닝 모델을 정의하고 실행한다. 이는 계산 그래프가 런타임 중에 정의되고 변경될 수 있다는 것을 의미한다. 이러한 접근 방식은 모델의 작성과 디버깅을 단순화하고, 유연성을 제공한다.
 2. 모듈화된 구성요소 :
    - 파이토치에서는 다양한 모듈화된 구성요소를 제공하여 딥러닝 모델을 구축한다.
 3. 텐서(Tensor) : 
    - 파이토치에서는 텐서(tensor)라고 불리는 다차원 배열을 기본 데이터 구조로 사용한다. 텐서는 넘파이(NumPy) 배열과 유사하지만, GPU를 사용하여 연산을 가속화할 수 있다.
 4. 자동 미분(Automatic Differentiation) :
    - 파이토치는 자동 미분을 지원하여 역전파(backpropagation)를 쉽게 수행할 수 있다. 이는 딥러닝 모델을 훈련시킬 때 그래디언트를 자동으로 계산하여 모델의 매개변수를 최적화하는 데 도움을 준다.
 5. 신경망 모듈(Neural Network Module) :
    - 파이토치는 신경망 모듈이라는 모듈화된 구성 요소를 제공하여 딥러닝 모델을 쉽게 구축할 수 있다. 이 모듈은 레이어(layer), 활성화 함수(activation function), 손실함수(loss function)등 다양한 요소로 구성된다.
 6. GPU 가속 :
    - 파이토치는 CUDA를 사용하여 GPU 가속을 지원한다. 따라서 대규모 데이터셋과 복잡한 모델을 효율적으로 처리할 수 있다.
 7. 편리한 API :
    - 파이토치는 사용자 친화적인 API를 제공하여 빠르고 쉽게 딥러닝 모델을 구축하고 훈련시킬 수 있다. 이는 코드를 간결하게 작성하소 이해하기 쉽게 만들어준다.
 8. 확장성 :
    - 파이토치는 모듈화된 디자인을 통해 확장성이 높다. 이는 사용자가 필요에 따라 커스텀한 모델과 기능을 쉽게 추가학소 확장할 수 있다.
 9. 편리한 데이터 로딩 및 전처리 :
    - "torchvision", "torchtext" 등의 라이브러리를 통해 이미지, 텍스트 등 다양한 유형의 데이터를 쉽게 로드하고 전처리할 수 있다.
     
### 데이터 작업하기
파이토치(PyToch)에는 데이터 작업을 위한 기본 요소 두가지인 torch.utils.data.DataLoader 와 torch.utils.data.Dataset가 있다.
   - Dataset : 샘플과 정답(label)을 저장
   - DataLoader : Dataset을 순회 가장한 객체(iterable)로 감싼다.
torchvision.datasets 모듈은 CIFAR, COCO 등과 같은 다양한 실제 비전(vision) 데이터에 대한 Dataset을 포함하고 있다. 모든 TorchVision Dataset은 샘플과 정답을 각각 변경하기 위한 transform 과 target_transform의 두 인자를 포함한다.  
Dataset을 DataLoader의 인자로 전달한다. 이는 데이터셋을 순회 가능한 객체(iterble)로 감싸고, 자동화된 배치(batch), 샘플링(sampling), 섞기(shuffle) 및 다중 프로세스로 데이터 불러오기를 지원한다. 여기서는 배치 크기를 64로 정의한다. 즉, 데이터로더 객체의 각 요소는 64개의 특징과 정답을 묶음으로 반환한다.

# Hair removal for colab

+) 필요한 dcm(dicom) 파일을 불러오는 과정은 hair_labeling 디렉토리의 README를 동일하게 참조하시면 된다.
해당 디렉토리에서 버전이 가장 높은 최신 hair_removal 코드를 사용하면 된다.

## 구현 결과

### 1. 원본 이미지
![original_image](https://user-images.githubusercontent.com/39727494/87151481-e2206400-c2ee-11ea-8cdf-b5e34ca89d6e.png)

### 2. 원본 이미지 흑백화
![grayscaled_image](https://user-images.githubusercontent.com/39727494/87151479-e187cd80-c2ee-11ea-9b41-cb18b03f458d.png)

### 3. blackhat filtering result
![blackHat_filtering_result](https://user-images.githubusercontent.com/39727494/87151478-e0ef3700-c2ee-11ea-9af1-5928f4109c31.png)

### 4. inpainting을 위한 임계값 찾기
![Thresholded_image_for_inpainting](https://user-images.githubusercontent.com/39727494/87151476-e0ef3700-c2ee-11ea-9967-42fa11530a93.png)

### 5. 결과
![image_after_inpainting](https://user-images.githubusercontent.com/39727494/87151474-e056a080-c2ee-11ea-9e03-da6e263a2ab9.png)

### 6. 원본과 결과 비교
![result](https://user-images.githubusercontent.com/39727494/87151472-df257380-c2ee-11ea-8901-487a5e89dfe2.png)

### 7. 결과
각 단계의 숫자들을 조율하여 최적의 inpainting 결과를 도출하거나, 거듭한 inpainting을 시도해 보는 등의 방법을 통해 hair removal의 정확도를 높여야할 것 같다.

#### +) 기타 문제점
##### 1. 이미지 마다 용량이 다른데 사이즈가 클수록 inpainting하는데 걸리는 시간이 기하급수적으로 증가한다. 이 부분을 해결해야 한다. 아무래도 scaling 작업을 
##### 2. 이거 언제 다 쳐하고 앉았지? 망해버렸다. hair 라벨링 결과로 이 작업 수행량을 줄여야 할 것 같다.
##### 3. 피부병 발생 부위와 모발의 색이 유사하면 inpainting 정확도가 확연히 낮아진다. 이 부분을 해결하려면 다른 방법을 도입해야할 것 같다.


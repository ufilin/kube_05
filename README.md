# kube_05

## Задание 1. Volume: обмен данными между контейнерами в поде

### Манифесты

**[deploy_task1.yaml](https://github.com/ufilin/kube_05/blob/main/deploy_task1.yaml)**

Дополнительно прикладываю файл результата вывода "kubectl describe pods" для удобства чтения:

**[kubectl describe pods](https://github.com/ufilin/kube_05/blob/main/k_describe_pods.txt)**

### Описание пода с контейнерами

<p align="center">
  <img src="kube_05-1-1.png" width="800">
</p>

<p align="center">
  <img src="kube_05-1-2.png" width="800">
</p>

### Вывод команды чтения файла

<p align="center">
  <img src="kube_05-1-3.png" width="800">
</p>

## Задание 2. PV, PVC

### Манифесты

**[pv_task1.yaml](https://github.com/ufilin/kube_05/blob/main/pv_task2.yaml)**
**[pvc_task1.yaml](https://github.com/ufilin/kube_05/blob/main/pvc_task2.yaml)**

### PV и PVC

<p align="center">
  <img src="kube_05-2-1.png" width="800">
</p>

### Демонстрация доступности из контейнера multitool

<p align="center">
  <img src="kube_05-2-2.png" width="800">
</p>

### Состояние PV после удаления Deployment and PVC

<p align="center">
  <img src="kube_05-2-3.png" width="800">
</p>

Состояние поменялось на Released в связи с тем что reclaim policy установлено retain. PV не удаляется и не может быть переиспользовано новым PVC.

### Состояние файл "до" и "после" удаления PV

<p align="center">
  <img src="kube_05-2-4.png" width="800">
</p>
  
<p align="center">
  <img src="kube_05-2-5.png" width="800">
</p>

Файл на Node не трогается в связи с выбранной политикой Retain. В случае работы с PV с использованием данной политики файл остаётся не тронутым, правяться только метаданные в etcd.

## Задание 3. StorageClass

### Манифесты

**[sc_task3.yaml](https://github.com/ufilin/kube_05/blob/main/sc_task3.yaml)**

### Демонстрация всех созданных элементов и доступность данных из контейнера multitool

<p align="center">
  <img src="kube_05-3-1.png" width="800">
</p>

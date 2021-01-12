# MNIST example with MLFlow

### Запуск кода

С дефолтными параметрами:
```
mlflow run .
```

С кастомными параметрами:

```
mlflow run . -P max_epochs=X
```
или
```
mlflow run . -P max_epochs=5 -P gpus=1 -P batch_size=32 -P num_workers=2 -P learning_rate=0.01 -P accelerator="ddp" -P patience=5 -P mode="min" -P monitor="val_loss" -P verbose=True
```

Если среда, в которой запускается код имеет все необходимые модули, то для запуска добавьте аргумент `--no-conda`
```
mlflow run . --no-conda
```

### Просмотр результатов в MLFlow UI

Как только код завершил свою работу, результаты тренировки можно посмотреть в веб интерфейсе, для этого пропишите
```
mlflow ui
```

и перейдите по  http://localhost:5000

# Задача 1

## **Пункт - 1**

![Снимок экрана от 2024-01-17 21-46-43](https://github.com/JustAleksy/introduction_to_terraform/assets/143338652/ce4e388b-79c2-43e1-a78a-c164b93ed935)

## **Пункт - 2**

![Снимок экрана от 2024-01-18 22-28-21](https://github.com/JustAleksy/introduction_to_terraform/assets/143338652/014c4778-7430-421d-8a4a-881dd1b15341)

## **Пункт - 3**

Не очень понял, ну наверное оно:  
"result": "Nx20O14HTfgS1RQG"

## **Пункт - 4**

![Снимок экрана от 2024-01-18 21-34-38](https://github.com/JustAleksy/introduction_to_terraform/assets/143338652/2f6b61a5-081c-45d8-b2b3-8c4bbb88ef7a)

## **Пункт - 5**

![Снимок экрана от 2024-01-18 21-47-27](https://github.com/JustAleksy/introduction_to_terraform/assets/143338652/0d235e65-3616-4657-9c93-5f1495bb5230)
![Снимок экрана от 2024-01-18 21-47-46](https://github.com/JustAleksy/introduction_to_terraform/assets/143338652/2e9fe079-7eb1-4baa-952e-6071a61e4ec9)

## **Пункт 6**

![Снимок экрана от 2024-01-18 21-51-19](https://github.com/JustAleksy/introduction_to_terraform/assets/143338652/5ecc3193-752a-4e4e-a1b7-26db88d90026)
![Снимок экрана от 2024-01-18 21-56-13](https://github.com/JustAleksy/introduction_to_terraform/assets/143338652/f61d0288-097f-4237-8d66-bce59de389f3)

## **Пункт - 7**
Содержимое terraform.tfstate  
```terraform
{
  "version": 4,
  "terraform_version": "1.5.7",
  "serial": 37,
  "lineage": "0a45c26c-7e22-de4c-1c0a-0978b13afb18",
  "outputs": {},
  "resources": [],
  "check_results": null
}
```

## **Пункт - 8**

`keep_locally = true` - а это значит что образ не удаляется при дестрое.  
```terraform
resource "docker_image" "nginx" {
  name         = "nginx:latest"
  keep_locally = true
}
```
`keep_locally = false` - для удаления.  
```terraform
resource "docker_image" "nginx" {
  name         = "nginx:latest"
  keep_locally = false
}
```
> **`keep_locally`** (Boolean) If true, then the Docker image won't be deleted on destroy operation. If this is false, it will delete the image from the docker local storage on destroy operation.

![Снимок экрана от 2024-01-18 22-33-34](https://github.com/JustAleksy/introduction_to_terraform/assets/143338652/d7c84603-d221-4290-aa40-dd46770c4cc7)  


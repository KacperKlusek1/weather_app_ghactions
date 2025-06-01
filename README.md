# weather_app_ghactions
Repozytorium zadania 2 z Programowanie Aplikacji w Chmurze Obliczeniowej

# Opis łańcuchu Github Actions:
1. Pobranie kodu (actions/checkout@v4)
2. Ustawienie buildera buildx (docker/setup-buildx-action@v3)
3. Logowanie do DockerHuba (docker/login-action@v3)
4. Logowanie do repozytorium ghcr.io (docker/login-action@v3)
5. Zbudowanie tymczasowego obrazu w celu przeskanowania go (docker/build-push-action@v5)
6. Przeskanowanie obrazu za pomocą Trivy (aquasecurity/trivy-action@0.13.0) //Użyłem Trivy ponieważ nie wymaga logowania do konta Dockera + nie wymaga żeby obraz był spushowany na ghcr.io, działa lokalnie
7. Budowanie i pushowanie obrazów dla obu architektur (docker/build-push-action@v5)

# Potwierdzenie wykonania workflow:
![obraz](https://github.com/user-attachments/assets/b4ffd4ee-550f-41d0-8729-d397e658b897)


# Potwierdzenie zapisania cache na DockerHubie:
![obraz](https://github.com/user-attachments/assets/4b18e8f6-b46f-4561-b96f-4107a409c446)

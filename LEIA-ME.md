# Força & Foco: gerar o APK

## Opção 1: sem instalar nada (GitHub)
1. Crie uma conta e um repositório novo em github.com.
2. Envie todo o conteúdo desta pasta (incluindo a pasta .github).
3. Abra a aba Actions, escolha "Build APK" e aguarde uns 5 minutos.
4. Baixe o arquivo forca-e-foco-apk (Artifacts), extraia e instale o app-debug.apk no celular.
   No Android, permita "instalar apps de fontes desconhecidas" quando pedir.

## Opção 2: no computador
Requisitos: Node 20+, Java 17 e Android Studio (SDK).
    npm install
    npx cap add android
    npx cap sync android
    cd android && ./gradlew assembleDebug
O APK fica em android/app/build/outputs/apk/debug/app-debug.apk

## Observações
- Seus dados ficam salvos no próprio app (localStorage).
- O IA Coach usa o ambiente do Claude e não funciona fora do claude.ai. No APK ele mostra aviso de indisponível.
- Para editar o app, altere www/index.html e rode "npx cap sync android" antes de gerar de novo.

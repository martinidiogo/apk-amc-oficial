# AMC Consistem – App Android (PWA)

Abre https://consistem.amctextil.com.br/ em tela cheia, sem barra de endereços
e com o botão/gesto "Voltar" desativado.

## Gerar o APK

### Opção A – GitHub (sem instalar nada)
1. Crie um repositório no GitHub e envie esta pasta.
2. Aba **Actions** → workflow **Gerar APK** roda sozinho.
3. Ao terminar, baixe o artefato **AMCConsistem-apk** (zip com o `app-debug.apk`).

### Opção B – Android Studio
1. File → Open → selecione esta pasta.
2. Build → Build App Bundle(s) / APK(s) → Build APK(s).
3. APK em `app/build/outputs/apk/debug/app-debug.apk`.

### Opção C – Linha de comando (com Android SDK + JDK 17)
    ./gradlew assembleDebug

## Ajustes rápidos
- URL: `app/build.gradle.kts` → `START_URL`
- Nome do app: `app/src/main/res/values/strings.xml`
- Cor: `app/src/main/res/values/colors.xml`
- Tela cheia (ocultar barras do sistema): `FULLSCREEN` em `MainActivity.kt`
- Domínio que permanece dentro do app: `ALLOWED_DOMAIN` em `MainActivity.kt`

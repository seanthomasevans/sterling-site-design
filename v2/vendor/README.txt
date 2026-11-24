elevenlabs-client-1.26.0.js: @elevenlabs/client 1.26.0 (MIT) bundled with its dependencies (livekit-client, Apache-2.0,
and others; licence notices at the end of the file) into one ES module (named .js so every host serves it as JavaScript) by esbuild 0.25, so the site assistant loads no
code from a CDN at chat time. Rebuild: npm i @elevenlabs/client@<version> esbuild; entry `export { Conversation } from
'@elevenlabs/client'`; esbuild entry.js --bundle --format=esm --platform=browser --minify --legal-comments=eof --target=es2020.
Text-only chat never fetches the audio resampler worklet the bundle references on cdn.jsdelivr.net (voice mode only).

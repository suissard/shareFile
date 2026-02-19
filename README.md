# ShareFile
## 📁 Partage de Fichiers P2P

Une application web simple et légère pour partager des fichiers directement entre deux appareils, sans aucun serveur intermédiaire (Peer-to-Peer).


## ✨ Fonctionnalités

+ 100% P2P : Transfert direct via WebRTC grâce à PeerJS. Aucune donnée n'est stockée sur un serveur.

+ Facile d'accès : Génération automatique d'un QR Code et d'un lien à partager.

+ Gros fichiers : Support du transfert de fichiers volumineux grâce au découpage des données en morceaux (chunking).

+ Suivi en temps réel : Barre de progression intégrée pour l'émission et la réception.

+ Zéro installation : Fonctionne directement dans le navigateur avec un simple fichier HTML.


## 🛠️ Technologies utilisées

+ HTML5 / JavaScript Vanilla

+ Tailwind CSS (CDN) pour le style.

+ PeerJS pour la connexion WebRTC simplifiée.

+ QRCode.js pour la génération du QR Code.


## 🚀 Comment l'utiliser

### Option 1 : Hébergement Web (Recommandé)

Pour partager des fichiers entre n'importe quels appareils (PC, mobile, etc.) de manière optimale :

Hébergez le fichier index.html sur un service gratuit comme GitHub Pages, Vercel ou Netlify.

Ouvrez l'URL publique sur l'appareil récepteur.

Scannez le QR Code avec l'appareil émetteur.


### Option 2 : Réseau Local (LAN / Wi-Fi)

Pour un partage entre deux appareils connectés à la même box internet :

Ouvrez un terminal dans le dossier contenant index.html.

Lancez un serveur local basique (ex: avec Python) :

```python3 -m http.server 8080```


Trouvez votre IP locale (hostname -I sous Linux/Mac ou ipconfig sous Windows).

Allez sur http://VOTRE_IP:8080 sur l'appareil récepteur.

Scannez le QR Code avec le second appareil.

(Attention : Ouvrir directement le fichier en file:/// bloquera la génération du QR Code réseau et le transfert vers un autre appareil).


## 🔒 Confidentialité

Toutes les données transitent directement de navigateur à navigateur (chiffrement WebRTC natif). Aucun fichier n'est conservé ou intercepté.

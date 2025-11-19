# kibalenfant - IA Chat Agent Multimodal

🤖 **Kibali Enfant Agent** - Agent IA multimodal ultra-puissant avec chat intelligent

## 🚀 Fonctionnalités

- **Chat IA Multimodal** : Conversation intelligente avec analyse d'images et PDFs
- **Vision par Ordinateur** : SmolVLM-500M pour analyse visuelle avancée
- **Détection d'Objets** : YOLO TensorFlow.js pour reconnaissance d'objets
- **Raisonnement Avancé** : Mistral-7B pour génération de texte intelligente
- **Synthèse Vocale** : Coqui TTS pour voix naturelle en français
- **Recherche Web** : Tavily pour informations à jour
- **Mémoire Vectorielle** : FAISS pour recherche contextuelle
- **RAG (Retrieval Augmented Generation)** : Indexation intelligente de documents

## 🛠️ Technologies

- **Backend** : FastAPI (Python)
- **IA** : SmolVLM, YOLO, Mistral-7B, Coqui TTS
- **Vector Search** : FAISS
- **Web Search** : Tavily API
- **Container** : Docker
- **Déploiement** : Render

## 📁 Structure

```
backend/
├── chat_agent_api.py          # API principale FastAPI
├── unified_agent.py           # Agent IA multimodal
├── models/                    # Modèles IA (ignorés par git)
├── storage/                   # Données persistantes
├── requirements-*.txt         # Dépendances Python
├── Dockerfile.node            # Container pour déploiement
└── README.md                  # Cette documentation
```

## 🚀 Démarrage Rapide

1. **Cloner le repository**
   ```bash
   git clone https://github.com/lojol469-cmd/kibalenfant.git
   cd kibalenfant
   ```

2. **Installer les dépendances**
   ```bash
   pip install -r requirements-agent.txt
   pip install -r requirements-chat.txt
   ```

3. **Configurer les variables d'environnement**
   ```bash
   cp .env.example .env
   # Éditer .env avec vos clés API
   ```

4. **Lancer l'API**
   ```bash
   python chat_agent_api.py
   ```

L'API sera disponible sur `http://localhost:8001`

## 🔧 Configuration

### Variables d'Environnement (.env)
```env
# API Keys
TAVILY_API_KEY=votre_clé_tavily

# Modèles (chemins locaux)
SMOLVLM_PATH=models/smolvlm/cache
MISTRAL_PATH=models/mistral/mistral-7b-instruct-v0.2.Q4_K_M.gguf
TTS_PATH=models/tts/tts_models--fr--css10--vits
```

### Téléchargement des Modèles

Les modèles IA sont volumineux et ignorés par Git. Téléchargez-les séparément :

```bash
# SmolVLM (auto-téléchargement via HuggingFace)
# Mistral-7B (télécharger depuis HuggingFace)
# Coqui TTS (auto-téléchargement)
```

## 📡 API Endpoints

- `POST /chat` - Conversation avec l'agent IA
- `POST /upload` - Upload et analyse de fichiers
- `GET /conversation/{id}` - Historique des conversations
- `POST /search` - Recherche dans la mémoire vectorielle
- `GET /stats` - Statistiques du système

## 🐳 Docker

### Build et Run
```bash
# Build
docker build -f Dockerfile.node -t kibalenfant .

# Run
docker run -p 8001:8001 kibalenfant
```

### Docker Compose (local)
```bash
docker-compose -f docker-compose.node.yml up
```

## 🚀 Déploiement

### Render (recommandé)
1. Connecter le repository GitHub
2. Créer un Web Service
3. Configuration Docker : `Dockerfile.node`
4. Variables d'environnement dans Render

### Autres plateformes
- Railway, Heroku, DigitalOcean App Platform
- Support Docker natif

## 📊 Capacités de l'Agent

### 🤖 Chat Intelligent
- Détection automatique d'intention
- Conversation contextuelle
- Mémoire des interactions précédentes

### 👁️ Analyse Visuelle
- Description détaillée d'images
- Reconnaissance d'objets et scènes
- Analyse de documents scannés

### 📄 Traitement PDF
- Extraction de texte
- Analyse d'images dans les PDFs
- Chunking intelligent pour RAG

### 🔍 Recherche Web
- Informations à jour via Tavily
- Recherche contextuelle intelligente
- Intégration transparente

### 🗣️ Synthèse Vocale
- Voix naturelle en français
- Génération audio haute qualité
- Intégration avec le chat

## 🤝 Contribution

1. Fork le projet
2. Créer une branche feature
3. Commit vos changements
4. Push et créer une Pull Request

## 📄 Licence

MIT License - voir LICENSE pour plus de détails.

## 📞 Support

Pour toute question ou problème :
- Ouvrir une issue sur GitHub
- Contacter l'équipe de développement

---

**Développé avec ❤️ par Nyundu Francis Arnaud**

# Knowledge Graph RAG System

Cette application est un système avancé de **Retrieval-Augmented Generation (RAG)** qui combine la création de graphes de connaissances avec des réponses à des requêtes basées sur des documents. Elle s'appuie sur **Neo4j** comme base de données de graphes, **Groq's ChatGroq** pour le traitement du langage, et **Hugging Face Embeddings** pour la vectorisation des documents. L'interface permet l'extraction de connaissances, des réponses contextuelles, et une visualisation interactive en 3D des relations entre les entités.

---

## 🚀 **Fonctionnalités**

- **📄 Upload de documents** : Chargez un document PDF pour extraire les entités et leurs relations.
- **📊 Création de graphe de connaissances** : Génère automatiquement un graphe basé sur les entités et relations extraites.
- **🔍 Interface de requêtes** : Posez des questions sur le document pour obtenir une réponse générée et les connexions associées dans le graphe.
- **🌀 Visualisation 3D interactive** : Représentation graphique des relations entre entités à l’aide de **Plotly**.

---

## 🛠️ **Technologies Utilisées**

- **[Streamlit](https://streamlit.io/)** : Pour l’interface utilisateur.
- **[Neo4j](https://neo4j.com/)** : Base de données graphique pour le stockage et la requête des relations.
- **[Groq's ChatGroq](https://www.groq.com/)** : Modèle de langage pour l’extraction de relations et d’entités.
- **[Hugging Face](https://huggingface.co/)** : Vectorisation des documents pour un meilleur alignement sémantique.
- **[Plotly](https://plotly.com/)** : Visualisation en 3D des graphes.
- **[LangChain](https://www.langchain.com/)** : Gestion des documents, opérations RAG et intégration des workflows.

---

## 🖥️ **Installation et Configuration**

### **Prérequis**

- Python 3.7 ou supérieur.
- Une instance **Neo4j** en cours d'exécution.
- Une clé API **Groq** pour le traitement du langage.
- Bibliothèques Python requises :
  - `neo4j`
  - `langchain`
  - `streamlit`
  - `plotly`
  - `networkx`
  - `pyvis`
  - `HuggingFaceEmbeddings`

### **Étapes d'installation**

# Étape 1 : Clonez ce dépôt sur votre machine locale
git clone https://github.com/yourusername/knowledge-graph-rag-system.git
cd knowledge-graph-rag-system

# Étape 2 : Installez les dépendances nécessaires
pip install -r requirements.txt

# Étape 3 : Configurez votre environnement en créant un fichier .env
# Exemple de contenu du fichier .env :
# (Assurez-vous de remplacer les valeurs par celles correspondant à votre configuration)
echo "NEO4J_URI=bolt://localhost:7687
NEO4J_USER=neo4j
NEO4J_PASSWORD=yourpassword
GROQ_API_KEY=your_groq_api_key" > .env

# Étape 4 : Exécutez l'application
streamlit run app.py

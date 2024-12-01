# MongoDB Local Database Setup and Sharing Guide

Dieses Projekt beschreibt, wie eine lokale MongoDB-Datenbank mit Docker eingerichtet und Daten aus einer CSV-Datei importiert werden können. Außerdem wird erklärt, wie die Datenbank exportiert und an andere weitergegeben werden kann.

## Voraussetzungen
- **Docker**: Für die einfache Einrichtung und Portabilität der MongoDB-Umgebung.
- **Python**: Für den Datenimport und die -verarbeitung mit `pandas` und `pymongo`.
- **venv**: Um eine virtuelle Umgebung zu erstellen und die benötigten Abhängigkeiten zu installieren.
- **MongoDB-Tools** (falls Docker nicht verwendet wird): `mongodump` und `mongorestore` für das Exportieren und Importieren.

## 1. Setup der virtuellen Umgebung und Installation der Abhängigkeiten

1. Erstelle eine virtuelle Umgebung:
    ```bash
    python -m venv venv
    ```
2. Aktiviere die virtuelle Umgebung:
    - **Windows**:
      ```bash
      venv\Scripts\activate
      ```
    - **Linux/Mac**:
      ```bash
      source venv/bin/activate
      ```
3. Installiere die Abhängigkeiten aus der `requirements.txt`-Datei:
    ```bash
    pip install -r requirements.txt
    ```

## 2. MongoDB mit Docker starten
1. Lade und installiere [Docker](https://www.docker.com/get-started), falls noch nicht installiert.
2. Starte eine MongoDB-Instanz mit Docker:
    ```bash
    docker run --name mongo -d -p 27017:27017 mongo
    ```

MongoDB läuft nun auf `localhost` und ist über den Standardport `27017` erreichbar.

## 3. CSV-Daten in MongoDB importieren

1. Verwende des Python-Skripts `DB_setup.ipynb`, um CSV-Daten in MongoDB zu importieren.

## Weiterführende Ressourcen
- [MongoDB Documentation](https://docs.mongodb.com/)
- [Docker Documentation](https://docs.docker.com/)

---
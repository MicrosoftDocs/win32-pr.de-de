---
description: Dateibibliothek ersetzt Dokumentordner
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: Dateibibliothek ersetzt Dokumentordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e8d08b176ebf4b5801a73695ea03f60a38eeb5a1ca51e1d90d9119dae5fcaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329670"
---
# <a name="file-library-replaces-document-folder"></a>Dateibibliothek ersetzt Dokumentordner

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen auf Features

**Schweregrad –** Mittel  
**Frequency** – High  











## <a name="description"></a>Beschreibung

Bibliotheken bieten eine zentralisierte ordnerähnliche Benutzeroberfläche für Dateispeicherung, Suche und Zugriff an mehreren Lokalen und Remotestandorten.

Die Standardspeicherorte, die von allgemeinen Dateidialogfeldern verwendet werden (z. B. Öffnen und Speichern), wurden vom Dokumentordner in die Dokumentbibliothek geändert. Die Benutzeroberfläche ist unverändert, aber der Benutzer kann die Bibliothek jetzt mit verschiedenen Anordnungsansichten anzeigen, durchsuchen und durchsuchen. Dateien werden am Standardspeicherort der Bibliothek gespeichert, es sei denn, der Benutzer ändert den Standardspeicherort oder wählt einen anderen Ordner aus.

Entwickler können mithilfe der IShellLibrary-Schnittstelle eigene Bibliotheken erstellen oder vorhandenen Bibliotheken Speicherorte hinzufügen. Benutzer können Bibliotheken mithilfe des Systems "Bekannter Ordner" suchen (z. B. FOLDERID \_ DocumentsLibrary).

## <a name="manifestation-of-impact"></a>Auswirkungen

Die Bibliothek ist selbst eine Datei und kein Ordner. Aus diesem Grund können Pfadmanipulationen fehlerbedingt sein, weil die Anwendung versucht, Dateien mit Dateien zu verketten.

## <a name="solution"></a>Lösung

Wenn Sie IFileDialog verwenden, müssen Sie die GetResult-Methode anstelle der Kombination aus GetFolder und GetFilename verwenden, wie sie in den vorherigen Betriebssystemversionen verwendet wurde. Verwenden Sie nach Möglichkeit die Shell-APIs, um mit Elementen im Shellnamespace (z. B. IShellItem) zu interagieren und diese zu bearbeiten.

## <a name="leveraging-feature-capabilities"></a>Nutzen von Featurefunktionen

Wenn Sie Eigene Bibliotheken erstellen oder vorhandenen Bibliotheken Speicherorte hinzufügen möchten, müssen Sie die IShellLibrary-API verwenden. Bibliotheken sind selbst Shellordner, sodass Sie sie genau wie jeden anderen Shellordner aufzählen können.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests

Mithilfe des allgemeinen Dateidialogfelds wird sichergestellt, dass Benutzer direkt in ihren Bibliotheken speichern können.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   **Windows Bibliotheken:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx
-   **Synchronisierung mit einer Bibliothek:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync

 

 




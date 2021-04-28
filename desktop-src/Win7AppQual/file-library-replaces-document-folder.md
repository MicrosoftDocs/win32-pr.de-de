---
description: Dateibibliothek ersetzt Dokumentordner
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: Dateibibliothek ersetzt Dokumentordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699c645d574012a419f77538bcc58d61a4938120
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088378"
---
# <a name="file-library-replaces-document-folder"></a>Dateibibliothek ersetzt Dokumentordner

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkung von Features

**Schweregrad:** Mittel  
**Häufigkeit** – Hoch  











## <a name="description"></a>BESCHREIBUNG

Bibliotheken bieten eine zentrale ordnerbasierte Begehung für Dateispeicherung, Suche und Zugriff über mehrere Lokale und Remotespeicherorte hinweg.

Die von allgemeinen Dateidialogfeldern verwendeten Standardspeicherorte (z. B. Öffnen und Speichern) wurden vom Dokumentordner in die Dokumentbibliothek geändert. Die Benutzeroberfläche unverändert, aber der Benutzer kann die Bibliothek nun mithilfe verschiedener Anordnungsansichten anzeigen, durchsuchen und durchsuchen. Dateien werden im Standardspeicherort Bibliothek gespeichert, es sei denn, der Benutzer ändert den Standardspeicherort oder wählt einen anderen Ordner aus.

Entwickler können über die IShellLibrary-Schnittstelle eigene Bibliotheken erstellen oder vorhandenen Bibliotheken Speicherorte hinzufügen. Benutzer können Bibliotheken mithilfe des Systems Für bekannte Ordner suchen (z. B. FOLDERID \_ DocumentsLibrary).

## <a name="manifestation-of-impact"></a>Auswirkungen

Die Bibliothek selbst ist eine Datei und kein Ordner. Aus diesem Grund können Pfadbearbeitungen zu Fehlern führen, weil die Anwendung versucht, Dateien mit Dateien zu verketten.

## <a name="solution"></a>Lösung

Bei Verwendung von IFileDialog müssen Sie die GetResult-Methode anstelle der Kombination aus GetFolder und GetFilename verwenden, wie in den vorherigen Betriebssystemversionen. Verwenden Sie nach Möglichkeit die Shell-APIs, um mit Elementen im Shellnamespace (z. B. IShellItem) zu interagieren und diese zu bearbeiten.

## <a name="leveraging-feature-capabilities"></a>Nutzen von Featurefunktionen

Wenn Sie Eigene Bibliotheken erstellen oder vorhandenen Bibliotheken Speicherorte hinzufügen möchten, müssen Sie die IShellLibrary-API verwenden. Bibliotheken sind selbst Shellordner, sodass Sie sie genau wie jeden anderen Shellordner aufzählen können.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests

Mithilfe des allgemeinen Dateidialogfelds wird sichergestellt, dass Benutzer direkt in ihren Bibliotheken speichern können.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   **Windows-Bibliotheken:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx
-   **Synchronisierung mit einer Bibliothek:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync

 

 




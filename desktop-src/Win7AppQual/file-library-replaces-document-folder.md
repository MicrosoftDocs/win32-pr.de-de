---
description: .
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: Datei Bibliothek ersetzt Dokument Ordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15431f5fb5fb5e73dbaf171625a0a6582fa7add2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868140"
---
# <a name="file-library-replaces-document-folder"></a>Datei Bibliothek ersetzt Dokument Ordner

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen von Features

**Schweregrad** -Mittel  
**Häufigkeit** -hoch  











## <a name="description"></a>BESCHREIBUNG

Bibliotheken bieten eine zentralisierte Ordner ähnliche Umgebung für die Speicherung von Dateien, die Suche und den Zugriff über mehrere Standorte hinweg, sowohl lokal als auch Remote.

Die Standard Speicherorte, die von allgemeinen Datei Dialogfeldern (z. b. "Öffnen" und "Speichern") verwendet werden, wurden aus dem Dokument Ordner in die Dokumentbibliothek geändert. Die Benutzeroberfläche ist unverändert, aber der Benutzer kann die Bibliothek nun mithilfe verschiedener Ansichts Ansichten anzeigen, durchsuchen und durchsuchen. Dateien werden im Standard Speicherort der Bibliothek gespeichert, es sei denn, der Benutzer ändert den Standard Speicherort oder wählt einen anderen Ordner aus.

Entwickler können Ihre eigenen Bibliotheken erstellen oder vorhandenen Bibliotheken mithilfe der ishelllibrary-Schnittstelle Speicherorte hinzufügen. Benutzer können Bibliotheken mit dem bekannten Ordnersystem suchen (z. b. folderid \_ documentslibrary).

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

Die Bibliothek ist selbst eine Datei und kein Ordner. Daher können Pfad Manipulationen aufgrund des Versuchs, dass die Anwendung Dateien zu Dateien verkettet, zu Fehlern führen.

## <a name="solution"></a>Lösung

Wenn Sie ifiledialog verwenden, müssen Sie die GetResult-Methode anstelle der Kombination aus "GetFolder" und "GetFileName" verwenden, wie in den vorherigen Betriebssystemversionen. Verwenden Sie nach Möglichkeit die Shell-APIs, um mit Elementen im Shellnamespace (z. b. IShellItem) zu interagieren und diese zu bearbeiten.

## <a name="leveraging-feature-capabilities"></a>Nutzen von Featurefunktionen

Wenn Sie eigene Bibliotheken erstellen oder vorhandenen Bibliotheken Speicherorte hinzufügen möchten, müssen Sie die ishelllibrary-API verwenden. Bibliotheken sind selbst Shellordner, sodass Sie Sie wie alle anderen Shellordner auflisten können.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit

Mithilfe des Dialog Felds "allgemeine Datei" wird sichergestellt, dass Benutzer direkt in ihren Bibliotheken speichern können.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   **Windows-Bibliotheken:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx
-   **Synchronisierung mit einer Bibliothek:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync

 

 




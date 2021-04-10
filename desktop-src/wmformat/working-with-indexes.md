---
title: Arbeiten mit Indizes
description: Arbeiten mit Indizes
ms.assetid: 7daa4b29-0597-462d-ad65-135d0ef7362d
keywords:
- Windows Media-Format-SDK, Indizes
- Advanced Systems Format (ASF), Indizes
- ASF (Advanced Systems Format), Indizes
- Indizes, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34057046223daf2e16950e0e38b1b0db5df32c4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855764"
---
# <a name="working-with-indexes"></a>Arbeiten mit Indizes

Das Windows Media-Format-SDK unterstützt das Suchen und Durchsuchen von Inhalten durch Inhalte. Durchsuchen können Sie einen Speicherort auf der Zeitachse der Datei angeben, um die Wiedergabe zu starten. Mithilfe von Strichs können Sie die Ausgabe einer Datei schnell vorwärts und zurückspulen. Dateien müssen indiziert werden, um diese Features nutzen zu können. Ein Index ist eine Reihe von Werten, die Positionen in der Datei (Präsentations Zeiten, Frame Nummern oder SMTPE-Zeit Codes) mit entsprechenden Offsets im Daten Abschnitt der Datei für jeden darstellen. Die Indizierung ist für Videostreams besonders wichtig, da die Audiodatenstrom-Präsentationszeit leicht geschätzt werden kann. Einige Audiodatenströme erfordern jedoch möglicherweise auch Indizes. Standardmäßig indiziert der Writer alle neuen ASF-Dateien. Wenn Änderungen am Inhalt einer Datei vorgenommen werden, müssen Sie den Index selbst mithilfe des Indexer-Objekts aktualisieren.

Der Indexer unterstützt sowohl eine temporale als auch eine Frame basierte Indizierung sowie die Indizierung auf der Grundlage von SMPTE-Zeit Codes (sofern vorhanden). Der Writer erstellt standardmäßig einen temporalen Index für jeden neuen Videostream, der in einer Datei codiert ist. Der Indexer muss explizit konfiguriert und aufgerufen werden, um einen Frame-oder SMPTE-Zeit Code Index zu erstellen.

Wenn Änderungen am Inhalt einer ASF-Datei vorgenommen werden, muss Sie erneut indiziert werden.

Die folgenden Abschnitte enthalten Beispielcode zum Ausführen allgemeiner Indizierungs Aufgaben.

-   [So deaktivieren Sie die automatische Indizierung](to-disable-automatic-indexing.md)
-   [So konfigurieren Sie den Indexer](to-configure-the-indexer.md)
-   [So indizieren Sie eine ASF-Datei](to-index-an-asf-file.md)
-   [So verhindern Sie die Ausführung der Indizierung](to-stop-indexing-in-progress.md)

Außerdem wird in der Beispielanwendung dscopy die Verwendung des Indexers veranschaulicht. Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).

 

 





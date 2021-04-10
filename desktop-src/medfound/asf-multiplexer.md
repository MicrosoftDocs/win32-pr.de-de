---
description: ASF Multiplexer
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: ASF Multiplexer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362a1e0be72e8bc516e37ec83c36446177816f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041571"
---
# <a name="asf-multiplexer"></a>ASF Multiplexer

Der ASF *Multiplexer* ist ein wmcontainer-Ebenenobjekt, das mit dem [ASF-Datenobjekt](asf-file-structure.md) zusammenarbeitet und einer Anwendung die Möglichkeit bietet, Datenpakete für einen ASF-Container zu generieren. Der Multiplexer akzeptiert Mediendaten in Form von [Medien Beispielen](media-samples.md) und gibt Medien Beispiele basierend auf Streaming-und ASF-Paket Parametern aus, die im [ASF-Header Objekt](asf-file-structure.md)definiert sind. Die Ausgabemedien Beispiele enthalten Verweise auf einen oder mehrere Medien Puffer, die packetisiert Digital Media-Daten enthalten. Sie können dieses Objekt in einem Datei Codierungs Szenario verwenden, in dem es codierte streambeispiele vom Encoder oder für die "ASF-ASF"-Transcodierung (remuxing) empfängt.

Das folgende Diagramm veranschaulicht die Erstellung von ASF-Datenpaketen für eine ASF-Datei mithilfe des Multiplexers.

![Diagramm mit der Erstellung des ASF-Datenpakets](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

Weitere Informationen zur Struktur einer ASF-Datei finden Sie unter [Struktur der ASF-Datei](asf-file-structure.md).

Dieser Abschnitt enthält die folgenden Themen:



| Thema                                                                  | BESCHREIBUNG                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Erstellen des Multiplexer-Objekts](creating-the-multiplexer-object.md) | Erstellen und Initialisieren des Multiplexers.                     |
| [Erstellen neuer ASF-Datenpakete](generating-new-asf-data-packets.md) | Generieren von Datenpaketen, um ein neues ASF-Datenobjekt zu bilden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wmcontainer-ASF-Komponenten](wmcontainer-asf-components.md)
</dt> <dt>

[Tutorial: Kopieren von ASF-Streams aus einer Datei in eine andere](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Tutorial: Schreiben einer WMA-Datei mithilfe der CBR-Codierung](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 




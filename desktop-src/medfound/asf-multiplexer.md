---
description: ASF Multiplexer
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: ASF Multiplexer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e1577f005004dbbe6bbb27e1ce7af346e56e134aff2b3201f5670175b015c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035562"
---
# <a name="asf-multiplexer"></a>ASF Multiplexer

Der *ASF-Multiplexer* ist ein WMContainer-Ebenenobjekt, das mit dem [ASF-Datenobjekt](asf-file-structure.md) funktioniert und einer Anwendung die Möglichkeit gibt, Datenpakete für einen ASF-Container zu generieren. Der Multiplexer akzeptiert Mediendaten in Form von [Medienbeispielen](media-samples.md) und gibt Medienbeispiele basierend auf Streaming- und ASF-Paketparametern aus, die im [ASF-Headerobjekt definiert sind.](asf-file-structure.md) Die Ausgabemedienbeispiele enthalten Verweise auf einen oder mehrere Medienpuffer, die paketierte digitale Mediendaten enthalten. Sie können dieses Objekt in einem Dateicodierungsszenario verwenden, in dem es codierte Streambeispiele vom Encoder oder für die ASF-ASF-Transcodierung (Remuxing) empfängt.

Das folgende Diagramm veranschaulicht die ASF-Datenpaketgenerierung für eine ASF-Datei mit dem Multiplexer.

![Diagramm zur Asf-Datenpaketgenerierung](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

Informationen zur Struktur einer ASF-Datei finden Sie unter [ASF-Dateistruktur.](asf-file-structure.md)

Dieser Abschnitt enthält die folgenden Themen:



| Thema                                                                  | Beschreibung                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Erstellen des Multiplexer-Objekts](creating-the-multiplexer-object.md) | Erstellen und Initialisieren des Multiplexers.                     |
| [Generieren neuer ASF-Datenpakete](generating-new-asf-data-packets.md) | Generieren von Datenpaketen, um ein neues ASF-Datenobjekt zu bilden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMContainer-ASF-Komponenten](wmcontainer-asf-components.md)
</dt> <dt>

[Tutorial: Kopieren von ASF-Streams aus einer Datei in eine andere](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Tutorial: Schreiben einer WMA-Datei mit CBR-Codierung](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 




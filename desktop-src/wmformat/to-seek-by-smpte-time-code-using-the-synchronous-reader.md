---
title: So suchen Sie nach SMPTE-Zeitcode mit dem synchronen Reader
description: So suchen Sie nach SMPTE-Zeitcode mit dem synchronen Reader
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- Advanced Systems Format (ASF), Suchen nach SMPTE-Zeitcodes
- ASF (Advanced Systems Format),Suchen nach SMPTE-Zeitcodes
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- Advanced Systems Format (ASF), SMPTE-Zeitcodes
- ASF (Advanced Systems Format), SMPTE-Zeitcodes
- synchrone Leser, suchen nach SMPTE-Zeitcodes
- synchrone Reader, SMPTE-Zeitcodes
- SMPTE-Zeitcodes, Suchen
- SMPTE-Zeitcodes, synchrone Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b368492d45d3bc564ce0fbb84a6013349c26fcdaca8c1ad576863a9cee6f6f36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196469"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a>So suchen Sie nach SMPTE-Zeitcode mit dem synchronen Reader

Das synchrone Readerobjekt kann basierend auf dem SMPTE-Zeitcode, der einem Videostream zugeordnet ist, nach einem Punkt in einer Datei suchen. Zeitcodedaten werden in [**WMT \_ TIMECODE \_ EXTENSION \_ DATA-Strukturen gekapselt,**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) die videobeispielen als Dateneinheitserweiterungen angefügt sind.

SMPTE-Zeitcodes werden durch einen Bereich und einen Zeitcode innerhalb dieses Bereichs definiert. Ein Bereich ist eine fortlaufende Reihe von Zeitcodes. Jeder Zeitcode wird nach Stunden, Minuten, Sekunden und Frames definiert.

Führen Sie die folgenden Schritte aus, um Daten in einer ASF-Datei mithilfe von SMPTE-Zeitcode mithilfe des synchronen Readers zu suchen.

1.  Legen Sie den Startzeitcode und den Endzeitcode für die Beispielübermittlung fest, indem [**Sie IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe)aufrufen. Sie müssen die Streamnummer eines Videostreams angeben, der nach Zeitcode indiziert ist. Der synchrone Reader synchronisiert die restlichen Ausgaben mit der Präsentationszeit des angegebenen Frames des angegebenen Streams.
2.  Beginnen Sie mit dem Abrufen von Beispielen mit Aufrufen von [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Fahren Sie wie gewohnt mit dem synchronen Reader fort.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[**SMPTE-Zeitcodeunterstützung**](smpte-time-code-support.md)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 





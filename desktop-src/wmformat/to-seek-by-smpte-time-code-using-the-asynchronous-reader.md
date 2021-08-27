---
title: So suchen Sie nach SMPTE-Zeitcode mit dem asynchronen Reader
description: So suchen Sie nach SMPTE-Zeitcode mit dem asynchronen Reader
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- Advanced Systems Format (ASF), Suchen nach SMPTE-Zeitcodes
- ASF (Advanced Systems Format),Suchen nach SMPTE-Zeitcodes
- Advanced Systems Format (ASF), asynchrone Reader
- ASF (Advanced Systems Format), asynchrone Reader
- Advanced Systems Format (ASF), SMPTE-Zeitcodes
- ASF (Advanced Systems Format), SMPTE-Zeitcodes
- asynchrone Reader, Suchen nach SMPTE-Zeitcodes
- asynchrone Reader, SMPTE-Zeitcodes
- SMPTE-Zeitcodes, Suchen
- SMPTE-Zeitcodes, asynchrone Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01ad42170c2458a4dc23a23cfa8102b406f45b6a624cacac28ce31a905ad299
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110120"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a>So suchen Sie nach SMPTE-Zeitcode mit dem asynchronen Reader

Das Readerobjekt kann basierend auf dem einem Videostream zugeordneten SMPTE-Zeitcode zu einem Punkt in einer Datei suchen. Zeitcodedaten werden in [**WMT \_ TIMECODE \_ EXTENSION \_ DATA-Strukturen gekapselt,**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) die videobeispielen als Dateneinheitserweiterungen angefügt sind.

SMPTE-Zeitcodes werden durch einen Bereich und einen Zeitcode innerhalb dieses Bereichs definiert. Ein Bereich ist eine fortlaufende Reihe von Zeitcodes. Jeder Zeitcode wird nach Stunden, Minuten, Sekunden und Frames definiert.

Führen Sie die folgenden Schritte aus, um daten in einer ASF-Datei nach SMPTE-Zeitcode mithilfe des asynchronen Readers zu suchen.

1.  Rufen Sie einen Zeiger auf die [**IWMReaderAdvanced3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) des Readerobjekts ab, indem **Sie IWMReader::QueryInterface** aufrufen.
2.  Legen Sie den Code und die Dauer der Startzeit fest, indem [**Sie IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition)aufrufen. Sie müssen die Streamnummer eines Videostreams angeben, der nach Zeitcode indiziert wird. Der Reader synchronisiert die restlichen Ausgaben mit der Präsentationszeit des angegebenen Frames des angegebenen Streams und beginnt mit der Übermittlung von Ausgabebeispielen.
3.  Verarbeiten Sie die Beispiele wie gewohnt in Ihrer Implementierung der **IWMReaderCallback::OnSample-Methode.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> <dt>

[**SMPTE-Zeitcodeunterstützung**](smpte-time-code-support.md)
</dt> </dl>

 

 





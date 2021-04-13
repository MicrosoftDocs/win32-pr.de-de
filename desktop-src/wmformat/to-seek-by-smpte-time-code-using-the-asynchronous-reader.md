---
title: So suchen Sie nach SMPTE-Zeit Code mithilfe des asynchronen Readers
description: So suchen Sie nach SMPTE-Zeit Code mithilfe des asynchronen Readers
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- Advanced Systems Format (ASF), Suche nach SMPTE-Zeit Codes
- ASF (Advanced Systems Format), Suche nach SMPTE-Zeit Codes
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), SMPTE-Zeit Codes
- ASF (Advanced Systems Format), SMPTE-Zeit Codes
- asynchrone Leser, Suche nach SMPTE-Zeit Codes
- asynchrone Leser, SMPTE-Zeit Codes
- SMPTE-Zeit Codes, suchen
- SMPTE-Zeit Codes, asynchrone Leser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bb90e899db9820ccbd14e42b9699a5f99c7434
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389840"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a>So suchen Sie nach SMPTE-Zeit Code mithilfe des asynchronen Readers

Das Reader-Objekt kann basierend auf dem SMPTE-Zeit Code, der einem Videostream zugeordnet ist, zu einem Punkt in einer Datei suchen. Zeit Code Daten werden in [**WMT-Zeit \_ Code \_ Erweiterungs \_ Daten**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) Strukturen gekapselt, die an Videobeispiele als Dateneinheiten Erweiterungen angefügt werden.

SMPTE-Zeit Codes werden durch einen Bereich und einen Zeit Code in diesem Bereich definiert. Ein Bereich ist eine fortlaufende Reihe von Zeit Codes. Jedes Mal, wenn Code durch Stunden, Minuten, Sekunden und Frames definiert wird.

Führen Sie die folgenden Schritte aus, um mithilfe des asynchronen Readers Daten in einer ASF-Datei nach SMPTE-Zeit Code zu suchen.

1.  Abrufen eines Zeigers auf die [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) -Schnittstelle des Reader-Objekts durch Aufrufen von **iwmreader:: QueryInterface**.
2.  Legen Sie den Start Zeit Code und die Dauer fest, indem Sie [**IWMReaderAdvanced3:: startatposition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition)aufrufen. Sie müssen die streamnummer eines Videodaten Stroms angeben, der nach Zeit Code indiziert wird. Der Reader synchronisiert den Rest der Ausgaben mit der Präsentationszeit des angegebenen Frames des angegebenen Streams und beginnt damit, Ausgabe Beispiele bereitzustellen.
3.  Behandeln Sie die Beispiele wie in der Implementierung der **iwmreadercallback:: onsample** -Methode.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> <dt>

[**SMPTE-Zeit Code Unterstützung**](smpte-time-code-support.md)
</dt> </dl>

 

 





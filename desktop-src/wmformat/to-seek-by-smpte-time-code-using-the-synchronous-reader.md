---
title: So suchen Sie nach SMPTE-Zeit Code mithilfe des synchronen Readers
description: So suchen Sie nach SMPTE-Zeit Code mithilfe des synchronen Readers
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- Advanced Systems Format (ASF), Suche nach SMPTE-Zeit Codes
- ASF (Advanced Systems Format), Suche nach SMPTE-Zeit Codes
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- Advanced Systems Format (ASF), SMPTE-Zeit Codes
- ASF (Advanced Systems Format), SMPTE-Zeit Codes
- synchrone Reader, Suche nach SMPTE-Zeit Codes
- synchrone Reader, SMPTE-Zeit Codes
- SMPTE-Zeit Codes, suchen
- SMPTE-Zeit Codes, synchrone Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c843ba802272d02f1dfc885a3c65b3d124b7423
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314327"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a>So suchen Sie nach SMPTE-Zeit Code mithilfe des synchronen Readers

Das synchrone Reader-Objekt kann basierend auf dem SMPTE-Zeit Code, der einem Videostream zugeordnet ist, zu einem Punkt in einer Datei suchen. Zeit Code Daten werden in [**WMT-Zeit \_ Code \_ Erweiterungs \_ Daten**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) Strukturen gekapselt, die an Videobeispiele als Dateneinheiten Erweiterungen angefügt werden.

SMPTE-Zeit Codes werden durch einen Bereich und einen Zeit Code in diesem Bereich definiert. Ein Bereich ist eine fortlaufende Reihe von Zeit Codes. Jedes Mal, wenn Code durch Stunden, Minuten, Sekunden und Frames definiert wird.

Führen Sie die folgenden Schritte aus, um mithilfe des synchronen Readers Daten in einer ASF-Datei nach SMPTE-Zeit Code zu suchen.

1.  Legen Sie den Start-und Endzeit Code für die Beispiel Übermittlung durch Aufrufen von [**iwmsyncreader:: setrangebyframe**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe)fest. Sie müssen die streamnummer eines Videodaten Stroms angeben, der nach Zeit Code indiziert ist. Der synchrone Reader synchronisiert den Rest der Ausgaben mit der Präsentationszeit des angegebenen Frames des angegebenen Streams.
2.  Beginnen Sie mit dem Abrufen von Beispielen mit Aufrufen von [**iwmsynkreader:: getnextsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Fahren Sie wie gewohnt mit dem synchronen Reader fort.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[**SMPTE-Zeit Code Unterstützung**](smpte-time-code-support.md)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 





---
title: So suchen Sie nach streamnummern und Ausgabe Nummern
description: So suchen Sie nach streamnummern und Ausgabe Nummern
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- Advanced Systems Format (ASF), streamnummern
- ASF (Advanced Systems Format), Erstellen von Zahlen
- Advanced Systems Format (ASF), suchen nach Ausgabe Nummern
- ASF (Advanced Systems Format), suchen nach Ausgabe Nummern
- synchrone Reader, streamnummern
- synchrone Leser, suchen nach Ausgabe Nummern
- Streams, suchen nach Zahlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4bdf10eaeb95f981ab2972ba56ad09b867cd99
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723464"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a>So suchen Sie nach streamnummern und Ausgabe Nummern

Der synchrone Reader unterstützt den vereinfachten Wechsel zwischen Stream und Ausgabe Nummern für die Wiedergabe als der asynchrone Reader. Daher ist es wichtiger, dass Sie in der Lage sein können, zu ermitteln, welche streamnummern mit welchen ausgabezahlen gleich sind.

Um die Ausgabe Nummer zu ermitteln, die einer Datenstrom Nummer entspricht, nennen Sie [**iwmsynkreader:: getoutputnumforstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).

Um die Datenstrom Nummer zu ermitteln, die einer Ausgabe Nummer entspricht, nennen Sie [ **iwmsynkreader:: getstreamnumforoutput** .](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmsynkreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 





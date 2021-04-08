---
title: So suchen Sie nach Zeit mithilfe des synchronen Readers
description: So suchen Sie nach Zeit mithilfe des synchronen Readers
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- Advanced Systems Format (ASF), Suche nach Zeit
- ASF (Advanced Systems Format), Suche nach Zeit
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- synchrone Leser, suchen nach Zeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a43e914a6fc0d320860db61f4747cbee3033e9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723560"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a>So suchen Sie nach Zeit mithilfe des synchronen Readers

Um mithilfe des synchronen Readers nach Daten zu suchen, geben Sie einen Bereich für die Wiedergabe an. Ein Bereich wird durch eine Start Präsentationszeit und eine Dauer, beide in 100-Nanosecond-Einheiten, definiert.

Führen Sie die folgenden Schritte aus, um mithilfe des synchronen Readers mithilfe des synchronen Readers Daten in einer ASF-Datei zu suchen.

1.  Geben Sie eine Startzeit und die Dauer für die Beispiel Übermittlung an, indem Sie [**iwmsyncreader:: abge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange)aufrufen. Diese Methode erfordert nicht, dass Sie eine Datenstrom Nummer angeben, da die Präsentations Zeiten der einzelnen Datenströme bereits synchronisiert sein sollten.
2.  Beginnen Sie mit dem Abrufen von Beispielen mit Aufrufen von [**iwmsynkreader:: getnextsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Fahren Sie wie gewohnt mit dem synchronen Reader fort.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmsynkreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 





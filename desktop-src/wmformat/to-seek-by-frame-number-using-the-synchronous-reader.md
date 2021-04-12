---
title: So suchen Sie nach Frame Nummer mithilfe des synchronen Readers
description: So suchen Sie nach Frame Nummer mithilfe des synchronen Readers
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- Advanced Systems Format (ASF), Suche nach Frame Nummern
- ASF (Advanced Systems Format), Suche nach Frame Nummern
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- synchrone Leser, suchen nach Frame Nummern
- Videostreams, suchen nach Frame Nummern
- Videostreams, synchrone Leser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c26711d2d839e47279e7e52a50f5dc82c6e81da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314267"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a>So suchen Sie nach Frame Nummer mithilfe des synchronen Readers

Zum Suchen nach Daten nach Frame Nummer mithilfe des synchronen Readers geben Sie einen Bereich für die Wiedergabe an. Ein Bereich wird durch eine Start Rahmennummer in einem bestimmten Videostream und eine Anzahl von Frames definiert.

Führen Sie die folgenden Schritte aus, um mithilfe des synchronen Readers Daten in einer ASF-Datei nach Frame Nummer zu suchen.

1.  Legen Sie die Start Frame Nummer und die Anzahl der Frames für die Beispiel Übermittlung durch Aufrufen von [**iwmsyncreader:: setrangebyframe**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe)fest. Sie müssen die streamnummer eines Frame indizierten Videostreams angeben. Der Reader synchronisiert den Rest der Ausgaben mit der Präsentationszeit des angegebenen Frames des angegebenen Streams und beginnt damit, Ausgabe Beispiele bereitzustellen.
2.  Beginnen Sie mit dem Abrufen von Beispielen mit Aufrufen von [**iwmsynkreader:: getnextsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Fahren Sie wie gewohnt mit dem synchronen Reader fort.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmsynkreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 





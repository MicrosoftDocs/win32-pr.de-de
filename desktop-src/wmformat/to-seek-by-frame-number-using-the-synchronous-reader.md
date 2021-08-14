---
title: So suchen Sie nach Framenummer mit dem synchronen Reader
description: So suchen Sie nach Framenummer mit dem synchronen Reader
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- Advanced Systems Format (ASF), suchen nach Framezahlen
- ASF (Advanced Systems Format), Suchen nach Framenummern
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- synchrone Leser, suchen nach Framezahlen
- Videostreams, Suchen nach Framenummern
- Videostreams, synchrone Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b2da615f23e5c1d17046f08310d0aeda49200d5c4ba9fba890d7ba4951e0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699111"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a>So suchen Sie nach Framenummer mit dem synchronen Reader

Um mithilfe des synchronen Readers nach Daten nach Framenummer zu suchen, geben Sie einen Bereich für die Wiedergabe an. Ein Bereich wird durch eine Startrahmennummer in einem bestimmten Videostream und eine Anzahl von Zu spielende Frames definiert.

Führen Sie die folgenden Schritte aus, um Daten in einer ASF-Datei anhand der Framenummer mithilfe des synchronen Readers zu suchen.

1.  Legen Sie durch Aufrufen von [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe)die Startframenummer und die Anzahl der Frames fest, die für die Beispielübermittlung gelesen werden sollen. Sie müssen die Streamnummer eines frameindizierten Videostreams angeben. Der Reader synchronisiert die restlichen Ausgaben mit der Präsentationszeit des angegebenen Frames des angegebenen Streams und beginnt mit der Übermittlung von Ausgabebeispielen.
2.  Beginnen Sie mit dem Abrufen von Beispielen mit Aufrufen von [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Fahren Sie wie gewohnt mit dem synchronen Reader fort.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMSyncReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 





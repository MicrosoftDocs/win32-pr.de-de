---
title: So suchen Sie nach Zeit mit dem synchronen Reader
description: So suchen Sie nach Zeit mit dem synchronen Reader
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- Advanced Systems Format (ASF), suchen nach Zeit
- ASF (Advanced Systems Format), Suchen nach Zeit
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- synchrone Leser, suchen nach Zeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74fb0cb4f73e70821347b82a9e5a2544eb9759e733fb164077b2fc007163db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432633"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a>So suchen Sie nach Zeit mit dem synchronen Reader

Um mit dem synchronen Reader nach Daten zu suchen, geben Sie einen Bereich für die Wiedergabe an. Ein Bereich wird durch eine Startpräsentationszeit und eine Dauer in Einheiten von 100 Nanosekunden definiert.

Führen Sie die folgenden Schritte aus, um Daten in einer ASF-Datei anhand der Präsentationszeit mithilfe des synchronen Readers zu suchen.

1.  Geben Sie eine Startzeit und Dauer für die Beispielübermittlung an, indem [**Sie IWMSyncReader::SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange)aufrufen. Bei dieser Methode müssen Sie keine Streamnummer angeben, da die Präsentationszeiten der einzelnen Datenströme bereits synchronisiert werden sollten.
2.  Beginnen Sie mit dem Abrufen von Beispielen mit Aufrufen von [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Fahren Sie wie gewohnt mit dem synchronen Reader fort.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMSyncReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 





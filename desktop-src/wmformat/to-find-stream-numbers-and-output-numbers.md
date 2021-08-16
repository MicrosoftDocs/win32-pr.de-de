---
title: So suchen Sie Datenstromnummern und Ausgabenummern
description: So suchen Sie Datenstromnummern und Ausgabenummern
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- Advanced Systems Format (ASF), Streamnummern
- ASF (Advanced Systems Format), Erstellen von Zahlen
- Advanced Systems Format (ASF), Suchen von Ausgabenummern
- ASF (Advanced Systems Format), Suchen von Ausgabenummern
- Synchrone Reader, Streamnummern
- Synchrone Reader,Suchen von Ausgabenummern
- Streams, Suchen von Zahlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4349bc98214d61a1529fe4a64dd142a9695d909f9e2a650162a8e4f8ac618177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699588"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a>So suchen Sie Datenstromnummern und Ausgabenummern

Der synchrone Reader unterstützt ein vereinfachtes Wechseln zwischen Stream- und Ausgabenummern für die Wiedergabe als der asynchrone Reader. Daher ist es wichtiger, zu finden, welche Datenstromnummern welchen Ausgabenummern gleichsetzen oder umgekehrt.

Um die Ausgabenummer zu finden, die einer Streamnummer entspricht, rufen [**Sie IWMSyncReader::GetOutputNumberForStream auf.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream)

Um die Streamnummer zu finden, die einer Ausgabenummer entspricht, rufen Sie [ **IWMSyncReader::GetStreamNumberForOutput auf.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMSyncReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 





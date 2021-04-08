---
title: So verhindern Sie die Ausführung der Indizierung
description: So verhindern Sie die Ausführung der Indizierung
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- Windows Media-Format-SDK, die Indizierung wird angehalten
- Advanced Systems Format (ASF), die Indizierung wird angehalten
- ASF (Advanced Systems Format), die Indizierung wird angehalten
- Indizes, die Indizierung wird angehalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea40cbf020182250e0fb982af5b5f84327d5d9a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038578"
---
# <a name="to-stop-indexing-in-progress"></a>So verhindern Sie die Ausführung der Indizierung

Nachdem Sie mit der Indizierung mit einem Aufruf von [**iwmindexer:: startindizierung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing)begonnen haben, wird der Indexer normalerweise so lange fortgesetzt, bis die Datei indiziert ist. Sie können die Indizierungs Vorgänge beenden, indem Sie die [**iwmindexer:: Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) -Methode aufrufen. Nachdem Sie die Indizierung abgebrochen haben, können Sie **startIndex** erneut aufrufen, aber der Indexer beginnt am Anfang der Datei, anstatt von dem Zeitpunkt des Abbruchs fortgesetzt zu werden.

Da **startindizierung** ein asynchroner Rückruf ist, müssen Sie in der Regel **Abbrechen** von einem anderen Thread oder Ereignishandler in der Anwendung aufrufen. In der Regel wird **Abbrechen** von einer Ereignis Prozedur aufgerufen, die einem Schaltflächen-Steuerelement einer Windows-Anwendung zugeordnet ist.

Wenn die Indizierung abgebrochen wird, übergibt der Indexer eine Statusmeldung von WMT \_ geschlossen, so als ob die Datei ordnungsgemäß indiziert wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmindexer-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 





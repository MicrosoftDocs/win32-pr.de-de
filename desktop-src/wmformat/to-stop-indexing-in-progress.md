---
title: So beenden Sie die Indizierung in Bearbeitung
description: So beenden Sie die Indizierung in Bearbeitung
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- Windows Medienformat-SDK, Indizierung wird beendet
- Advanced Systems Format (ASF), Indizierung wird beendet
- ASF (Advanced Systems Format), Indizierung wird beendet
- Indizes,Indizierung wird beendet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d441e42bc3c7033e776d353cf64fc5938183a4f8d720f086b4fb5fd9828be02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432623"
---
# <a name="to-stop-indexing-in-progress"></a>So beenden Sie die Indizierung in Bearbeitung

Nachdem Sie mit dem Indizieren mit einem Aufruf von [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing)begonnen haben, wird der Indexer normalerweise fortgesetzt, bis die Datei indiziert ist. Sie können Indizierungsvorgänge beenden, indem Sie die [**IWMIndexer::Cancel-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) aufrufen. Nachdem Sie die Indizierung abgebrochen haben, können Sie **StartIndexing** erneut aufrufen, aber der Indexer beginnt am Anfang der Datei, anstatt ab dem Punkt des Abbruchs fortsetzen zu müssen.

Da **StartIndexing ein** asynchroner Aufruf ist, müssen Sie normalerweise **Cancel** von einem anderen Thread oder Ereignishandler in Ihrer Anwendung aufrufen. In der **Regel wird Abbrechen** von einer Ereignisprozedur aufgerufen, die einem Schaltflächen-Steuerelement einer Windows zugeordnet ist.

Wenn die Indizierung abgebrochen wird, übersendet der Indexer die Statusmeldung WMT CLOSED, als wäre die Datei \_ ordnungsgemäß indiziert worden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMIndexer-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 





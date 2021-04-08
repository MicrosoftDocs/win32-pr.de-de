---
title: Kontexte bearbeiten
description: Kontexte bearbeiten
ms.assetid: cf8bbe66-d2ad-49b3-9e7c-246e4ca50149
keywords:
- Text Dienste-Framework (TSF), Bearbeiten von Kontexten
- TSF (Text Dienst Framework), Kontexte bearbeiten
- Text Dienste, Kontexte bearbeiten
- TSF-aktivierte Anwendungen, Kontexte bearbeiten
- Kontexte bearbeiten
- Text Dienste-Framework (TSF), Cookies bearbeiten
- TSF (Text Dienste-Framework), Cookies bearbeiten
- Text Dienste, Cookies bearbeiten
- TSF-aktivierte Anwendungen, Cookies bearbeiten
- Cookies bearbeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020ca8713d66d9d14e387381fc21157db8bdedf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855943"
---
# <a name="edit-contexts"></a>Kontexte bearbeiten

## <a name="applications"></a>Anwendungen

Um einen Bearbeitungs Kontext zu erstellen, ruft eine Anwendung [ITfDocumentMgr:: kreatecontext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)auf.

## <a name="text-services"></a>Text Dienste

Ein Text Dienst verwendet häufig den aktuell aktiven Bearbeitungs Kontext. Der derzeit aktive Bearbeitungs Kontext ist der Bearbeitungs Kontext am oberen Rand des Stapels des aktiven Dokument-Managers. Um den derzeit aktiven Kontext abzurufen, Ruft ein Text Dienst [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) auf, um den aktiven Dokument-Manager abzurufen. Anschließend wird [ITfDocumentMgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) aufgerufen, um den Bearbeitungs Kontext am oberen Rand des Stapels abzurufen.

In einigen Fällen erfordert ein Text Dienst einen eigenen Bearbeitungs Kontext. Um einen Bearbeitungs Kontext zu erstellen, Ruft ein Text Dienst **ITfDocumentMgr:: kreatecontext** auf.

## <a name="edit-cookies"></a>Cookies bearbeiten

Viele Methoden, wie z. b. [itfrange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), erfordern eine Möglichkeit, einen Bearbeitungs Kontext zu identifizieren, der über eine schreibgeschützte oder Lese-/Schreib-Dokumentsperre verfügt. [](document-locks.md) Eine Dokument Sperre wird durch eine Aushandlung zwischen dem TSF-Manager und der Anwendung abgerufen. Ein Text Dienst kann diese Aushandlung nicht direkt ausführen. Ein Text Dienst kann nur dann eine Sperre abrufen, indem er eine [Bearbeitungs Sitzung](edit-sessions.md) mit einem bestimmten Kontext und Lese-oder Lese-/Schreibzugriff anfordert. Wenn die Bearbeitungs Sitzung erteilt wird, wird der Text Dienst mit einem *Bearbeitungs Cookie* bereitgestellt, das den Bearbeitungs Kontext mit dem angeforderten Zugriff identifiziert. Dieses Cookie wird dann an die-Methode weitergegeben, um den Bearbeitungs Kontext mit dem richtigen Zugriff zu identifizieren.

**ITfDocumentMgr:: kreatecontext** stellt dem Kontext Ersteller außerdem ein Bearbeitungs Cookie zur Verfügung. Dieses Cookie hat schreibgeschützten Zugriff, und es gibt keine Möglichkeit, die Zugriffsebene zu ändern. In Wahrheit aushandelt der TSF-Manager keine Dokument Sperre für dieses Bearbeitungs Cookie. Das Cookie ist intern als schreibgeschützt gekennzeichnet, aber das Dokument ist eigentlich nicht gesperrt. Wenn der Kontext Ersteller z. b. [ITfContext:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) mit dem Bearbeitungs Cookie aufruft, das von **ITfDocumentMgr:: featecontext** zurückgegeben wird, führt dies dazu, dass die Anwendung [ITextStoreACP:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) oder [itextstoreanchor:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) aufgerufen wird. Vor dem Abrufen der Auswahl wird von der Anwendung bestimmt, ob eine Dokument Sperre vorhanden ist. Da keine Sperre vorhanden ist, kann die Anwendung mit TS \_ E \_ NOLOCK nicht ausgeführt werden. Das heißt, wenn eine Anwendung mit diesem Cookie eine Methode aufruft, die dazu führt, dass eine der aufrufenden Text Speichermethoden der Anwendung aufgerufen wird, muss dieser Fall intern behandelt werden, da die Anwendung nicht tatsächlich über eine Dokument Sperre verfügt.

Wenn für den Kontext Ersteller ein Bearbeitungs Cookie mit Lese-/Schreibzugriff erforderlich ist, muss eine eigene Bearbeitungs Sitzung eingerichtet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[ITF documentmgr:: kreatecontext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[ITF documentmgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[Itfrange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[Dokument Sperren](document-locks.md)
</dt> <dt>

[Bearbeitungssitzungen](edit-sessions.md)
</dt> <dt>

[ITF context:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[Itextstoreanchor:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 





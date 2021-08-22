---
title: Asynchrone und synchrone Bindung
description: Asynchrone und synchrone Bindung
ms.assetid: 9852df19-5ae4-4425-9ce0-cac160d68456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb498d083260db087e9f32cd3f24b67f03f9a788c0add2592dde36fe7a7905e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048858"
---
# <a name="asynchronous-and-synchronous-binding"></a>Asynchrone und synchrone Bindung

Der Client kann überprüfen, ob der Moniker asynchron ist, indem er die [**IsAsyncMoniker-Funktion**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) aufruft. Wenn der Client das BINDF ASYNCHRONOUS-Flag zurückgibt, anstatt einen Objektzeiger oder einen Speicherzeiger aus nachfolgenden Aufrufen von \_ [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) oder [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)zurückgibt, gibt der Moniker MK S ASYNCHRONOUS anstelle des Objektzeigers und NULL anstelle des Speicherzeigers \_ \_ zurück.  Als Antwort sollte der Client während der Implementierung von [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) und [**IBindStatusCallBack::OnObjectAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775063(v=vs.85))auf den Empfang des angeforderten Objekts oder Speichers warten.

Das Rückrufobjekt empfängt auch eine Statusbenachrichtigung über [**IBindStatusCallback::OnProgress,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85))eine Datenverfügbarkeitsbenachrichtigung über [**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))und verschiedene andere Benachrichtigungen vom Moniker über den Status des Bindungsvorgang.

Wenn der Client das BINDF ASYNCHRONOUS-Flag nicht aus dem Aufruf von \_ [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))des Monikers zurück gibt, wird der Bindungsvorgang synchron fortgesetzt, und das gewünschte Objekt oder der gewünschte Speicher wird von nachfolgenden Aufrufen von [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) oder [**BindToStorage zurückgegeben.**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) Wenn der Client einen synchronen Vorgang möchte und keine Statusbenachrichtigungen oder Rückrufe empfangen möchte, kann er einen asynchronen Moniker anfordern, um sich synchron zu verhalten, indem [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85))nicht implementieren. In solchen Fällen verhält sich der asynchrone Moniker wie ein synchroner Standardmoniker.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Moniker](asynchronous-monikers.md)
</dt> </dl>

 

 
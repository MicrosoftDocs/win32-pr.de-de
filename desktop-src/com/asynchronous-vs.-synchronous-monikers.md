---
title: Asynchrone und synchrone Moniker
description: Asynchrone und synchrone Moniker
ms.assetid: 79c7894d-956a-4c86-8806-2c6c7faa6034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c631c669d73796d1596f52ab2ec6e724829ea80e6873523c1e9bd4f8ad567f09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071108"
---
# <a name="asynchronous-and-synchronous-monikers"></a>Asynchrone und synchrone Moniker

Ein Client eines synchronen STANDARD-OLE-Monikers erstellt und enthält in der Regel einen Verweis auf den Moniker sowie den Bindungskontext, der während der Bindung verwendet werden soll. Die Komponenten, die an der Verwendung herkömmlicher Moniker beteiligt sind, sind im folgenden Diagramm dargestellt.

![Diagramm, das den Client zeigt, der entweder mit dem Bindungskontext oder einem beliebigen Moniker für das vom System bereitgestellte Verbunden ist.](images/1b29d6fe-f6e7-4eec-91e7-5043c09ca4dc.png)

Clients erstellen in der Regel Standardmoniker durch Aufrufen von Funktionen wie [**CreateFileMoniker,**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker)oder [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) oder , da sie im persistenten Speicher gespeichert werden können, über [**OleSaveToStream**](/windows/desktop/api/ole/nf-ole-olesavetostream) und [**OleLoadFromStream**](/windows/desktop/api/ole/nf-ole-oleloadfromstream). Moniker können auch aus einem Containerobjekt durch Aufrufen der [**IBindHost::CreateMoniker-Methode erhalten**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) werden. Clients erstellen Bindungskontexte, indem sie die [**CreateBindCtx-Funktion**](/windows/desktop/api/Objbase/nf-objbase-createbindctx) aufrufen und dann den Bindungskontext mit Aufrufen von [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) oder [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)an den Moniker übergeben.

Wie im folgenden Diagramm gezeigt, erstellt und enthält ein Client eines asynchronen Monikers auch einen Verweis auf den Moniker und bindungskontext, der während der Bindung verwendet werden soll.

![Diagramm, das die Verbindungen zwischen vom Client bereitgestellten, vom Schütz bereitgestellten und vom System bereitgestellten Verbindungen zeigt.](images/86872be9-bcbb-4ce8-b69a-38ae5bd7ba41.png)

Um asynchrones Verhalten zu erhalten, implementiert der Client die [**IBindStatusCallback-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) für ein bind-status-callback-Objekt und ruft entweder die [**RegisterBindStatusCallback-Funktion**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) oder die [**CreateAsyncBindCtx-Funktion**](/windows/desktop/api/Urlmon/nf-urlmon-createasyncbindctx) auf, um diese Schnittstelle beim Bindungskontext zu registrieren. Der Moniker übergibt einen Zeiger auf seine [**IBinding-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) in einem Aufruf der [**IBindStatusCallback::OnStartBinding-Methode.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)) Der Client teilt dem asynchronen Moniker mit, wie er beim Zurückgeben vom Aufruf der [**IBindStatusCallback::GetBindInfo-Methode des Monikers gebunden werden**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)) soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Moniker](asynchronous-monikers.md)
</dt> </dl>

 

 
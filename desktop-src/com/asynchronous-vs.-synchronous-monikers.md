---
title: Asynchrone und synchrone Moniker
description: Asynchrone und synchrone Moniker
ms.assetid: 79c7894d-956a-4c86-8806-2c6c7faa6034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d54ee1b5f31941774944463baad893058fd15ad
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104571571"
---
# <a name="asynchronous-and-synchronous-monikers"></a>Asynchrone und synchrone Moniker

Ein Client eines standardmäßigen synchronen OLE-Monikers erstellt und enthält in der Regel einen Verweis auf den Moniker sowie den Bindungs Kontext, der während der Bindung verwendet werden soll. Die Komponenten, die bei der Verwendung herkömmlicher Moniker beteiligt sind, werden im folgenden Diagramm dargestellt.

![Diagramm, das den Client anzeigt, der entweder mit dem Bindungs Kontext oder einem beliebigen Moniker für das vom System bereitgestellte verbunden ist.](images/1b29d6fe-f6e7-4eec-91e7-5043c09ca4dc.png)

Clients erstellen standardmoniker in der Regel durch Aufrufen von Funktionen wie z. b. [**createfilemoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker), [**createitemmoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker)oder [**createpointermoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) oder, da Sie über [**olesavetostream**](/windows/desktop/api/ole/nf-ole-olesavetostream) und [**oleloadfromstream**](/windows/desktop/api/ole/nf-ole-oleloadfromstream)im persistenten Speicher gespeichert werden können. Moniker können auch aus einem Container Objekt abgerufen werden, indem die [**ibindhost:: createmoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) -Methode aufgerufen wird. Clients erstellen Bindungs Kontexte, indem Sie die [**createbindctx**](/windows/desktop/api/Objbase/nf-objbase-createbindctx) -Funktion aufrufen und dann den Bindungs Kontext mit Aufrufen an [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) oder [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)an den Moniker übergeben.

Wie im folgenden Diagramm gezeigt, erstellt ein Client eines asynchronen Monikers auch einen Verweis auf den Moniker und den Bindungs Kontext, der während der Bindung verwendet werden soll.

![Diagramm, das die Verbindungen zwischen vom Client bereitgestellten, von Monker bereitgestellten und vom System bereitgestellten anzeigt.](images/86872be9-bcbb-4ce8-b69a-38ae5bd7ba41.png)

Um asynchrones Verhalten zu erhalten, implementiert der Client die [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) -Schnittstelle für ein BIND-Status-Callback-Objekt und ruft entweder die [**registerbindstatuscallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) -Funktion oder die Funktion "" in der Funktion "" von "" die Funktion "" der Funktion " [**roateasyncbindctx**](/windows/desktop/api/Urlmon/nf-urlmon-createasyncbindctx) Der Moniker übergibt einen Zeiger an seine [**ibinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) -Schnittstelle in einem Aufruf der [**ibindstatuencallback:: onstartbinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)) -Methode. Der Client teilt dem asynchronen Moniker mit, wie er an die Rückgabe des Monikers-Aufrufs an die [**ibindstatuencallback:: getbindinfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)) -Methode gebunden werden will.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Moniker](asynchronous-monikers.md)
</dt> </dl>

 

 
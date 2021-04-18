---
title: Rückruf Synchronisierung
description: Rückruf Synchronisierung
ms.assetid: e8268f18-49e7-4e09-9006-77858b734bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c274c35a6df176f65c505f2a3fecc9a53a20e5d9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106338087"
---
# <a name="callback-synchronization"></a><span data-ttu-id="b649b-103">Rückruf Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="b649b-103">Callback Synchronization</span></span>

<span data-ttu-id="b649b-104">Die asynchrone [WinInet-API](/windows/desktop/WinInet/portal) (die für die am häufigsten verwendeten Protokolle verwendet wird) lässt die Synchronisierung des Rückrufmechanismus und der aufrufenden Anwendung als Übung für den Client zu.</span><span class="sxs-lookup"><span data-stu-id="b649b-104">The asynchronous [WinInet API](/windows/desktop/WinInet/portal) (used for the most common protocols) leaves the synchronization of the callback mechanism and the calling application as an exercise for the client.</span></span> <span data-ttu-id="b649b-105">Dies ist beabsichtigt, da Sie das größte Maß an Flexibilität ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b649b-105">This is intentional because it allows the greatest degree of flexibility.</span></span> <span data-ttu-id="b649b-106">Die Standardprotokolle und die URL-monikerimplementierung führen diese Synchronisierung durch und garantieren, dass Single Thread-und Apartment Thread-Anwendungen niemals mit Konflikten im freien Thread arbeiten müssen.</span><span class="sxs-lookup"><span data-stu-id="b649b-106">The default protocols and the URL moniker implementation perform this synchronization and guarantee that single-threaded and apartment-threaded applications never have to deal with free-thread-style contention.</span></span> <span data-ttu-id="b649b-107">Das heißt, dass die [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) -und [**ibindstatuuscallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) -Schnittstellen des Clients nur in ihren richtigen Threads aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b649b-107">That is, the client's [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) and [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) interfaces are called only on their proper threads.</span></span> <span data-ttu-id="b649b-108">Diese Funktion ist für den Benutzer des URL-mmonikers so lange transparent, dass jeder Thread, der [**IMoniker:: bindesstorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) und [**IMoniker:: bindesobject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) aufruft, über eine Nachrichten Warteschlange verfügt.</span><span class="sxs-lookup"><span data-stu-id="b649b-108">This feature is transparent to the user of the URL mMoniker as long each thread that calls [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) and [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) has a message queue.</span></span>

<span data-ttu-id="b649b-109">Die asynchrone monikerspezifikation erfordert eine präzisere Steuerung der Priorisierung und Verwaltung von Downloads, als von entweder von Winsock oder WinInet zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="b649b-109">The asynchronous moniker specification requires more precise control over the prioritization and management of downloads than is allowed for by either WinSock or WinInet.</span></span> <span data-ttu-id="b649b-110">Dementsprechend verwaltet ein URL-Moniker alle Downloads für jeden beliebigen Thread des Aufrufers, wobei (als Teil der Synchronisierung) ein Prioritäts Schema basierend auf der [**ibinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) -Spezifikation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b649b-110">Accordingly, a URL moniker manages all the downloads for any given caller's thread, using (as part of its synchronization) a priority scheme based on the [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) specification.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b649b-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b649b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b649b-112">URL-Moniker</span><span class="sxs-lookup"><span data-stu-id="b649b-112">URL Monikers</span></span>](url-monikers.md)
</dt> </dl>

 

 
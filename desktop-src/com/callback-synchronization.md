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
# <a name="callback-synchronization"></a>Rückruf Synchronisierung

Die asynchrone [WinInet-API](/windows/desktop/WinInet/portal) (die für die am häufigsten verwendeten Protokolle verwendet wird) lässt die Synchronisierung des Rückrufmechanismus und der aufrufenden Anwendung als Übung für den Client zu. Dies ist beabsichtigt, da Sie das größte Maß an Flexibilität ermöglicht. Die Standardprotokolle und die URL-monikerimplementierung führen diese Synchronisierung durch und garantieren, dass Single Thread-und Apartment Thread-Anwendungen niemals mit Konflikten im freien Thread arbeiten müssen. Das heißt, dass die [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) -und [**ibindstatuuscallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) -Schnittstellen des Clients nur in ihren richtigen Threads aufgerufen werden. Diese Funktion ist für den Benutzer des URL-mmonikers so lange transparent, dass jeder Thread, der [**IMoniker:: bindesstorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) und [**IMoniker:: bindesobject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) aufruft, über eine Nachrichten Warteschlange verfügt.

Die asynchrone monikerspezifikation erfordert eine präzisere Steuerung der Priorisierung und Verwaltung von Downloads, als von entweder von Winsock oder WinInet zugelassen wird. Dementsprechend verwaltet ein URL-Moniker alle Downloads für jeden beliebigen Thread des Aufrufers, wobei (als Teil der Synchronisierung) ein Prioritäts Schema basierend auf der [**ibinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) -Spezifikation verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[URL-Moniker](url-monikers.md)
</dt> </dl>

 

 
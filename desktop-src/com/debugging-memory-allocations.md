---
title: Debugging von Speicher Belegungen
description: Debugging von Speicher Belegungen
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb6a7dbe313cfe571fa6b4d244df35407fa331e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316526"
---
# <a name="debugging-memory-allocations"></a><span data-ttu-id="6cb3a-103">Debugging von Speicher Belegungen</span><span class="sxs-lookup"><span data-stu-id="6cb3a-103">Debugging Memory Allocations</span></span>

<span data-ttu-id="6cb3a-104">COM stellt die [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) -Schnittstelle bereit, die Entwickler zum Debuggen Ihrer Speicher Belegungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-104">COM provides the [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) interface for developers to use to debug their memory allocations.</span></span> <span data-ttu-id="6cb3a-105">Für jede Methode in [**imzuzuordc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc)gibt es zwei Methoden in **imzuordcspy**, eine "Pre"-Methode und eine "Post"-Methode.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-105">For each method in [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc), there are two methods in **IMallocSpy**, a "pre" method and a "post" method.</span></span> <span data-ttu-id="6cb3a-106">Nachdem ein Entwickler es implementiert und im System veröffentlicht hat, ruft das System die **IMallocSpy** -Methode "Pre" direkt vor der entsprechenden **IMalloc** -Methode auf, sodass der Debugcode für die Zuordnungs Operation "Spy" und die Post-Methode aufgerufen wird, um den Spy freizugeben.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-106">After a developer implements it and publishes it to the system, the system calls the **IMallocSpy** "pre" method just before the corresponding **IMalloc** method, effectively allowing the debug code to "spy" on the allocation operation, and calls the "post" method to release the spy.</span></span>

<span data-ttu-id="6cb3a-107">Wenn com z. b. erkennt, dass der nächste Aufruf ein Aufruf von [**imzuzuordc:: zuordc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc)ist, wird [**imzuzuordcspy::P rezuzuzuweisung**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc)aufgerufen. dabei werden die Debugvorgänge ausgeführt, die der Entwickler bei der **Zuord:P** **nungsausführung** wünscht [](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc)</span><span class="sxs-lookup"><span data-stu-id="6cb3a-107">For example, when COM detects that the next call is a call to [**IMalloc::Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), it calls [**IMallocSpy::PreAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), executing whatever debug operations the developer wants during the **Alloc** execution, and then, when the **Alloc** call returns, calls [**IMallocSpy::PostAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) to release the spy and return control to the code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cb3a-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6cb3a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cb3a-109">Verwalten der Speicher Belegung</span><span class="sxs-lookup"><span data-stu-id="6cb3a-109">Managing Memory Allocation</span></span>](managing-memory-allocation.md)
</dt> </dl>

 

 
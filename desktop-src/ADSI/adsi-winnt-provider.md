---
title: ADSI WinNT-Anbieter
description: Der Microsoft ADSI-Anbieter implementiert eine Reihe von ADSI-Objekten, um verschiedene ADSI-Schnittstellen zu unterstützen.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- ADSI-WinNT-Anbieter ADSI
- WinNT-Dienstanbieter ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9748e17185417eb382281774c31554cb983742
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387966"
---
# <a name="adsi-winnt-provider"></a><span data-ttu-id="af56d-105">ADSI WinNT-Anbieter</span><span class="sxs-lookup"><span data-stu-id="af56d-105">ADSI WinNT Provider</span></span>

<span data-ttu-id="af56d-106">Der Microsoft ADSI-Anbieter implementiert eine Reihe von ADSI-Objekten, um verschiedene ADSI-Schnittstellen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="af56d-106">The Microsoft ADSI provider implements a set of ADSI objects to support various ADSI interfaces.</span></span> <span data-ttu-id="af56d-107">Der Namespace Name für den Windows-Anbieter ist "Winnt", und dieser Anbieter wird häufig als WinNT-Anbieter bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="af56d-107">The namespace name for the Windows provider is "WinNT" and this provider is commonly referred to as the WinNT provider.</span></span> <span data-ttu-id="af56d-108">Um auf den WinNT-Anbieter zuzugreifen, binden Sie mithilfe von [Winnt ADsPath](winnt-adspath.md)an eines der [ADSI-Objekte von Winnt](adsi-objects-of-winnt.md).</span><span class="sxs-lookup"><span data-stu-id="af56d-108">To access the WinNT provider, bind to any of the [ADSI objects of WinNT](adsi-objects-of-winnt.md), using the [WinNT AdsPath](winnt-adspath.md).</span></span>

<span data-ttu-id="af56d-109">Der WinNT-Anbieter ist in der ADSI-Systemkomponente für Windows und Windows Server enthalten.</span><span class="sxs-lookup"><span data-stu-id="af56d-109">The WinNT provider is included in the ADSI system component for Windows and Windows Server.</span></span>

> [!Note]  
> <span data-ttu-id="af56d-110">Der standardmäßige WinNT-Anbieter kann nicht als vollständig Thread sicher angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="af56d-110">The default WinNT provider cannot be assumed to be completely thread-safe.</span></span> <span data-ttu-id="af56d-111">Writer von Multithreadanwendungen sollten Multithreading verarbeiten, um den Zugriff zwischen Threads durch die ordnungsgemäße Verwendung von Synchronisierungs Objekten, wie Semaphore, Mutexen, kritischen Abschnitten usw., ordnungsgemäß zu koordinieren.</span><span class="sxs-lookup"><span data-stu-id="af56d-111">Writers of multithreaded applications should handle multithreading to properly coordinate any access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

 

 





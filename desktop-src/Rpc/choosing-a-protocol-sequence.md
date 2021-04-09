---
title: Auswählen einer Protokoll Sequenz
description: Zu den bewährten Methoden für die Auswahl einer Protokoll Sequenz gehört die Verwendung von ncacn \_ IP \_ TCP und Ncalrpc, nicht ncacn \_ NP, ncacn \_ SPX und ncadg \_ \.
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3dea44868b96361ccaddc6e339f94fde92704f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039523"
---
# <a name="choosing-a-protocol-sequence"></a><span data-ttu-id="c3e3a-103">Auswählen einer Protokoll Sequenz</span><span class="sxs-lookup"><span data-stu-id="c3e3a-103">Choosing a Protocol Sequence</span></span>

<span data-ttu-id="c3e3a-104">**Bewährte Methoden:** Verwenden Sie [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) beim Ausführen eines Remote Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="c3e3a-104">**Best practice:** Use [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) when making a remote call.</span></span> <span data-ttu-id="c3e3a-105">Verwenden Sie [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) für lokale Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="c3e3a-105">Use [**ncalrpc**](/windows/desktop/Midl/ncalrpc) for local calls.</span></span> <span data-ttu-id="c3e3a-106">Verwenden Sie nicht [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), [**ncacn \_ SPX**](/windows/desktop/Midl/ncacn-spx)oder eine der **ncadg \_ \*** -Protokoll Sequenzen, Sie sind weniger effizient und verfügen über untergeordnete Funktionen.</span><span class="sxs-lookup"><span data-stu-id="c3e3a-106">Do not use [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), [**ncacn\_spx**](/windows/desktop/Midl/ncacn-spx), or any of the **ncadg\_\*** protocol sequences; they are less efficient and have inferior capabilities.</span></span>

 

 
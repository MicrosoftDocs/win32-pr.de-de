---
description: Status „Wird angehalten“
ms.assetid: 945e1b1a-2557-4be2-bfdb-bb11ac7c3fe8
title: Status „Wird angehalten“
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07f6f610c3cfac9361e1db40c0fcd37b90645b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125012"
---
# <a name="pausing"></a><span data-ttu-id="5d9c4-103">Status „Wird angehalten“</span><span class="sxs-lookup"><span data-stu-id="5d9c4-103">Pausing</span></span>

<span data-ttu-id="5d9c4-104">Alle Filter Zustandsänderungen müssen die Filter Sperre enthalten.</span><span class="sxs-lookup"><span data-stu-id="5d9c4-104">All filter state changes must hold the filter lock.</span></span> <span data-ttu-id="5d9c4-105">Erstellen Sie in der **Pause** -Methode alle Ressourcen, die der Filter benötigt:</span><span class="sxs-lookup"><span data-stu-id="5d9c4-105">In the **Pause** method, create any resources the filter needs:</span></span>


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



<span data-ttu-id="5d9c4-106">Die [**cbasefilter::P ause**](cbasefilter-pause.md) -Methode legt den korrekten Zustand für den Filter fest (Zustand \_ angehalten) und ruft die [**cbasepin:: Active**](cbasepin-active.md) -Methode für jede verbundene PIN im Filter auf.</span><span class="sxs-lookup"><span data-stu-id="5d9c4-106">The [**CBaseFilter::Pause**](cbasefilter-pause.md) method sets the correct state on the filter (State\_Paused) and calls the [**CBasePin::Active**](cbasepin-active.md) method on every connected pin in the filter.</span></span> <span data-ttu-id="5d9c4-107">Die **aktive** Methode teilt der PIN mit, dass der Filter aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="5d9c4-107">The **Active** method informs the pin that the filter has become active.</span></span> <span data-ttu-id="5d9c4-108">Wenn die PIN Ressourcen erstellt, überschreiben Sie die **aktive** Methode wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5d9c4-108">If the pin creates resources, override the **Active** method, as follows:</span></span>


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 




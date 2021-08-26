---
description: Status „Wird angehalten“
ms.assetid: 945e1b1a-2557-4be2-bfdb-bb11ac7c3fe8
title: Status „Wird angehalten“
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f113bdaa41709055202886112d678c2a1fbb172d99e880ceaafc997817412a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997280"
---
# <a name="pausing"></a>Status „Wird angehalten“

Alle Filterzustandsänderungen müssen die Filtersperre enthalten. Erstellen Sie in der **Pause-Methode** alle Ressourcen, die der Filter benötigt:


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



Die [**CBaseFilter::P ause-Methode**](cbasefilter-pause.md) legt den richtigen Zustand für den Filter fest (State \_ Paused) und ruft die [**CBasePin::Active-Methode**](cbasepin-active.md) für jeden verbundenen Pin im Filter auf. Die **Active-Methode** informiert den Pin darüber, dass der Filter aktiv geworden ist. Wenn der Pin Ressourcen erstellt, überschreiben Sie die **Active-Methode** wie folgt:


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 




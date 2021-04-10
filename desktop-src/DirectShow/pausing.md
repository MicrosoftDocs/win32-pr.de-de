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
# <a name="pausing"></a>Status „Wird angehalten“

Alle Filter Zustandsänderungen müssen die Filter Sperre enthalten. Erstellen Sie in der **Pause** -Methode alle Ressourcen, die der Filter benötigt:


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



Die [**cbasefilter::P ause**](cbasefilter-pause.md) -Methode legt den korrekten Zustand für den Filter fest (Zustand \_ angehalten) und ruft die [**cbasepin:: Active**](cbasepin-active.md) -Methode für jede verbundene PIN im Filter auf. Die **aktive** Methode teilt der PIN mit, dass der Filter aktiv ist. Wenn die PIN Ressourcen erstellt, überschreiben Sie die **aktive** Methode wie folgt:


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 




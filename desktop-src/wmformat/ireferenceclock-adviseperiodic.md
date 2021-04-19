---
title: IReferenceClock-Methode
description: Diese Methode ist nicht implementiert.
ms.assetid: b34ef914-992e-4ce2-943b-8bc36687a88a
keywords:
- Adviin periodische Methode Windows Media-Format
- Adviin periodische Methode Windows Media-Format, IReferenceClock-Schnittstelle
- IReferenceClock-Schnittstelle Windows Media-Format, adviin periodische Methode
topic_type:
- apiref
api_name:
- IReferenceClock.AdvisePeriodic
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65b4020c42430d10e48125fa7d5f1481e7f0ee7c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106342325"
---
# <a name="ireferenceclockadviseperiodic-method"></a><span data-ttu-id="d5948-106">IReferenceClock:: advisperiodische-Methode</span><span class="sxs-lookup"><span data-stu-id="d5948-106">IReferenceClock::AdvisePeriodic method</span></span>

<span data-ttu-id="d5948-107">Diese Methode ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d5948-107">This method is not implemented.</span></span>

<span data-ttu-id="d5948-108">In anderen Implementierungen der **IReferenceClock** -Schnittstelle, wie z. b. in der DirectShow-® Komponente von Microsoft® DirectX®, wird die **adviseperiodische** -Methode verwendet, um eine regelmäßige anforderungsanforderung zu erstellen, die jedes Mal, wenn das angegebene Zeitintervall abläuft, das angegebene Ereignis Objekt signalisiert.</span><span class="sxs-lookup"><span data-stu-id="d5948-108">In other implementations of the **IReferenceClock** interface, such as in the DirectShow® component of Microsoft® DirectX®, the **AdvisePeriodic** method is used to create a periodic advise request that would signal the specified event object each time the specified time interval elapses.</span></span> <span data-ttu-id="d5948-109">Dieses SDK implementiert die Funktionalität dieser Methode nicht, und alle Aufrufe, die an dieses SDK durchgeführt werden, führen zu einem Rückgabewert von E \_ notimpl.</span><span class="sxs-lookup"><span data-stu-id="d5948-109">This SDK does not implement the functionality of this method, and any calls made to it will result in a return value of E\_NOTIMPL.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5948-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5948-110">Syntax</span></span>


```C++
 AdvisePeriodic();
```



## <a name="parameters"></a><span data-ttu-id="d5948-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5948-111">Parameters</span></span>

<span data-ttu-id="d5948-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d5948-112">This method has no parameters.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5948-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5948-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5948-114">**IReferenceClock-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d5948-114">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





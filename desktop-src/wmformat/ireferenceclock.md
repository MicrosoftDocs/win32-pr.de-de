---
title: IReferenceClock-Schnittstelle
description: Die IReferenceClock-Schnittstelle ermöglicht den Zugriff auf eine externe Uhr. Diese Schnittstelle wird bereitgestellt, um zu ermöglichen, dass alle renderingroutinen mit derselben Uhr synchronisiert werden. Diese Schnittstelle kann von einem Reader-Objekt abgerufen werden.
ms.assetid: 1424fd74-d56c-4338-801f-319ef975169f
keywords:
- IReferenceClock-Schnittstelle Windows Media-Format
- IReferenceClock-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IReferenceClock
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72d17ef362aa5436fe98443d86dff5ae31212650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338262"
---
# <a name="ireferenceclock-interface"></a><span data-ttu-id="d57b1-106">IReferenceClock-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d57b1-106">IReferenceClock interface</span></span>

<span data-ttu-id="d57b1-107">Die **IReferenceClock** -Schnittstelle ermöglicht den Zugriff auf eine externe Uhr.</span><span class="sxs-lookup"><span data-stu-id="d57b1-107">The **IReferenceClock** interface provides access to an external clock.</span></span> <span data-ttu-id="d57b1-108">Diese Schnittstelle wird bereitgestellt, um zu ermöglichen, dass alle renderingroutinen mit derselben Uhr synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d57b1-108">This interface is provided to enable all rendering routines to be synchronized to the same clock.</span></span>

<span data-ttu-id="d57b1-109">Diese Schnittstelle kann von einem Reader-Objekt abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d57b1-109">This interface can be obtained from a reader object.</span></span>

## <a name="members"></a><span data-ttu-id="d57b1-110">Member</span><span class="sxs-lookup"><span data-stu-id="d57b1-110">Members</span></span>

<span data-ttu-id="d57b1-111">Die **IReferenceClock** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d57b1-111">The **IReferenceClock** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d57b1-112">**IReferenceClock** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d57b1-112">**IReferenceClock** also has these types of members:</span></span>

-   [<span data-ttu-id="d57b1-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="d57b1-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d57b1-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="d57b1-114">Methods</span></span>

<span data-ttu-id="d57b1-115">Die **IReferenceClock** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d57b1-115">The **IReferenceClock** interface has these methods.</span></span>



| <span data-ttu-id="d57b1-116">Methode</span><span class="sxs-lookup"><span data-stu-id="d57b1-116">Method</span></span>                                                   | <span data-ttu-id="d57b1-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d57b1-117">Description</span></span>                                                               |
|:---------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="d57b1-118">**Empfehlungen regelmäßig**</span><span class="sxs-lookup"><span data-stu-id="d57b1-118">**AdvisePeriodic**</span></span>](ireferenceclock-adviseperiodic.md) | <span data-ttu-id="d57b1-119">Wird von diesem SDK nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d57b1-119">Not implemented by this SDK.</span></span><br/>                                   |
| [<span data-ttu-id="d57b1-120">**Empfehlungen**</span><span class="sxs-lookup"><span data-stu-id="d57b1-120">**AdviseTime**</span></span>](ireferenceclock-advisetime.md)         | <span data-ttu-id="d57b1-121">Fordert eine asynchrone Benachrichtigung an, dass eine Zeit abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="d57b1-121">Requests an asynchronous notification that a time has elapsed.</span></span><br/> |
| [<span data-ttu-id="d57b1-122">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="d57b1-122">**GetTime**</span></span>](ireferenceclock-gettime.md)               | <span data-ttu-id="d57b1-123">Ruft den aktuellen Verweis Zeitpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="d57b1-123">Retrieves the current reference time.</span></span><br/>                          |
| [<span data-ttu-id="d57b1-124">**Unadvise**</span><span class="sxs-lookup"><span data-stu-id="d57b1-124">**Unadvise**</span></span>](ireferenceclock-unadvise.md)             | <span data-ttu-id="d57b1-125">Bricht eine Benachrichtigungs Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="d57b1-125">Cancels a notification request.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="d57b1-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d57b1-126">Remarks</span></span>

<span data-ttu-id="d57b1-127">Informationen zu anderen Schnittstellen, die mithilfe der QueryInterface-Methode dieser Schnittstelle abgerufen werden können, finden Sie unter Reader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d57b1-127">For information on other interfaces that can be obtained by using the QueryInterface method of this interface, see Reader Object.</span></span>

## <a name="see-also"></a><span data-ttu-id="d57b1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d57b1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57b1-129">**Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="d57b1-129">**Interfaces**</span></span>](interfaces.md)
</dt> </dl>

 


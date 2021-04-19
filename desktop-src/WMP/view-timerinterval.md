---
title: View. TimerInterval
description: Das TimerInterval-Attribut gibt das Intervall (in Millisekunden) an, in dem der Timer Ereignisse für den OnTimer-Ereignishandler auslöst, oder ruft es ab.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- Ansicht. TimerInterval-Fenster Media Player
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790c95fbb2cded134222271d04c4c37dae412b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352860"
---
# <a name="viewtimerinterval"></a><span data-ttu-id="bfe35-104">View. TimerInterval</span><span class="sxs-lookup"><span data-stu-id="bfe35-104">VIEW.timerInterval</span></span>

<span data-ttu-id="bfe35-105">Das **TimerInterval** -Attribut gibt das Intervall (in Millisekunden) an, in dem der Timer Ereignisse für den **OnTimer** -Ereignishandler auslöst, oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="bfe35-105">The **timerInterval** attribute specifies or retrieves the interval, in milliseconds, at which the timer fires events to the **ontimer** event handler.</span></span>

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a><span data-ttu-id="bfe35-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="bfe35-106">Possible Values</span></span>

<span data-ttu-id="bfe35-107">Dieses Attribut ist eine Lese-/schreibzahl (**Long**) mit einem Standardwert von 1000. </span><span class="sxs-lookup"><span data-stu-id="bfe35-107">This attribute is a read/write **Number** (**long**) with a default value of 1000.</span></span>



| <span data-ttu-id="bfe35-108">Wert</span><span class="sxs-lookup"><span data-stu-id="bfe35-108">Value</span></span>        | <span data-ttu-id="bfe35-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bfe35-109">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="bfe35-110">0</span><span class="sxs-lookup"><span data-stu-id="bfe35-110">0</span></span>            | <span data-ttu-id="bfe35-111">Das Timer-Ereignis wird nicht ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="bfe35-111">The timer event does not fire.</span></span> |
| <span data-ttu-id="bfe35-112">50 und höher</span><span class="sxs-lookup"><span data-stu-id="bfe35-112">50 and above</span></span> | <span data-ttu-id="bfe35-113">Das Intervall in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="bfe35-113">The interval in milliseconds.</span></span>  |



 

<span data-ttu-id="bfe35-114">Jeder Wert unter 50 (einschließlich negativer Zahlen, aber nicht einschließlich 0) generiert einen Fehler, und der vorherige Wert wird beibehalten.</span><span class="sxs-lookup"><span data-stu-id="bfe35-114">Any value below 50 (including negative numbers, but not including zero) generates an error and the previous value is maintained.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfe35-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfe35-115">Remarks</span></span>

<span data-ttu-id="bfe35-116">Dies wird nicht automatisch ausgelöst, wenn kein **OnTimer** -Ereignishandler implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="bfe35-116">This will not fire automatically if no **ontimer** event handler is implemented.</span></span> <span data-ttu-id="bfe35-117">Folglich gibt es keine Leistungsminderung, obwohl der Standardwert ungleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="bfe35-117">Thus there is no performance degradation even though the default value is nonzero.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfe35-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfe35-118">Requirements</span></span>



| <span data-ttu-id="bfe35-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfe35-119">Requirement</span></span> | <span data-ttu-id="bfe35-120">Wert</span><span class="sxs-lookup"><span data-stu-id="bfe35-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="bfe35-121">Version</span><span class="sxs-lookup"><span data-stu-id="bfe35-121">Version</span></span><br/> | <span data-ttu-id="bfe35-122">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="bfe35-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bfe35-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfe35-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfe35-124">**View-Element**</span><span class="sxs-lookup"><span data-stu-id="bfe35-124">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="bfe35-125">**View. OnTimer**</span><span class="sxs-lookup"><span data-stu-id="bfe35-125">**VIEW.ontimer**</span></span>](view-ontimer.md)
</dt> </dl>

 

 






---
description: Tritt auf, wenn der Cursor den physischen Erkennungsbereich (Nähe) des Tablet-Kontexts verlässt.
ms.assetid: a3a570ed-570b-4579-b120-ed5457630bc2
title: InkCollector. Cursor Event Event (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e2d6ee30a60c260d861cdc5c24e22d7b4b43b0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348379"
---
# <a name="inkcollectorcursoroutofrange-event"></a><span data-ttu-id="02e49-103">InkCollector. Cursor Event-Ereignis</span><span class="sxs-lookup"><span data-stu-id="02e49-103">InkCollector.CursorOutOfRange event</span></span>

<span data-ttu-id="02e49-104">Tritt auf, wenn der Cursor den physischen Erkennungsbereich (Nähe) des Tablet-Kontexts verlässt.</span><span class="sxs-lookup"><span data-stu-id="02e49-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="02e49-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02e49-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="02e49-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02e49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02e49-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02e49-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02e49-108">Das [**iinkcursor-Schnittstellen**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Objekt, das das **cursoroutfrange** -Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="02e49-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorOutOfRange** event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02e49-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02e49-109">Return value</span></span>

<span data-ttu-id="02e49-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="02e49-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02e49-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02e49-111">Remarks</span></span>

<span data-ttu-id="02e49-112">Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icecursoroutofrange definiert.</span><span class="sxs-lookup"><span data-stu-id="02e49-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="02e49-113">Das Ereignis " **Cursor** Ereignis" wird auch dann ausgelöst, wenn Sie sich im Modus "auswählen" oder "Löschen" befinden, nicht nur im frei Hand Modus.</span><span class="sxs-lookup"><span data-stu-id="02e49-113">The **CursorOutOfRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="02e49-114">Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie für die Festlegung verantwortlich sind) und den Modus beachten, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="02e49-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="02e49-115">Der Vorteil dieser Anforderung ist, dass die Innovationen auf der Plattform durch ein höheres Bewusstsein für Platt Form Ereignisse verstärkt werden.</span><span class="sxs-lookup"><span data-stu-id="02e49-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e49-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02e49-116">Requirements</span></span>



| <span data-ttu-id="02e49-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02e49-117">Requirement</span></span> | <span data-ttu-id="02e49-118">Wert</span><span class="sxs-lookup"><span data-stu-id="02e49-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e49-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02e49-119">Minimum supported client</span></span><br/> | <span data-ttu-id="02e49-120">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02e49-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="02e49-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02e49-121">Minimum supported server</span></span><br/> | <span data-ttu-id="02e49-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="02e49-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="02e49-123">Header</span><span class="sxs-lookup"><span data-stu-id="02e49-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="02e49-124"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="02e49-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="02e49-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="02e49-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="02e49-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02e49-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="02e49-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02e49-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e49-128">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="02e49-128">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="02e49-129">**Cursor Event Range-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="02e49-129">**CursorInRange Event**</span></span>](inkcollector-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="02e49-130">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="02e49-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 





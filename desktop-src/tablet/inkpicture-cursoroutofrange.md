---
description: 'InkPicture.CursorOutOfRange-Ereignis: Tritt auf, wenn der Cursor den physischen Erkennungsbereich (Nähe) des Tablet-Kontexts verlässt.'
ms.assetid: 0c71a4ad-3c09-4134-b0e7-82f29e8913ed
title: InkPicture.CursorOutOfRange-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d80584eafb7f1e5222316507f08bd73efb12fae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086568"
---
# <a name="inkpicturecursoroutofrange-event"></a><span data-ttu-id="100f0-103">InkPicture.CursorOutOfRange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="100f0-103">InkPicture.CursorOutOfRange event</span></span>

<span data-ttu-id="100f0-104">Tritt ein, wenn der Cursor den physischen Erkennungsbereich (Nähe) des Tablet-Kontexts verlässt.</span><span class="sxs-lookup"><span data-stu-id="100f0-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="100f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="100f0-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="100f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="100f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="100f0-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="100f0-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="100f0-108">Das [**IInkCursor-Schnittstellenobjekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **CursorOutOfRange-Ereignis generiert** hat.</span><span class="sxs-lookup"><span data-stu-id="100f0-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorOutOfRange** event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="100f0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="100f0-109">Return value</span></span>

<span data-ttu-id="100f0-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="100f0-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="100f0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="100f0-111">Remarks</span></span>

<span data-ttu-id="100f0-112">Diese Ereignismethode wird in den Dispatch-Schnittstellen **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ ICECursorOutOfRange definiert.</span><span class="sxs-lookup"><span data-stu-id="100f0-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="100f0-113">Das **CursorOutOfRange-Ereignis** wird auch dann ausgelöst, wenn es sich im Auswahl- oder Löschmodus befindet, nicht nur im Ink-Modus.</span><span class="sxs-lookup"><span data-stu-id="100f0-113">The **CursorOutOfRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="100f0-114">Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="100f0-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="100f0-115">Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein größeres Bewusstsein für Plattformereignisse.</span><span class="sxs-lookup"><span data-stu-id="100f0-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="100f0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="100f0-116">Requirements</span></span>



| <span data-ttu-id="100f0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="100f0-117">Requirement</span></span> | <span data-ttu-id="100f0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="100f0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="100f0-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="100f0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="100f0-120">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="100f0-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="100f0-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="100f0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="100f0-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="100f0-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="100f0-123">Header</span><span class="sxs-lookup"><span data-stu-id="100f0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="100f0-124"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="100f0-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="100f0-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="100f0-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="100f0-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="100f0-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="100f0-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="100f0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="100f0-128">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="100f0-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="100f0-129">**CursorInRange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="100f0-129">**CursorInRange Event**</span></span>](inkpicture-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="100f0-130">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="100f0-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 





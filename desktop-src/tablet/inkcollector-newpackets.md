---
description: 'InkCollector.NewPackets-Ereignis: Tritt auf, wenn der Ink-Collector ein Paket empfängt.'
ms.assetid: 2682e7ba-dabd-497e-aea4-6d3f837f4f10
title: InkCollector.NewPackets-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bab9d13dd2f33689700ef4a9aee2ed5059403e8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110118"
---
# <a name="inkcollectornewpackets-event"></a><span data-ttu-id="7ca39-103">InkCollector.NewPackets-Ereignis</span><span class="sxs-lookup"><span data-stu-id="7ca39-103">InkCollector.NewPackets event</span></span>

<span data-ttu-id="7ca39-104">Tritt ein, wenn der Ink-Collector ein Paket empfängt.</span><span class="sxs-lookup"><span data-stu-id="7ca39-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ca39-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ca39-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="7ca39-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ca39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ca39-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7ca39-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca39-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**NewInAirPackets-Ereignis**](inkcollector-newinairpackets.md) generiert hat.</span><span class="sxs-lookup"><span data-stu-id="7ca39-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="7ca39-109">*Strich* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7ca39-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca39-110">Gibt das [**IInkStrokeDisp-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) an.</span><span class="sxs-lookup"><span data-stu-id="7ca39-110">Specifies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="7ca39-111">*PacketCount* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7ca39-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca39-112">Die Anzahl der empfangenen Pakete für ein [**IInkStrokeDisp-Objekt.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)</span><span class="sxs-lookup"><span data-stu-id="7ca39-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="7ca39-113">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7ca39-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca39-114">Diese Methode gibt ein Array zurück, das die ausgewählten Daten für das Paket enthält.</span><span class="sxs-lookup"><span data-stu-id="7ca39-114">When this method returns, contains an array that contains the selected data for the packet.</span></span>

<span data-ttu-id="7ca39-115">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek.](using-the-com-library.md)</span><span class="sxs-lookup"><span data-stu-id="7ca39-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ca39-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ca39-116">Return value</span></span>

<span data-ttu-id="7ca39-117">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7ca39-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ca39-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ca39-118">Remarks</span></span>

<span data-ttu-id="7ca39-119">Pakete werden empfangen, während ein Strich erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="7ca39-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="7ca39-120">Paketereignisse treten schnell auf, und ein **NewPackets-Ereignishandler** muss schnell sein oder die Leistung beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="7ca39-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="7ca39-121">Die TThis-Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICENewPackets definiert.</span><span class="sxs-lookup"><span data-stu-id="7ca39-121">TThis event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="7ca39-122">Dieses Ereignis sollte sorgfältig verwendet werden, da es negative Auswirkungen auf die Ink-Leistung haben kann, wenn zu viel Code in den Ereignishandlern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ca39-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="7ca39-123">Verwenden Sie die [**DesiredPacketDescription-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) des Ink-Collectorobjekts, um festzulegen, welche Eigenschaften in diesem Array enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7ca39-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="7ca39-124">Das Array, das der *PacketData-Parameter* zurückgibt, enthält die Daten für diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7ca39-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="7ca39-125">Obwohl Sie die Paketdaten ändern können, werden diese Änderungen nicht beibehalten oder verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ca39-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ca39-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ca39-126">Requirements</span></span>



| <span data-ttu-id="7ca39-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ca39-127">Requirement</span></span> | <span data-ttu-id="7ca39-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7ca39-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca39-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ca39-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7ca39-130">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7ca39-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7ca39-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ca39-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7ca39-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7ca39-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7ca39-133">Header</span><span class="sxs-lookup"><span data-stu-id="7ca39-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ca39-134"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="7ca39-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7ca39-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7ca39-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ca39-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ca39-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7ca39-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7ca39-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca39-138">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7ca39-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="7ca39-139">**NewInAirPackets-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="7ca39-139">**NewInAirPackets Event**</span></span>](inkcollector-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="7ca39-140">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7ca39-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="7ca39-141">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7ca39-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 





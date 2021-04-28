---
description: 'InkPicture.NewPackets-Ereignis: Tritt auf, wenn der Ink-Collector ein Paket empfängt.'
ms.assetid: 7d120198-c016-4452-b8a8-22c4ad87d526
title: InkPicture.NewPackets-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194fb9bffae07cca561fbfc11ff8a185d63bb9e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086478"
---
# <a name="inkpicturenewpackets-event"></a><span data-ttu-id="c541e-103">InkPicture.NewPackets-Ereignis</span><span class="sxs-lookup"><span data-stu-id="c541e-103">InkPicture.NewPackets event</span></span>

<span data-ttu-id="c541e-104">Tritt ein, wenn der Ink-Collector ein Paket empfängt.</span><span class="sxs-lookup"><span data-stu-id="c541e-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="c541e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c541e-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="c541e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c541e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c541e-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c541e-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c541e-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**NewInAirPackets-Ereignis**](inkpicture-newinairpackets.md) generiert hat.</span><span class="sxs-lookup"><span data-stu-id="c541e-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkpicture-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="c541e-109">*Strich* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c541e-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c541e-110">Das [**IInkStrokeDisp-Objekt.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)</span><span class="sxs-lookup"><span data-stu-id="c541e-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="c541e-111">*PacketCount* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c541e-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c541e-112">Die Anzahl der empfangenen Pakete für ein [**IInkStrokeDisp-Objekt.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)</span><span class="sxs-lookup"><span data-stu-id="c541e-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="c541e-113">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c541e-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c541e-114">Ein Array, das die ausgewählten Daten für das Paket enthält.</span><span class="sxs-lookup"><span data-stu-id="c541e-114">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="c541e-115">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek.](using-the-com-library.md)</span><span class="sxs-lookup"><span data-stu-id="c541e-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c541e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c541e-116">Return value</span></span>

<span data-ttu-id="c541e-117">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c541e-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c541e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c541e-118">Remarks</span></span>

<span data-ttu-id="c541e-119">Pakete werden empfangen, während ein Strich erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="c541e-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="c541e-120">Paketereignisse treten schnell auf, und ein **NewPackets-Ereignishandler** muss schnell sein oder die Leistung beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="c541e-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="c541e-121">Diese Ereignismethode wird in den Dispatch-Only-Schnittstellen **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ ICENewPackets definiert.</span><span class="sxs-lookup"><span data-stu-id="c541e-121">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="c541e-122">Dieses Ereignis sollte sorgfältig verwendet werden, da es negative Auswirkungen auf die Ink-Leistung haben kann, wenn zu viel Code in den Ereignishandlern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c541e-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="c541e-123">Verwenden Sie die [**DesiredPacketDescription-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) des Ink-Collectorobjekts, um festzulegen, welche Eigenschaften in diesem Array enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c541e-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="c541e-124">Das Array, das der *PacketData-Parameter* zurückgibt, enthält die Daten für diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c541e-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="c541e-125">Obwohl Sie die Paketdaten ändern können, werden diese Änderungen nicht beibehalten oder verwendet.</span><span class="sxs-lookup"><span data-stu-id="c541e-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c541e-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c541e-126">Requirements</span></span>



| <span data-ttu-id="c541e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c541e-127">Requirement</span></span> | <span data-ttu-id="c541e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c541e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c541e-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c541e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c541e-130">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c541e-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c541e-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c541e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c541e-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c541e-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c541e-133">Header</span><span class="sxs-lookup"><span data-stu-id="c541e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c541e-134"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="c541e-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c541e-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c541e-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="c541e-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c541e-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c541e-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c541e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c541e-138">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="c541e-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="c541e-139">**NewInAirPackets-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="c541e-139">**NewInAirPackets Event**</span></span>](inkpicture-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="c541e-140">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c541e-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="c541e-141">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c541e-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 





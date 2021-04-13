---
description: Tritt auf, wenn der Ink Collector ein Paket empfängt.
ms.assetid: 2682e7ba-dabd-497e-aea4-6d3f837f4f10
title: InkCollector. newcollector-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b03e1a561a61c9b291bca8e59f990dc12b4e2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342809"
---
# <a name="inkcollectornewpackets-event"></a><span data-ttu-id="08493-103">InkCollector. newcollector-Ereignis</span><span class="sxs-lookup"><span data-stu-id="08493-103">InkCollector.NewPackets event</span></span>

<span data-ttu-id="08493-104">Tritt auf, wenn der Ink Collector ein Paket empfängt.</span><span class="sxs-lookup"><span data-stu-id="08493-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="08493-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="08493-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="08493-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08493-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08493-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08493-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08493-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das Ereignis " [**nwinairpakete**](inkcollector-newinairpackets.md) " generiert hat.</span><span class="sxs-lookup"><span data-stu-id="08493-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="08493-109">*Strich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08493-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08493-110">Gibt das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="08493-110">Specifies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="08493-111">*PacketCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08493-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08493-112">Die Anzahl der für ein [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt empfangenen Pakete.</span><span class="sxs-lookup"><span data-stu-id="08493-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="08493-113">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="08493-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="08493-114">Wenn diese Methode zurückgegeben wird, enthält Sie ein Array, das die ausgewählten Daten für das Paket enthält.</span><span class="sxs-lookup"><span data-stu-id="08493-114">When this method returns, contains an array that contains the selected data for the packet.</span></span>

<span data-ttu-id="08493-115">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="08493-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08493-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08493-116">Return value</span></span>

<span data-ttu-id="08493-117">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="08493-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08493-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08493-118">Remarks</span></span>

<span data-ttu-id="08493-119">Pakete werden empfangen, während ein Strich erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="08493-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="08493-120">Paket Ereignisse treten schnell auf, und ein **newpacket** -Ereignishandler muss schnell sein, oder die Leistung ist beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="08493-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="08493-121">TDiese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen iinkcollectorevents, iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ icenewpakete definiert.</span><span class="sxs-lookup"><span data-stu-id="08493-121">TThis event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="08493-122">Dieses Ereignis sollte sorgfältig verwendet werden, da es eine negative Auswirkung auf die Handschrift Leistung haben kann, wenn zu viel Code in den Ereignis Handlern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08493-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="08493-123">Verwenden Sie die [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) -Eigenschaft des Ink Collector-Objekts, um festzulegen, welche Eigenschaften in diesem Array enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="08493-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="08493-124">Das Array, das der *packetData* -Parameter zurückgibt, enthält die Daten für diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08493-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="08493-125">Obwohl Sie die Paketdaten ändern können, werden diese Änderungen nicht beibehalten oder verwendet.</span><span class="sxs-lookup"><span data-stu-id="08493-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="08493-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08493-126">Requirements</span></span>



| <span data-ttu-id="08493-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08493-127">Requirement</span></span> | <span data-ttu-id="08493-128">Wert</span><span class="sxs-lookup"><span data-stu-id="08493-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08493-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08493-129">Minimum supported client</span></span><br/> | <span data-ttu-id="08493-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08493-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="08493-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08493-131">Minimum supported server</span></span><br/> | <span data-ttu-id="08493-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="08493-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="08493-133">Header</span><span class="sxs-lookup"><span data-stu-id="08493-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="08493-134"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="08493-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="08493-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="08493-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="08493-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08493-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="08493-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08493-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08493-138">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="08493-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="08493-139">**"Nwinairpakete"-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="08493-139">**NewInAirPackets Event**</span></span>](inkcollector-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="08493-140">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="08493-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="08493-141">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="08493-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 





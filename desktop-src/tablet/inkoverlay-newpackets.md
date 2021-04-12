---
description: Tritt auf, wenn der frei Hand Collecto ein Paket empfängt.
ms.assetid: 26d5a3eb-430a-4e21-8a3f-fdec5005cd6e
title: InkOverlay. newpakets-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43743b47d007b44d4f2460266e7198266c36afd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218049"
---
# <a name="inkoverlaynewpackets-event"></a><span data-ttu-id="c4f3e-103">InkOverlay. newpackt-Ereignis</span><span class="sxs-lookup"><span data-stu-id="c4f3e-103">InkOverlay.NewPackets event</span></span>

<span data-ttu-id="c4f3e-104">Tritt auf, wenn das frei Hand Collecto-Paket ein Paket empfängt.</span><span class="sxs-lookup"><span data-stu-id="c4f3e-104">Occurs when the ink collecto rreceives a packet</span></span>

## <a name="syntax"></a><span data-ttu-id="c4f3e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4f3e-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="c4f3e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4f3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4f3e-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4f3e-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4f3e-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das Ereignis " [**nwinairpakete**](inkcollector-newinairpackets.md) " generiert hat.</span><span class="sxs-lookup"><span data-stu-id="c4f3e-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="c4f3e-109">*Strich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4f3e-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4f3e-110">Gibt das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c4f3e-110">Specifies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="c4f3e-111">*PacketCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4f3e-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4f3e-112">Die Anzahl der für ein [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt empfangenen Pakete.</span><span class="sxs-lookup"><span data-stu-id="c4f3e-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="c4f3e-113">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c4f3e-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4f3e-114">Ein Array, das die ausgewählten Daten für das Paket enthält.</span><span class="sxs-lookup"><span data-stu-id="c4f3e-114">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="c4f3e-115">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="c4f3e-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4f3e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4f3e-116">Return value</span></span>

<span data-ttu-id="c4f3e-117">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c4f3e-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4f3e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4f3e-118">Remarks</span></span>

<span data-ttu-id="c4f3e-119">Pakete werden empfangen, während ein Strich erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="c4f3e-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="c4f3e-120">Paket Ereignisse treten schnell auf, und ein [**newpacket**](inkcollector-newpackets.md) -Ereignishandler muss schnell sein, oder die Leistung ist beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="c4f3e-120">Packet events occur rapidly, and a [**NewPackets**](inkcollector-newpackets.md) event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="c4f3e-121">Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icenewpakete definiert.</span><span class="sxs-lookup"><span data-stu-id="c4f3e-121">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="c4f3e-122">Dieses Ereignis sollte sorgfältig verwendet werden, da es eine negative Auswirkung auf die Handschrift Leistung haben kann, wenn zu viel Code in den Ereignis Handlern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4f3e-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="c4f3e-123">Verwenden Sie die [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) -Eigenschaft des Ink Collector-Objekts, um festzulegen, welche Eigenschaften in diesem Array enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c4f3e-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="c4f3e-124">Das Array, das der *packetData* -Parameter zurückgibt, enthält die Daten für diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c4f3e-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="c4f3e-125">Obwohl Sie die Paketdaten ändern können, werden diese Änderungen nicht beibehalten oder verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4f3e-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c4f3e-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4f3e-126">Requirements</span></span>



| <span data-ttu-id="c4f3e-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4f3e-127">Requirement</span></span> | <span data-ttu-id="c4f3e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c4f3e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4f3e-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4f3e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c4f3e-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4f3e-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c4f3e-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4f3e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c4f3e-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c4f3e-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c4f3e-133">Header</span><span class="sxs-lookup"><span data-stu-id="c4f3e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4f3e-134"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c4f3e-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c4f3e-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c4f3e-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4f3e-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4f3e-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c4f3e-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4f3e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4f3e-138">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c4f3e-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="c4f3e-139">**"Nwinairpakete"-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="c4f3e-139">**NewInAirPackets Event**</span></span>](inkcollector-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="c4f3e-140">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c4f3e-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="c4f3e-141">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c4f3e-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 





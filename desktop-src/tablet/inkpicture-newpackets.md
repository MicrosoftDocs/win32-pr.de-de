---
description: Tritt auf, wenn der Ink Collector ein Paket empfängt.
ms.assetid: 7d120198-c016-4452-b8a8-22c4ad87d526
title: InkPicture. newpackt-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0b3e1df0df2ba051150550daa60772e2a068df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368010"
---
# <a name="inkpicturenewpackets-event"></a><span data-ttu-id="a1c82-103">InkPicture. newpackt-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a1c82-103">InkPicture.NewPackets event</span></span>

<span data-ttu-id="a1c82-104">Tritt auf, wenn der Ink Collector ein Paket empfängt.</span><span class="sxs-lookup"><span data-stu-id="a1c82-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1c82-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1c82-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="a1c82-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1c82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1c82-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1c82-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1c82-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das Ereignis " [**nwinairpakete**](inkpicture-newinairpackets.md) " generiert hat.</span><span class="sxs-lookup"><span data-stu-id="a1c82-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkpicture-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-109">*Strich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1c82-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1c82-110">Das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a1c82-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-111">*PacketCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1c82-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1c82-112">Die Anzahl der für ein [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt empfangenen Pakete.</span><span class="sxs-lookup"><span data-stu-id="a1c82-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-113">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a1c82-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1c82-114">Ein Array, das die ausgewählten Daten für das Paket enthält.</span><span class="sxs-lookup"><span data-stu-id="a1c82-114">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="a1c82-115">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="a1c82-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1c82-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1c82-116">Return value</span></span>

<span data-ttu-id="a1c82-117">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a1c82-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1c82-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1c82-118">Remarks</span></span>

<span data-ttu-id="a1c82-119">Pakete werden empfangen, während ein Strich erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="a1c82-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="a1c82-120">Paket Ereignisse treten schnell auf, und ein **newpacket** -Ereignishandler muss schnell sein, oder die Leistung ist beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="a1c82-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="a1c82-121">Diese Ereignismethode wird in den Schnittstellen **\_ iinkcollectorevents**, **\_ iinkoverlayevents** und **\_ iinkpictureevents** Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icenewpakete definiert.</span><span class="sxs-lookup"><span data-stu-id="a1c82-121">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="a1c82-122">Dieses Ereignis sollte sorgfältig verwendet werden, da es eine negative Auswirkung auf die Handschrift Leistung haben kann, wenn zu viel Code in den Ereignis Handlern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1c82-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="a1c82-123">Verwenden Sie die [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) -Eigenschaft des Ink Collector-Objekts, um festzulegen, welche Eigenschaften in diesem Array enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a1c82-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="a1c82-124">Das Array, das der *packetData* -Parameter zurückgibt, enthält die Daten für diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1c82-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="a1c82-125">Obwohl Sie die Paketdaten ändern können, werden diese Änderungen nicht beibehalten oder verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1c82-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a1c82-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1c82-126">Requirements</span></span>



| <span data-ttu-id="a1c82-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1c82-127">Requirement</span></span> | <span data-ttu-id="a1c82-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a1c82-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c82-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1c82-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a1c82-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1c82-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a1c82-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1c82-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a1c82-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a1c82-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a1c82-133">Header</span><span class="sxs-lookup"><span data-stu-id="a1c82-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1c82-134"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a1c82-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a1c82-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a1c82-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1c82-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1c82-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a1c82-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1c82-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1c82-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="a1c82-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a1c82-139">**"Nwinairpakete"-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="a1c82-139">**NewInAirPackets Event**</span></span>](inkpicture-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="a1c82-140">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a1c82-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="a1c82-141">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a1c82-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 





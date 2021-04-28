---
description: 'InkOverlay.NewInAirPackets-Ereignis: Tritt auf, wenn ein In-Air-Paket gesehen wird.'
ms.assetid: 10dc1909-bfbc-4ea0-b77a-e33149205107
title: InkOverlay.NewInAirPackets-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39e568941b1af0727ad9c8464913325409b4604
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086708"
---
# <a name="inkoverlaynewinairpackets-event"></a><span data-ttu-id="cdb19-103">InkOverlay.NewInAirPackets-Ereignis</span><span class="sxs-lookup"><span data-stu-id="cdb19-103">InkOverlay.NewInAirPackets event</span></span>

<span data-ttu-id="cdb19-104">Tritt ein, wenn ein In-Air-Paket gesehen wird.</span><span class="sxs-lookup"><span data-stu-id="cdb19-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdb19-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdb19-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="cdb19-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdb19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdb19-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cdb19-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb19-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**NewInAirPackets-Ereignis generiert**](inkcollector-newinairpackets.md) hat.</span><span class="sxs-lookup"><span data-stu-id="cdb19-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="cdb19-109">*PacketCount* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cdb19-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb19-110">Die Anzahl der empfangenen In-Air-Pakete.</span><span class="sxs-lookup"><span data-stu-id="cdb19-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="cdb19-111">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cdb19-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb19-112">Ein Array, das die ausgewählten Daten für das Paket enthält.</span><span class="sxs-lookup"><span data-stu-id="cdb19-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="cdb19-113">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="cdb19-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdb19-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdb19-114">Return value</span></span>

<span data-ttu-id="cdb19-115">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cdb19-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdb19-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdb19-116">Remarks</span></span>

<span data-ttu-id="cdb19-117">Ein In-Air-Paket wird erstellt, wenn ein Benutzer einen Stift in die Nähe des Tablets verschiebt und sich der Cursor im Fenster des Freiformsammlerobjekts befindet oder der Benutzer eine Maus im zugeordneten Fenster des Freiformsammlerobjekts bewegt.</span><span class="sxs-lookup"><span data-stu-id="cdb19-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="cdb19-118">[**NewInAirPackets-Ereignisse**](inkcollector-newinairpackets.md) werden schnell generiert, und der Ereignishandler muss schnell sein oder die Leistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="cdb19-118">[**NewInAirPackets**](inkcollector-newinairpackets.md) events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="cdb19-119">Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICENewInAirPackets definiert.</span><span class="sxs-lookup"><span data-stu-id="cdb19-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="cdb19-120">Das [**NewInAirPackets-Ereignis**](inkcollector-newinairpackets.md) wird auch dann ausgelöst, wenn es sich im Auswahl- oder Löschmodus befindet, nicht nur beim Einfügen von Ink.</span><span class="sxs-lookup"><span data-stu-id="cdb19-120">The [**NewInAirPackets**](inkcollector-newinairpackets.md) event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="cdb19-121">Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="cdb19-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="cdb19-122">Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein größeres Bewusstsein für Plattformereignisse.</span><span class="sxs-lookup"><span data-stu-id="cdb19-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="cdb19-123">Verwenden Sie zum Festlegen der in diesem Array enthaltenen Eigenschaften die [**DesiredPacketDescription-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) des Ink-Collectorobjekts.</span><span class="sxs-lookup"><span data-stu-id="cdb19-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="cdb19-124">Das Array, das der *PacketData-Parameter* zurückgibt, enthält die Daten für diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cdb19-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="cdb19-125">Obwohl Sie die Paketdaten ändern können, werden diese Änderungen nicht beibehalten oder verwendet.</span><span class="sxs-lookup"><span data-stu-id="cdb19-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cdb19-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdb19-126">Requirements</span></span>



| <span data-ttu-id="cdb19-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdb19-127">Requirement</span></span> | <span data-ttu-id="cdb19-128">Wert</span><span class="sxs-lookup"><span data-stu-id="cdb19-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb19-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cdb19-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cdb19-130">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cdb19-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="cdb19-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cdb19-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cdb19-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cdb19-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="cdb19-133">Header</span><span class="sxs-lookup"><span data-stu-id="cdb19-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdb19-134"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="cdb19-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cdb19-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cdb19-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="cdb19-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdb19-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="cdb19-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cdb19-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdb19-138">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cdb19-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="cdb19-139">**DesiredPacketDescription-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="cdb19-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="cdb19-140">**NewPackets-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="cdb19-140">**NewPackets Event**</span></span>](inkcollector-newpackets.md)
</dt> <dt>

[<span data-ttu-id="cdb19-141">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cdb19-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 





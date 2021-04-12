---
description: Tritt auf, wenn ein in-Air-Paket angezeigt wird.
ms.assetid: 10dc1909-bfbc-4ea0-b77a-e33149205107
title: InkOverlay. nwinairpaketen-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ac030a2e32ecf662d811a3c91ccdc2dd3c5fd03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217678"
---
# <a name="inkoverlaynewinairpackets-event"></a><span data-ttu-id="7e0b1-103">InkOverlay. nwinairpackt-Ereignis</span><span class="sxs-lookup"><span data-stu-id="7e0b1-103">InkOverlay.NewInAirPackets event</span></span>

<span data-ttu-id="7e0b1-104">Tritt auf, wenn ein in-Air-Paket angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7e0b1-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e0b1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e0b1-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="7e0b1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e0b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e0b1-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e0b1-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e0b1-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das Ereignis " [**nwinairpakete**](inkcollector-newinairpackets.md) " generiert hat.</span><span class="sxs-lookup"><span data-stu-id="7e0b1-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="7e0b1-109">*PacketCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e0b1-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e0b1-110">Die Anzahl der empfangenen in-Air-Pakete.</span><span class="sxs-lookup"><span data-stu-id="7e0b1-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="7e0b1-111">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7e0b1-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e0b1-112">Ein Array, das die ausgewählten Daten für das Paket enthält.</span><span class="sxs-lookup"><span data-stu-id="7e0b1-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="7e0b1-113">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="7e0b1-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e0b1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e0b1-114">Return value</span></span>

<span data-ttu-id="7e0b1-115">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7e0b1-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e0b1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e0b1-116">Remarks</span></span>

<span data-ttu-id="7e0b1-117">Ein in-Air-Paket wird erstellt, wenn ein Benutzer einen Stift in der Nähe des Tablets bewegt und sich der Cursor im Fenster des Ink Collector-Objekts befindet oder wenn der Benutzer eine Maus innerhalb des zugehörigen Fensters des Ink Collector-Objekts bewegt.</span><span class="sxs-lookup"><span data-stu-id="7e0b1-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="7e0b1-118">Das generieren [**von Ereignissen wird**](inkcollector-newinairpackets.md) schnell und der Ereignishandler muss schnell oder leistungsstark beeinträchtigt sein.</span><span class="sxs-lookup"><span data-stu-id="7e0b1-118">[**NewInAirPackets**](inkcollector-newinairpackets.md) events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="7e0b1-119">Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icenewinairpakete definiert.</span><span class="sxs-lookup"><span data-stu-id="7e0b1-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="7e0b1-120">Das Ereignis " [**netwinairpackt**](inkcollector-newinairpackets.md) " wird auch dann ausgelöst, wenn es sich im Modus "auswählen" oder "Löschen" befindet</span><span class="sxs-lookup"><span data-stu-id="7e0b1-120">The [**NewInAirPackets**](inkcollector-newinairpackets.md) event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="7e0b1-121">Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie für die Festlegung verantwortlich sind) und den Modus beachten, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="7e0b1-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="7e0b1-122">Der Vorteil dieser Anforderung ist, dass die Innovationen auf der Plattform durch ein höheres Bewusstsein für Platt Form Ereignisse verstärkt werden.</span><span class="sxs-lookup"><span data-stu-id="7e0b1-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="7e0b1-123">Verwenden Sie die [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) -Eigenschaft des Ink Collector-Objekts, um festzulegen, welche Eigenschaften in diesem Array enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7e0b1-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="7e0b1-124">Das Array, das der *packetData* -Parameter zurückgibt, enthält die Daten für diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7e0b1-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="7e0b1-125">Obwohl Sie die Paketdaten ändern können, werden diese Änderungen nicht beibehalten oder verwendet.</span><span class="sxs-lookup"><span data-stu-id="7e0b1-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7e0b1-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e0b1-126">Requirements</span></span>



| <span data-ttu-id="7e0b1-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e0b1-127">Requirement</span></span> | <span data-ttu-id="7e0b1-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7e0b1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e0b1-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e0b1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7e0b1-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e0b1-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7e0b1-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e0b1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7e0b1-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7e0b1-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7e0b1-133">Header</span><span class="sxs-lookup"><span data-stu-id="7e0b1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e0b1-134"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7e0b1-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7e0b1-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7e0b1-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="7e0b1-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e0b1-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7e0b1-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e0b1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e0b1-138">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7e0b1-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="7e0b1-139">**DesiredPacketDescription (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="7e0b1-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="7e0b1-140">**Newpakete-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="7e0b1-140">**NewPackets Event**</span></span>](inkcollector-newpackets.md)
</dt> <dt>

[<span data-ttu-id="7e0b1-141">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7e0b1-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 





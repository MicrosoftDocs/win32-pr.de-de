---
description: Tritt auf, wenn ein in-Air-Paket angezeigt wird.
ms.assetid: 30bc423d-0642-4515-9e51-a8b8b36aecad
title: InkPicture. nwinairpaketen-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0331eb4e855e2051cd8b2b6d7b312d7f32e76096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350299"
---
# <a name="inkpicturenewinairpackets-event"></a><span data-ttu-id="14333-103">InkPicture. nwinairpakete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="14333-103">InkPicture.NewInAirPackets event</span></span>

<span data-ttu-id="14333-104">Tritt auf, wenn ein in-Air-Paket angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="14333-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="14333-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14333-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="14333-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14333-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14333-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14333-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14333-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das Ereignis " **nwinairpakete** " generiert hat.</span><span class="sxs-lookup"><span data-stu-id="14333-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **NewInAirPackets** event.</span></span>

</dd> <dt>

<span data-ttu-id="14333-109">*PacketCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14333-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14333-110">Die Anzahl der empfangenen in-Air-Pakete.</span><span class="sxs-lookup"><span data-stu-id="14333-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="14333-111">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="14333-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="14333-112">Ein Array, das die ausgewählten Daten für das Paket enthält.</span><span class="sxs-lookup"><span data-stu-id="14333-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="14333-113">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="14333-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14333-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14333-114">Return value</span></span>

<span data-ttu-id="14333-115">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="14333-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14333-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14333-116">Remarks</span></span>

<span data-ttu-id="14333-117">Ein in-Air-Paket wird erstellt, wenn ein Benutzer einen Stift in der Nähe des Tablets bewegt und sich der Cursor im Fenster des Ink Collector-Objekts befindet oder wenn der Benutzer eine Maus innerhalb des zugehörigen Fensters des Ink Collector-Objekts bewegt.</span><span class="sxs-lookup"><span data-stu-id="14333-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="14333-118">Das generieren **von Ereignissen wird** schnell und der Ereignishandler muss schnell oder leistungsstark beeinträchtigt sein.</span><span class="sxs-lookup"><span data-stu-id="14333-118">**NewInAirPackets** events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="14333-119">Diese Ereignismethode wird in den Schnittstellen **\_ iinkcollectorevents**, **\_ iinkoverlayevents** und **\_ iinkpictureevents** Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icenewinairpakete definiert.</span><span class="sxs-lookup"><span data-stu-id="14333-119">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="14333-120">Das Ereignis " **netwinairpackt** " wird auch dann ausgelöst, wenn es sich im Modus "auswählen" oder "Löschen" befindet</span><span class="sxs-lookup"><span data-stu-id="14333-120">The **NewInAirPackets** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="14333-121">Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie für die Festlegung verantwortlich sind) und den Modus beachten, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="14333-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="14333-122">Der Vorteil dieser Anforderung ist, dass die Innovationen auf der Plattform durch ein höheres Bewusstsein für Platt Form Ereignisse verstärkt werden.</span><span class="sxs-lookup"><span data-stu-id="14333-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="14333-123">Verwenden Sie die [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) -Eigenschaft des Ink Collector-Objekts, um festzulegen, welche Eigenschaften in diesem Array enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="14333-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="14333-124">Das Array, das der *packetData* -Parameter zurückgibt, enthält die Daten für diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="14333-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="14333-125">Obwohl Sie die Paketdaten ändern können, werden diese Änderungen nicht beibehalten oder verwendet.</span><span class="sxs-lookup"><span data-stu-id="14333-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="14333-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14333-126">Requirements</span></span>



| <span data-ttu-id="14333-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14333-127">Requirement</span></span> | <span data-ttu-id="14333-128">Wert</span><span class="sxs-lookup"><span data-stu-id="14333-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14333-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14333-129">Minimum supported client</span></span><br/> | <span data-ttu-id="14333-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14333-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="14333-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14333-131">Minimum supported server</span></span><br/> | <span data-ttu-id="14333-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="14333-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="14333-133">Header</span><span class="sxs-lookup"><span data-stu-id="14333-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="14333-134"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="14333-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="14333-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="14333-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="14333-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14333-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="14333-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14333-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14333-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="14333-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="14333-139">**DesiredPacketDescription (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="14333-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="14333-140">**Newpakete-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="14333-140">**NewPackets Event**</span></span>](inkpicture-newpackets.md)
</dt> <dt>

[<span data-ttu-id="14333-141">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="14333-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 





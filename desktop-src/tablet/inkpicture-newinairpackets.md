---
description: 'InkPicture.NewInAirPackets-Ereignis: Tritt auf, wenn ein In-Air-Paket erkannt wird.'
ms.assetid: 30bc423d-0642-4515-9e51-a8b8b36aecad
title: InkPicture.NewInAirPackets-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0de8f2423817bada84f83b63de1517393740db4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086558"
---
# <a name="inkpicturenewinairpackets-event"></a><span data-ttu-id="869af-103">InkPicture.NewInAirPackets-Ereignis</span><span class="sxs-lookup"><span data-stu-id="869af-103">InkPicture.NewInAirPackets event</span></span>

<span data-ttu-id="869af-104">Tritt ein, wenn ein In-Air-Paket erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="869af-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="869af-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="869af-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="869af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="869af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="869af-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="869af-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="869af-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **NewInAirPackets-Ereignis** generiert hat.</span><span class="sxs-lookup"><span data-stu-id="869af-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **NewInAirPackets** event.</span></span>

</dd> <dt>

<span data-ttu-id="869af-109">*PacketCount* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="869af-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="869af-110">Die Anzahl der empfangenen In-Air-Pakete.</span><span class="sxs-lookup"><span data-stu-id="869af-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="869af-111">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="869af-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="869af-112">Ein Array, das die ausgewählten Daten für das Paket enthält.</span><span class="sxs-lookup"><span data-stu-id="869af-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="869af-113">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek.](using-the-com-library.md)</span><span class="sxs-lookup"><span data-stu-id="869af-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="869af-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="869af-114">Return value</span></span>

<span data-ttu-id="869af-115">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="869af-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="869af-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="869af-116">Remarks</span></span>

<span data-ttu-id="869af-117">Ein In-Air-Paket wird erstellt, wenn ein Benutzer einen Stift in der Nähe des Tabletts verschiebt und sich der Cursor im Fenster des Freihandsammlerobjekts befindet oder der Benutzer eine Maus innerhalb des zugeordneten Fensters des Freihandsammlerobjekts bewegt.</span><span class="sxs-lookup"><span data-stu-id="869af-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="869af-118">**NewInAirPackets-Ereignisse** werden schnell generiert, und der Ereignishandler muss schnell sein, oder die Leistung beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="869af-118">**NewInAirPackets** events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="869af-119">Diese Ereignismethode wird in den Dispatch-Only-Schnittstellen **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ ICENewInAirPackets definiert.</span><span class="sxs-lookup"><span data-stu-id="869af-119">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="869af-120">Das **NewInAirPackets-Ereignis** wird ausgelöst, auch wenn sie sich im Auswahl- oder Löschmodus befinden, nicht nur beim Einfügen von Ink.</span><span class="sxs-lookup"><span data-stu-id="869af-120">The **NewInAirPackets** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="869af-121">Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="869af-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="869af-122">Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein höheres Bewusstsein für Plattformereignisse.</span><span class="sxs-lookup"><span data-stu-id="869af-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="869af-123">Verwenden Sie die [**DesiredPacketDescription-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) des Ink-Collectorobjekts, um festzulegen, welche Eigenschaften in diesem Array enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="869af-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="869af-124">Das Array, das der *PacketData-Parameter* zurückgibt, enthält die Daten für diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="869af-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="869af-125">Obwohl Sie die Paketdaten ändern können, werden diese Änderungen nicht beibehalten oder verwendet.</span><span class="sxs-lookup"><span data-stu-id="869af-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="869af-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="869af-126">Requirements</span></span>



| <span data-ttu-id="869af-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="869af-127">Requirement</span></span> | <span data-ttu-id="869af-128">Wert</span><span class="sxs-lookup"><span data-stu-id="869af-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="869af-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="869af-129">Minimum supported client</span></span><br/> | <span data-ttu-id="869af-130">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="869af-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="869af-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="869af-131">Minimum supported server</span></span><br/> | <span data-ttu-id="869af-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="869af-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="869af-133">Header</span><span class="sxs-lookup"><span data-stu-id="869af-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="869af-134"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="869af-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="869af-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="869af-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="869af-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="869af-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="869af-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="869af-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="869af-138">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="869af-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="869af-139">**DesiredPacketDescription-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="869af-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="869af-140">**NewPackets-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="869af-140">**NewPackets Event**</span></span>](inkpicture-newpackets.md)
</dt> <dt>

[<span data-ttu-id="869af-141">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="869af-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 





---
description: Gibt die Startzeit der Präsentation an.
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: MF_TOPONODE_MEDIASTART-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab00727cc328bfd6ba780050160fb21eecbb96f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361763"
---
# <a name="mf_toponode_mediastart-attribute"></a><span data-ttu-id="b5c80-103">MF \_ toponode \_ mediastart-Attribut</span><span class="sxs-lookup"><span data-stu-id="b5c80-103">MF\_TOPONODE\_MEDIASTART attribute</span></span>

<span data-ttu-id="b5c80-104">Gibt die Startzeit der Präsentation an.</span><span class="sxs-lookup"><span data-stu-id="b5c80-104">Specifies the start time of the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="b5c80-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b5c80-105">Data type</span></span>

<span data-ttu-id="b5c80-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="b5c80-106">**UINT64**</span></span>

<span data-ttu-id="b5c80-107">Als **Longlong** -Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="b5c80-107">Treat as a **LONGLONG** value.</span></span>

## <a name="getset"></a><span data-ttu-id="b5c80-108">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="b5c80-108">Get/set</span></span>

<span data-ttu-id="b5c80-109">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="b5c80-109">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="b5c80-110">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="b5c80-110">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b5c80-111">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="b5c80-111">Applies to</span></span>

[<span data-ttu-id="b5c80-112">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="b5c80-112">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a><span data-ttu-id="b5c80-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5c80-113">Remarks</span></span>

<span data-ttu-id="b5c80-114">Dieses Attribut gibt die Position in der Quelle an, an der die Wiedergabe in 100-Nanosecond-Einheiten relativ zum Start der Quelle beginnt.</span><span class="sxs-lookup"><span data-stu-id="b5c80-114">This attribute specifies the position in the source where playback starts, in 100-nanosecond units, relative to the start the source.</span></span> <span data-ttu-id="b5c80-115">Wenn das-Attribut nicht festgelegt ist, wird die Wiedergabe bei NULL (dem Anfang der Datei) gestartet.</span><span class="sxs-lookup"><span data-stu-id="b5c80-115">If the attribute is not set, playback starts at zero (the start of the file).</span></span> <span data-ttu-id="b5c80-116">Wenn Sie z. b. die Wiedergabe an der 5-Sekunden-Markierung starten möchten, legen Sie dieses Attribut auf 50 Millionen fest.</span><span class="sxs-lookup"><span data-stu-id="b5c80-116">For example, to start playback at the 5-second mark, set this attribute to 50000000.</span></span> <span data-ttu-id="b5c80-117">Legen Sie das-Attribut auf den Quellknoten in der Topologie fest (Knoten, deren Typ gleich der **MF- \_ Topologie \_ sourcestream- \_ Knoten** ist).</span><span class="sxs-lookup"><span data-stu-id="b5c80-117">Set the attribute on the source nodes in the topology (nodes with type equal to **MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="b5c80-118">Legen Sie das-Attribut vor dem Aufrufen von [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)fest.</span><span class="sxs-lookup"><span data-stu-id="b5c80-118">Set the attribute before calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

> [!Note]  
> <span data-ttu-id="b5c80-119">Wenn Sie einen Decoder manuell in die Topologie einfügen, müssen Sie auch die hier aufgeführten Attribute " [MF \_ toponode \_ Markin \_ here](mf-toponode-markin-here-attribute.md) " und " [MF \_ toponode \_ markout \_ ](mf-toponode-markout-here-attribute.md) " auf dem Decoder-Knoten festlegen.</span><span class="sxs-lookup"><span data-stu-id="b5c80-119">If you manually insert a decoder into the topology, you must also set the [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) and [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) attributes on the decoder node.</span></span>

 

<span data-ttu-id="b5c80-120">Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="b5c80-120">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="b5c80-121">Negative Werte sind jedoch nicht sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="b5c80-121">However, negative values are not meaningful.</span></span>

<span data-ttu-id="b5c80-122">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="b5c80-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5c80-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5c80-123">Requirements</span></span>



| <span data-ttu-id="b5c80-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5c80-124">Requirement</span></span> | <span data-ttu-id="b5c80-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b5c80-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c80-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5c80-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b5c80-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5c80-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b5c80-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5c80-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b5c80-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5c80-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b5c80-130">Header</span><span class="sxs-lookup"><span data-stu-id="b5c80-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5c80-131"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5c80-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5c80-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5c80-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5c80-133">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b5c80-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b5c80-134">Sequenz Präsentations Zeiten</span><span class="sxs-lookup"><span data-stu-id="b5c80-134">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="b5c80-135">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="b5c80-135">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="b5c80-136">**MF- \_ toponode- \_ mediastop**</span><span class="sxs-lookup"><span data-stu-id="b5c80-136">**MF\_TOPONODE\_MEDIASTOP**</span></span>](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 





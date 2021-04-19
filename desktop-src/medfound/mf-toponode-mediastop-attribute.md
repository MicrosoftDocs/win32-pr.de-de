---
description: Gibt die Endzeit der Präsentation an.
ms.assetid: c1022538-ea9f-41e9-9075-c106e8b16b7b
title: MF_TOPONODE_MEDIASTOP-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5b763d1d5adabc520900dde6839d1599ddcb3d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363033"
---
# <a name="mf_toponode_mediastop-attribute"></a><span data-ttu-id="e2d93-103">MF- \_ toponode- \_ mediastop-Attribut</span><span class="sxs-lookup"><span data-stu-id="e2d93-103">MF\_TOPONODE\_MEDIASTOP attribute</span></span>

<span data-ttu-id="e2d93-104">Gibt die Endzeit der Präsentation an.</span><span class="sxs-lookup"><span data-stu-id="e2d93-104">Specifies the stop time of the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="e2d93-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e2d93-105">Data type</span></span>

<span data-ttu-id="e2d93-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="e2d93-106">**UINT64**</span></span>

<span data-ttu-id="e2d93-107">Als **Longlong** -Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="e2d93-107">Treat as a **LONGLONG** value.</span></span>

## <a name="getset"></a><span data-ttu-id="e2d93-108">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="e2d93-108">Get/set</span></span>

<span data-ttu-id="e2d93-109">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="e2d93-109">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="e2d93-110">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="e2d93-110">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e2d93-111">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="e2d93-111">Applies to</span></span>

[<span data-ttu-id="e2d93-112">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="e2d93-112">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a><span data-ttu-id="e2d93-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2d93-113">Remarks</span></span>

<span data-ttu-id="e2d93-114">Dieses Attribut gibt die Position in der Quelle an, an der die Wiedergabe in 100-Nanosecond-Einheiten relativ zum Start der Quelle beendet wird.</span><span class="sxs-lookup"><span data-stu-id="e2d93-114">This attribute specifies the position in the source where playback stops, in 100-nanosecond units, relative to the start the source.</span></span> <span data-ttu-id="e2d93-115">Wenn das Attribut nicht festgelegt ist, wird die Wiedergabe am Ende der Quelle angehalten.</span><span class="sxs-lookup"><span data-stu-id="e2d93-115">If the attribute is not set, playback stops at the end of the source.</span></span> <span data-ttu-id="e2d93-116">Um z. b. die Wiedergabe an der 5-Sekunden-Markierung anzuhalten, legen Sie dieses Attribut auf 50 Millionen fest.</span><span class="sxs-lookup"><span data-stu-id="e2d93-116">For example, to stop playback at the 5-second mark, set this attribute to 50000000.</span></span> <span data-ttu-id="e2d93-117">Legen Sie das-Attribut auf den Quellknoten in der Topologie fest (Knoten, deren Typ gleich der **MF- \_ Topologie \_ sourcestream- \_ Knoten** ist).</span><span class="sxs-lookup"><span data-stu-id="e2d93-117">Set the attribute on the source nodes in the topology (nodes with type equal to **MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="e2d93-118">Legen Sie das-Attribut vor dem Aufrufen von [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)fest.</span><span class="sxs-lookup"><span data-stu-id="e2d93-118">Set the attribute before calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

> [!Note]  
> <span data-ttu-id="e2d93-119">Wenn Sie einen Decoder manuell in die Topologie einfügen, müssen Sie auch die hier aufgeführten Attribute " [MF \_ toponode \_ Markin \_ here](mf-toponode-markin-here-attribute.md) " und " [MF \_ toponode \_ markout \_ ](mf-toponode-markout-here-attribute.md) " auf dem Decoder-Knoten festlegen.</span><span class="sxs-lookup"><span data-stu-id="e2d93-119">If you manually insert a decoder into the topology, you must also set the [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) and [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) attributes on the decoder node.</span></span>

 

<span data-ttu-id="e2d93-120">Nachdem die Topologie festgelegt wurde, hat das Festlegen dieses Attributs keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="e2d93-120">After the topology is set, setting this attribute has no effect.</span></span>

<span data-ttu-id="e2d93-121">Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e2d93-121">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="e2d93-122">Negative Werte sind jedoch nicht sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="e2d93-122">However, negative values are not meaningful.</span></span>

<span data-ttu-id="e2d93-123">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="e2d93-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d93-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2d93-124">Requirements</span></span>



| <span data-ttu-id="e2d93-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2d93-125">Requirement</span></span> | <span data-ttu-id="e2d93-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e2d93-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d93-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2d93-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e2d93-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2d93-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e2d93-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2d93-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e2d93-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2d93-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e2d93-131">Header</span><span class="sxs-lookup"><span data-stu-id="e2d93-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2d93-132"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2d93-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2d93-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2d93-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d93-134">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e2d93-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e2d93-135">Sequenz Präsentations Zeiten</span><span class="sxs-lookup"><span data-stu-id="e2d93-135">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="e2d93-136">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="e2d93-136">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="e2d93-137">**MF \_ toponode \_ mediastart**</span><span class="sxs-lookup"><span data-stu-id="e2d93-137">**MF\_TOPONODE\_MEDIASTART**</span></span>](mf-toponode-mediastart-attribute.md)
</dt> </dl>

 

 





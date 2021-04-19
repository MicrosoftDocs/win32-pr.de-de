---
description: Enthält den Medien Untertyp für einen topologieknoten. Dieses Attribut wird festgelegt, wenn die Topologie nicht geladen werden kann, da der richtige Decoder nicht gefunden werden konnte.
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: MF_TOPONODE_ERROR_SUBTYPE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1233fb62c271a6f4fd84ec8b2c0b34aa6c49b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348830"
---
# <a name="mf_toponode_error_subtype-attribute"></a><span data-ttu-id="a08ae-104">MF- \_ toponode- \_ \_ fehlersubtype-Attribut</span><span class="sxs-lookup"><span data-stu-id="a08ae-104">MF\_TOPONODE\_ERROR\_SUBTYPE attribute</span></span>

<span data-ttu-id="a08ae-105">Enthält den Medien Untertyp für einen topologieknoten.</span><span class="sxs-lookup"><span data-stu-id="a08ae-105">Contains the media subtype for a topology node.</span></span> <span data-ttu-id="a08ae-106">Dieses Attribut wird festgelegt, wenn die Topologie nicht geladen werden kann, da der richtige Decoder nicht gefunden werden konnte.</span><span class="sxs-lookup"><span data-stu-id="a08ae-106">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>

## <a name="data-type"></a><span data-ttu-id="a08ae-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a08ae-107">Data type</span></span>

<span data-ttu-id="a08ae-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="a08ae-108">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="a08ae-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a08ae-109">Remarks</span></span>

<span data-ttu-id="a08ae-110">Dieses Attribut gilt für alle Knoten Typen.</span><span class="sxs-lookup"><span data-stu-id="a08ae-110">This attribute applies to all node types.</span></span>

<span data-ttu-id="a08ae-111">Das topologielader-Attribut kann das-Attribut festlegen.</span><span class="sxs-lookup"><span data-stu-id="a08ae-111">The topology loader might set the attribute.</span></span> <span data-ttu-id="a08ae-112">Anwendungen lesen dieses Attribut in der Regel, ohne es festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a08ae-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="a08ae-113">Eine Liste möglicher Werte finden Sie unter [Medientyp-GUIDs](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="a08ae-113">For a list of possible values, see [Media Type GUIDs](media-type-guids.md).</span></span>

<span data-ttu-id="a08ae-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="a08ae-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a08ae-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a08ae-115">Requirements</span></span>



| <span data-ttu-id="a08ae-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a08ae-116">Requirement</span></span> | <span data-ttu-id="a08ae-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a08ae-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a08ae-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a08ae-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a08ae-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a08ae-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a08ae-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a08ae-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a08ae-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a08ae-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a08ae-122">Header</span><span class="sxs-lookup"><span data-stu-id="a08ae-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a08ae-123"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a08ae-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a08ae-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a08ae-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08ae-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a08ae-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a08ae-126">**Imfattributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="a08ae-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="a08ae-127">**Imfattributes:: SetGuid**</span><span class="sxs-lookup"><span data-stu-id="a08ae-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="a08ae-128">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="a08ae-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="a08ae-129">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="a08ae-129">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 





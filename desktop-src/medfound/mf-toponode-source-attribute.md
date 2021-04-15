---
description: Enthält einen Zeiger auf die Medienquelle, die einem topologieknoten zugeordnet ist.
ms.assetid: 73b84ab6-bdc2-4b22-9ce4-b79b954476e5
title: MF_TOPONODE_SOURCE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57904e9797e0f669b2cb782750e4ae9199059d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527422"
---
# <a name="mf_toponode_source-attribute"></a><span data-ttu-id="cf6d6-103">MF- \_ toponode- \_ Quell Attribut</span><span class="sxs-lookup"><span data-stu-id="cf6d6-103">MF\_TOPONODE\_SOURCE attribute</span></span>

<span data-ttu-id="cf6d6-104">Enthält einen Zeiger auf die Medienquelle, die einem topologieknoten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cf6d6-104">Contains a pointer to the media source associated with a topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="cf6d6-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cf6d6-105">Data type</span></span>

<span data-ttu-id="cf6d6-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="cf6d6-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="cf6d6-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf6d6-107">Remarks</span></span>

<span data-ttu-id="cf6d6-108">Dieses Attribut gilt für Quellknoten (_ \* MF- \_ Topologie \_ sourcestream- \_ Knoten \* \*).</span><span class="sxs-lookup"><span data-stu-id="cf6d6-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="cf6d6-109">Der Wert des-Attributs ist ein Zeiger auf die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="cf6d6-109">The value of the attribute is a pointer to the media source's [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="cf6d6-110">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cf6d6-110">This attribute is required.</span></span>

<span data-ttu-id="cf6d6-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="cf6d6-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf6d6-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf6d6-112">Requirements</span></span>



| <span data-ttu-id="cf6d6-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf6d6-113">Requirement</span></span> | <span data-ttu-id="cf6d6-114">Wert</span><span class="sxs-lookup"><span data-stu-id="cf6d6-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6d6-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf6d6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cf6d6-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf6d6-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cf6d6-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf6d6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cf6d6-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf6d6-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cf6d6-119">Header</span><span class="sxs-lookup"><span data-stu-id="cf6d6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf6d6-120"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf6d6-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf6d6-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf6d6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf6d6-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="cf6d6-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cf6d6-123">**Imfattributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="cf6d6-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="cf6d6-124">\**Imfattributes:: *-Known**</span><span class="sxs-lookup"><span data-stu-id="cf6d6-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="cf6d6-125">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="cf6d6-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="cf6d6-126">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="cf6d6-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 





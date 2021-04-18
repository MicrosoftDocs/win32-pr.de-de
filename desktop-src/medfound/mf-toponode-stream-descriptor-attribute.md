---
description: Enthält einen Zeiger auf den Datenstrom Deskriptor für die Medienquelle.
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: MF_TOPONODE_STREAM_DESCRIPTOR-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f074a1c1ffde3671779362724676f884c3b6b0b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368148"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a><span data-ttu-id="37be3-103">Das MF- \_ toponode- \_ \_ streamdeskriptorattribut</span><span class="sxs-lookup"><span data-stu-id="37be3-103">MF\_TOPONODE\_STREAM\_DESCRIPTOR attribute</span></span>

<span data-ttu-id="37be3-104">Enthält einen Zeiger auf den Datenstrom Deskriptor für die Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="37be3-104">Contains a pointer to the stream descriptor for the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="37be3-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="37be3-105">Data type</span></span>

<span data-ttu-id="37be3-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="37be3-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="37be3-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37be3-107">Remarks</span></span>

<span data-ttu-id="37be3-108">Dieses Attribut gilt für Quellknoten (_ \* MF- \_ Topologie \_ sourcestream- \_ Knoten \* \*).</span><span class="sxs-lookup"><span data-stu-id="37be3-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="37be3-109">Der Wert des-Attributs ist ein Zeiger auf die [**imfstreamdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) -Schnittstelle des Stream-Deskriptors.</span><span class="sxs-lookup"><span data-stu-id="37be3-109">The value of the attribute is a pointer to the stream descriptor's [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) interface.</span></span> <span data-ttu-id="37be3-110">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37be3-110">This attribute is required.</span></span>

<span data-ttu-id="37be3-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="37be3-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="37be3-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37be3-112">Requirements</span></span>



| <span data-ttu-id="37be3-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37be3-113">Requirement</span></span> | <span data-ttu-id="37be3-114">Wert</span><span class="sxs-lookup"><span data-stu-id="37be3-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37be3-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37be3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="37be3-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37be3-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="37be3-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37be3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="37be3-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37be3-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="37be3-119">Header</span><span class="sxs-lookup"><span data-stu-id="37be3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="37be3-120"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="37be3-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37be3-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37be3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37be3-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="37be3-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="37be3-123">**Imfattributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="37be3-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="37be3-124">\**Imfattributes:: *-Known**</span><span class="sxs-lookup"><span data-stu-id="37be3-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="37be3-125">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="37be3-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="37be3-126">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="37be3-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 





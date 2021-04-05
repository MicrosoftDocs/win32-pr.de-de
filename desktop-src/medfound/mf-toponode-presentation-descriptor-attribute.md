---
description: Enthält einen Zeiger auf den Präsentations Deskriptor für die Medienquelle.
ms.assetid: 4f2c1ad8-fda9-482f-b82a-9838d15d2785
title: MF_TOPONODE_PRESENTATION_DESCRIPTOR-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d95fae4f2c4d4a482c2a62d57e0835ea4f1c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753160"
---
# <a name="mf_toponode_presentation_descriptor-attribute"></a><span data-ttu-id="9a0cc-103">MF- \_ toponode- \_ Präsentations \_ deskriptorattribut</span><span class="sxs-lookup"><span data-stu-id="9a0cc-103">MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR attribute</span></span>

<span data-ttu-id="9a0cc-104">Enthält einen Zeiger auf den Präsentations Deskriptor für die Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-104">Contains a pointer to the presentation descriptor for the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="9a0cc-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9a0cc-105">Data type</span></span>

<span data-ttu-id="9a0cc-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="9a0cc-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="9a0cc-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a0cc-107">Remarks</span></span>

<span data-ttu-id="9a0cc-108">Dieses Attribut gilt für Quellknoten (_ \* MF- \_ Topologie \_ sourcestream- \_ Knoten \* \*).</span><span class="sxs-lookup"><span data-stu-id="9a0cc-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="9a0cc-109">Der Wert des-Attributs ist ein Zeiger auf die [**imfpresentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Schnittstelle des Präsentations Deskriptors.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-109">The value of the attribute is a pointer to the presentation descriptor's [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface.</span></span> <span data-ttu-id="9a0cc-110">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-110">This attribute is required.</span></span>

<span data-ttu-id="9a0cc-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0cc-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a0cc-112">Requirements</span></span>



| <span data-ttu-id="9a0cc-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a0cc-113">Requirement</span></span> | <span data-ttu-id="9a0cc-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9a0cc-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9a0cc-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a0cc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9a0cc-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a0cc-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9a0cc-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a0cc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9a0cc-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a0cc-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9a0cc-119">Header</span><span class="sxs-lookup"><span data-stu-id="9a0cc-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a0cc-120"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a0cc-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a0cc-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a0cc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a0cc-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9a0cc-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9a0cc-123">**Imfattributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="9a0cc-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="9a0cc-124">\**Imfattributes:: *-Known**</span><span class="sxs-lookup"><span data-stu-id="9a0cc-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="9a0cc-125">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="9a0cc-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="9a0cc-126">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9a0cc-126">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 





---
description: Gibt an, ob die Medien Sitzung versucht, die Topologie zu ändern, wenn das Format eines Datenstroms geändert wird.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ade7308c4fadef315fae0828a5c2cb29575b03a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484803"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a><span data-ttu-id="c1526-103">Die \_ dynamische Änderung der MF-Topologie ist \_ \_ \_ nicht \_ zulässig.</span><span class="sxs-lookup"><span data-stu-id="c1526-103">MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED attribute</span></span>

<span data-ttu-id="c1526-104">Gibt an, ob die Medien Sitzung versucht, die Topologie zu ändern, wenn das Format eines Datenstroms geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c1526-104">Specifies whether the Media Session attempts to modify the topology when the format of a stream changes.</span></span>

## <a name="data-type"></a><span data-ttu-id="c1526-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c1526-105">Data type</span></span>

<span data-ttu-id="c1526-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c1526-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c1526-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="c1526-107">Get/set</span></span>

<span data-ttu-id="c1526-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c1526-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c1526-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="c1526-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c1526-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="c1526-110">Applies to</span></span>

[<span data-ttu-id="c1526-111">**Imftopology**</span><span class="sxs-lookup"><span data-stu-id="c1526-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="c1526-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1526-112">Remarks</span></span>

<span data-ttu-id="c1526-113">Dieses Attribut steuert, wie die Medien Sitzung antwortet, wenn sich das Format eines Streams beim Streaming ändert.</span><span class="sxs-lookup"><span data-stu-id="c1526-113">This attribute controls how the Media Session responds if the format of a stream changes during streaming.</span></span>

<span data-ttu-id="c1526-114">Wenn das Format geändert wird und das \_ Attribut "dynamische Änderung der MF-Topologie \_ \_ nicht zulässig" auf "false" gesetzt \_ \_ ist, kann die Medien Sitzung neue Knoten in die Topologie einfügen, damit Sie dem neuen Format entspricht. </span><span class="sxs-lookup"><span data-stu-id="c1526-114">If the format changes and the MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED attribute is **FALSE**, the Media Session might insert new nodes into the topology to match the new format.</span></span> <span data-ttu-id="c1526-115">Wenn sich beispielsweise die Videogröße ändert, kann die Medien Sitzung eine Media Foundation Transformation (MFT) hinzufügen, die die Größe des Videos ändert.</span><span class="sxs-lookup"><span data-stu-id="c1526-115">For example, if the video size changes, the Media Session might add a Media Foundation transform (MFT) that resizes the video.</span></span> <span data-ttu-id="c1526-116">Wenn das Attribut **true** ist, wird die Topologie in der Medien Sitzung nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="c1526-116">Otherwise, if the attribute is **TRUE**, the Media Session will not modify the topology.</span></span>

<span data-ttu-id="c1526-117">Der Standardwert dieses Attributs ist **false**.</span><span class="sxs-lookup"><span data-stu-id="c1526-117">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="c1526-118">Der empfohlene Wert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="c1526-118">The recommended value is **FALSE**.</span></span>

<span data-ttu-id="c1526-119">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="c1526-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1526-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1526-120">Requirements</span></span>



| <span data-ttu-id="c1526-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1526-121">Requirement</span></span> | <span data-ttu-id="c1526-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c1526-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1526-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1526-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c1526-124">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1526-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c1526-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1526-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c1526-126">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1526-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c1526-127">Header</span><span class="sxs-lookup"><span data-stu-id="c1526-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1526-128"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1526-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1526-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1526-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1526-130">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c1526-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c1526-131">Topologieattribute</span><span class="sxs-lookup"><span data-stu-id="c1526-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 





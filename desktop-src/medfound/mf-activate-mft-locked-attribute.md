---
description: Gibt an, ob das topologielader die Medientypen in einer Media Foundation Transformation (MFT) ändert. Anwendungen verwenden dieses Attribut in der Regel nicht.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: MF_ACTIVATE_MFT_LOCKED-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d6dcb6cb60f760d87761a18b2b83545937878c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130725"
---
# <a name="mf_activate_mft_locked-attribute"></a><span data-ttu-id="8824e-104">MF \_ Aktivieren des \_ MFT- \_ gesperrten Attributs</span><span class="sxs-lookup"><span data-stu-id="8824e-104">MF\_ACTIVATE\_MFT\_LOCKED attribute</span></span>

<span data-ttu-id="8824e-105">Gibt an, ob das topologielader die Medientypen in einer Media Foundation Transformation (MFT) ändert.</span><span class="sxs-lookup"><span data-stu-id="8824e-105">Specifies whether the Topology Loader will change the media types on a Media Foundation transform (MFT).</span></span> <span data-ttu-id="8824e-106">Anwendungen verwenden dieses Attribut in der Regel nicht.</span><span class="sxs-lookup"><span data-stu-id="8824e-106">Applications typically do not use this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="8824e-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8824e-107">Data type</span></span>

<span data-ttu-id="8824e-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8824e-108">**UINT32**</span></span>

<span data-ttu-id="8824e-109">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="8824e-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8824e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8824e-110">Remarks</span></span>

<span data-ttu-id="8824e-111">Wenn der Wert dieses Attributs ungleich 0 (null) ist, werden die Medientypen in der MFT vom topologielader nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="8824e-111">If value of this attribute is nonzero, the topology loader will not change the media types on the MFT.</span></span> <span data-ttu-id="8824e-112">Das topologielader legt dieses Attribut fest, nachdem es die Topologie geladen hat.</span><span class="sxs-lookup"><span data-stu-id="8824e-112">The topology loader sets this attribute after it loads the topology.</span></span>

<span data-ttu-id="8824e-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="8824e-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8824e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8824e-114">Requirements</span></span>



| <span data-ttu-id="8824e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8824e-115">Requirement</span></span> | <span data-ttu-id="8824e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8824e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8824e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8824e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8824e-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8824e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8824e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8824e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8824e-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8824e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8824e-121">Header</span><span class="sxs-lookup"><span data-stu-id="8824e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8824e-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8824e-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8824e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8824e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8824e-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="8824e-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8824e-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8824e-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8824e-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8824e-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="8824e-127">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="8824e-127">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 





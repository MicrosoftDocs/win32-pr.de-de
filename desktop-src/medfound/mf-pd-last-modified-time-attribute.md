---
description: Gibt an, wann eine Präsentation zuletzt geändert wurde.
ms.assetid: 12990de2-7656-4781-943b-c46f42a0e38d
title: MF_PD_LAST_MODIFIED_TIME-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f97bf47cff32834b694f36cbd4c9062e06f2d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960091"
---
# <a name="mf_pd_last_modified_time-attribute"></a><span data-ttu-id="76ff5-103">\_Zeit Attribut für die \_ Letzte \_ Änderung \_ der MF-PD</span><span class="sxs-lookup"><span data-stu-id="76ff5-103">MF\_PD\_LAST\_MODIFIED\_TIME attribute</span></span>

<span data-ttu-id="76ff5-104">Gibt an, wann eine Präsentation zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="76ff5-104">Specifies when a presentation was last modified.</span></span>

## <a name="data-type"></a><span data-ttu-id="76ff5-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="76ff5-105">Data type</span></span>

<span data-ttu-id="76ff5-106">Bytearray</span><span class="sxs-lookup"><span data-stu-id="76ff5-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="76ff5-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76ff5-107">Remarks</span></span>

<span data-ttu-id="76ff5-108">Medienquellen können dieses Attribut für einen Präsentations Deskriptor festlegen.</span><span class="sxs-lookup"><span data-stu-id="76ff5-108">Media sources can set this attribute on a presentation descriptor.</span></span> <span data-ttu-id="76ff5-109">Der Wert des-Attributs ist eine **FILETIME** -Struktur, die in der Windows SDK dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="76ff5-109">The value of the attribute is a **FILETIME** structure, which is documented in the Windows SDK.</span></span>

<span data-ttu-id="76ff5-110">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="76ff5-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="76ff5-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76ff5-111">Requirements</span></span>



| <span data-ttu-id="76ff5-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76ff5-112">Requirement</span></span> | <span data-ttu-id="76ff5-113">Wert</span><span class="sxs-lookup"><span data-stu-id="76ff5-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76ff5-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76ff5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="76ff5-115">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="76ff5-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="76ff5-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76ff5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="76ff5-117">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="76ff5-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="76ff5-118">Header</span><span class="sxs-lookup"><span data-stu-id="76ff5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="76ff5-119"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="76ff5-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76ff5-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76ff5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ff5-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="76ff5-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="76ff5-122">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="76ff5-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="76ff5-123">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="76ff5-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="76ff5-124">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="76ff5-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="76ff5-125">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="76ff5-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 





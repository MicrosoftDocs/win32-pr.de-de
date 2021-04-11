---
description: Enthält einen Zeiger auf den Präsentations Deskriptor aus dem geschützten Medien Pfad (PMP).
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: MF_PD_APP_CONTEXT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217541"
---
# <a name="mf_pd_app_context-attribute"></a><span data-ttu-id="36100-103">MF- \_ PD- \_ App- \_ Kontext Attribut</span><span class="sxs-lookup"><span data-stu-id="36100-103">MF\_PD\_APP\_CONTEXT attribute</span></span>

<span data-ttu-id="36100-104">Enthält einen Zeiger auf den Präsentations Deskriptor aus dem geschützten Medien Pfad (PMP).</span><span class="sxs-lookup"><span data-stu-id="36100-104">Contains a pointer to the presentation descriptor from the Protected Media Path (PMP).</span></span>

## <a name="data-type"></a><span data-ttu-id="36100-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="36100-105">Data type</span></span>

<span data-ttu-id="36100-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="36100-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="36100-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36100-107">Remarks</span></span>

<span data-ttu-id="36100-108">Der Medienquellen Proxy, der im PMP-Prozess erstellt wird, verwendet dieses Attribut, um den Remote Präsentations Deskriptor im Präsentations Deskriptor der Anwendung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="36100-108">The media source proxy, which is created in the PMP process, uses this attribute to store the remote presentation descriptor on the application's presentation descriptor.</span></span>

<span data-ttu-id="36100-109">Der Wert dieses Attributs ist ein Zeiger auf die [_ *imfpresentationdescriptor* \*](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="36100-109">The value of this attribute is a pointer to the [_ *IMFPresentationDescriptor*\*](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface.</span></span>

<span data-ttu-id="36100-110">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="36100-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="36100-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36100-111">Requirements</span></span>



| <span data-ttu-id="36100-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36100-112">Requirement</span></span> | <span data-ttu-id="36100-113">Wert</span><span class="sxs-lookup"><span data-stu-id="36100-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36100-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36100-114">Minimum supported client</span></span><br/> | <span data-ttu-id="36100-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36100-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="36100-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36100-116">Minimum supported server</span></span><br/> | <span data-ttu-id="36100-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36100-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="36100-118">Header</span><span class="sxs-lookup"><span data-stu-id="36100-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="36100-119"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="36100-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36100-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36100-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36100-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="36100-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="36100-122">**Imfattributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="36100-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="36100-123">\**Imfattributes:: *-Known**</span><span class="sxs-lookup"><span data-stu-id="36100-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="36100-124">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="36100-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 





---
description: Enthält einen Zeiger auf das Proxy Objekt für den Anwendungs Präsentations Deskriptor.
ms.assetid: 0cd83204-0d32-417c-8911-1d3358eb0802
title: MF_PD_PMPHOST_CONTEXT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e8903e438a4649ae43d7aa2072e5a5146e3126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393705"
---
# <a name="mf_pd_pmphost_context-attribute"></a><span data-ttu-id="73ea0-103">MF \_ PD \_ pmphost- \_ Kontext Attribut</span><span class="sxs-lookup"><span data-stu-id="73ea0-103">MF\_PD\_PMPHOST\_CONTEXT attribute</span></span>

<span data-ttu-id="73ea0-104">Enthält einen Zeiger auf das Proxy Objekt für den Präsentations Deskriptor der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="73ea0-104">Contains a pointer to the proxy object for the application's presentation descriptor.</span></span>

## <a name="data-type"></a><span data-ttu-id="73ea0-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="73ea0-105">Data type</span></span>

<span data-ttu-id="73ea0-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="73ea0-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="73ea0-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73ea0-107">Remarks</span></span>

<span data-ttu-id="73ea0-108">Der PMP-Host (Protected Media Path) verwendet dieses Attribut, um den Präsentations Deskriptor der Anwendung auf dem Remote Präsentations Deskriptor zu speichern.</span><span class="sxs-lookup"><span data-stu-id="73ea0-108">The Protected Media Path (PMP) host uses this attribute to store the application's presentation descriptor on the remote presentation descriptor.</span></span> <span data-ttu-id="73ea0-109">Der Attribut Wert ist ein Zeiger auf die [_ *imfremoteproxy* \*](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="73ea0-109">The attribute value is a pointer to the [_ *IMFRemoteProxy*\*](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) interface.</span></span>

<span data-ttu-id="73ea0-110">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="73ea0-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="73ea0-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73ea0-111">Requirements</span></span>



| <span data-ttu-id="73ea0-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73ea0-112">Requirement</span></span> | <span data-ttu-id="73ea0-113">Wert</span><span class="sxs-lookup"><span data-stu-id="73ea0-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73ea0-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73ea0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="73ea0-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73ea0-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="73ea0-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73ea0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="73ea0-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73ea0-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="73ea0-118">Header</span><span class="sxs-lookup"><span data-stu-id="73ea0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="73ea0-119"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="73ea0-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73ea0-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73ea0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ea0-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="73ea0-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="73ea0-122">**Imfattributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="73ea0-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="73ea0-123">\**Imfattributes:: *-Known**</span><span class="sxs-lookup"><span data-stu-id="73ea0-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="73ea0-124">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="73ea0-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="73ea0-125">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="73ea0-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 





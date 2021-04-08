---
description: Enthält einen Zeiger auf die imfnettresourcefilter-Rückruf Schnittstelle für den Microsoft Media Foundation http-Byte-Stream.
ms.assetid: C035B4AD-CF99-4A4F-9384-F80A3620BD27
title: MFNETSOURCE_RESOURCE_FILTER-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da94e8bc0bedba3e47dc2784119a5b30d2bffcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754257"
---
# <a name="mfnetsource_resource_filter-property"></a><span data-ttu-id="ce3f3-103">MF-Quell \_ Ressourcen \_ Filter (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ce3f3-103">MFNETSOURCE\_RESOURCE\_FILTER property</span></span>

<span data-ttu-id="ce3f3-104">Enthält einen Zeiger auf die [**imfnettresourcefilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) -Rückruf Schnittstelle für den Microsoft Media Foundation http-Byte-Stream.</span><span class="sxs-lookup"><span data-stu-id="ce3f3-104">Contains a pointer to the [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) callback interface for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="ce3f3-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ce3f3-105">Data type</span></span>

<span data-ttu-id="ce3f3-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="ce3f3-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="ce3f3-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="ce3f3-107">PROPVARIANT member</span></span>

<span data-ttu-id="ce3f3-108">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="ce3f3-108">\**IUnknown\** _</span></span>

<span data-ttu-id="ce3f3-109">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="ce3f3-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="ce3f3-110">_ *punkVal*\*</span><span class="sxs-lookup"><span data-stu-id="ce3f3-110">_ *punkVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="ce3f3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce3f3-111">Remarks</span></span>

<span data-ttu-id="ce3f3-112">Verwenden Sie diese Eigenschaft, um den Media Foundation http-Bytestream zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ce3f3-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="ce3f3-113">Um die-Eigenschaft festzulegen, übergeben Sie einen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="ce3f3-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="ce3f3-114">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="ce3f3-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce3f3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce3f3-115">Requirements</span></span>



| <span data-ttu-id="ce3f3-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce3f3-116">Requirement</span></span> | <span data-ttu-id="ce3f3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ce3f3-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce3f3-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce3f3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ce3f3-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce3f3-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ce3f3-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce3f3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ce3f3-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce3f3-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ce3f3-122">Header</span><span class="sxs-lookup"><span data-stu-id="ce3f3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce3f3-123"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce3f3-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce3f3-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce3f3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce3f3-125">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ce3f3-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

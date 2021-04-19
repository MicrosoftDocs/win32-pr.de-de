---
description: Definiert bei YUV-Medientypen die Konvertierungs Matrix aus dem YCbCr-Farbraum in den RGB-Farbraum.
ms.assetid: b268d16d-b4cc-4026-9ba7-805cc5409b95
title: MF_MT_YUV_MATRIX-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0c6976e4652c69b3bddc910dcc536a3d07bf39a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373315"
---
# <a name="mf_mt_yuv_matrix-attribute"></a><span data-ttu-id="edec8-103">MF \_ MT \_ YUV \_ Matrix-Attribut</span><span class="sxs-lookup"><span data-stu-id="edec8-103">MF\_MT\_YUV\_MATRIX attribute</span></span>

<span data-ttu-id="edec8-104">Definiert bei YUV-Medientypen die Konvertierungs Matrix aus dem Farbraum ' ' der ' '-Eigenschaft ' CR ' in den ' g '-Farbbereich.</span><span class="sxs-lookup"><span data-stu-id="edec8-104">For YUV media types, defines the conversion matrix from the Y'Cb'Cr' color space to the R'G'B' color space.</span></span>

## <a name="data-type"></a><span data-ttu-id="edec8-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="edec8-105">Data type</span></span>

<span data-ttu-id="edec8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="edec8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="edec8-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="edec8-107">Remarks</span></span>

<span data-ttu-id="edec8-108">Der Wert dieses Attributs ist ein Member der [**mfvideotransfermatrix**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="edec8-108">The value of this attribute is a member of the [**MFVideoTransferMatrix**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) enumeration.</span></span>

<span data-ttu-id="edec8-109">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="edec8-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="edec8-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="edec8-110">Requirements</span></span>



| <span data-ttu-id="edec8-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="edec8-111">Requirement</span></span> | <span data-ttu-id="edec8-112">Wert</span><span class="sxs-lookup"><span data-stu-id="edec8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="edec8-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="edec8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="edec8-114">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="edec8-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="edec8-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="edec8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="edec8-116">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="edec8-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="edec8-117">Header</span><span class="sxs-lookup"><span data-stu-id="edec8-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="edec8-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="edec8-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edec8-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edec8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edec8-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="edec8-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="edec8-121">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="edec8-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="edec8-122">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="edec8-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="edec8-123">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="edec8-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="edec8-124">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="edec8-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="edec8-125">Erweiterte Farbinformationen</span><span class="sxs-lookup"><span data-stu-id="edec8-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 





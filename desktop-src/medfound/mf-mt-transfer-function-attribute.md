---
description: Gibt die Konvertierungs Funktion von RGB in RGB für einen Video Medientyp an.
ms.assetid: c64c2135-f588-4d7a-9ca8-ae4f7b290572
title: MF_MT_TRANSFER_FUNCTION-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d175a0e40d0aba45b4ec664d71e236e077e09a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358506"
---
# <a name="mf_mt_transfer_function-attribute"></a><span data-ttu-id="62d8e-103">MF \_ MT- \_ Übertragungs \_ Funktions Attribut</span><span class="sxs-lookup"><span data-stu-id="62d8e-103">MF\_MT\_TRANSFER\_FUNCTION attribute</span></span>

<span data-ttu-id="62d8e-104">Gibt die Konvertierungs Funktion für einen Video Medientyp zwischen RGB und r' B ' an.</span><span class="sxs-lookup"><span data-stu-id="62d8e-104">Specifies the conversion function from RGB to R'G'B' for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="62d8e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="62d8e-105">Data type</span></span>

<span data-ttu-id="62d8e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="62d8e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="62d8e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62d8e-107">Remarks</span></span>

<span data-ttu-id="62d8e-108">Der Wert dieses Attributs ist ein Member der [**mfvideotransferfunction**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransferfunction) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="62d8e-108">The value of this attribute is a member of the [**MFVideoTransferFunction**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransferfunction) enumeration.</span></span>

<span data-ttu-id="62d8e-109">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="62d8e-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="62d8e-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62d8e-110">Requirements</span></span>



| <span data-ttu-id="62d8e-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62d8e-111">Requirement</span></span> | <span data-ttu-id="62d8e-112">Wert</span><span class="sxs-lookup"><span data-stu-id="62d8e-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62d8e-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62d8e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="62d8e-114">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="62d8e-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="62d8e-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62d8e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="62d8e-116">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="62d8e-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="62d8e-117">Header</span><span class="sxs-lookup"><span data-stu-id="62d8e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="62d8e-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="62d8e-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62d8e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62d8e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62d8e-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="62d8e-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="62d8e-121">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="62d8e-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="62d8e-122">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="62d8e-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="62d8e-123">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="62d8e-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="62d8e-124">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="62d8e-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="62d8e-125">Erweiterte Farbinformationen</span><span class="sxs-lookup"><span data-stu-id="62d8e-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 





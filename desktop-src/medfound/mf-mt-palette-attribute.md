---
description: Enthält die Paletteneinträge für einen Video Medientyp. Verwenden Sie dieses Attribut für Paletten-Videoformate, wie z. b. RGB 8.
ms.assetid: 3efc124b-073e-4c48-9550-c100e29f2d6f
title: MF_MT_PALETTE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dcfc596ae463cf642cc462da1c73dc641356d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355655"
---
# <a name="mf_mt_palette-attribute"></a><span data-ttu-id="80fa5-104">MF- \_ MT- \_ Palette-Attribut</span><span class="sxs-lookup"><span data-stu-id="80fa5-104">MF\_MT\_PALETTE attribute</span></span>

<span data-ttu-id="80fa5-105">Enthält die Paletteneinträge für einen Video Medientyp.</span><span class="sxs-lookup"><span data-stu-id="80fa5-105">Contains the palette entries for a video media type.</span></span> <span data-ttu-id="80fa5-106">Verwenden Sie dieses Attribut für Paletten-Videoformate, wie z. b. RGB 8.</span><span class="sxs-lookup"><span data-stu-id="80fa5-106">Use this attribute for palettized video formats, such as RGB 8.</span></span>

## <a name="data-type"></a><span data-ttu-id="80fa5-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="80fa5-107">Data type</span></span>

<span data-ttu-id="80fa5-108">Bytearray</span><span class="sxs-lookup"><span data-stu-id="80fa5-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="80fa5-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80fa5-109">Remarks</span></span>

<span data-ttu-id="80fa5-110">Bei den Attributdaten handelt es sich um ein Array von [**MF-etteentry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) -Unions.</span><span class="sxs-lookup"><span data-stu-id="80fa5-110">The attribute data is an array of [**MFPaletteEntry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) unions.</span></span>

<span data-ttu-id="80fa5-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="80fa5-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="80fa5-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80fa5-112">Requirements</span></span>



| <span data-ttu-id="80fa5-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80fa5-113">Requirement</span></span> | <span data-ttu-id="80fa5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="80fa5-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="80fa5-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80fa5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="80fa5-116">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="80fa5-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="80fa5-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80fa5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="80fa5-118">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="80fa5-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="80fa5-119">Header</span><span class="sxs-lookup"><span data-stu-id="80fa5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="80fa5-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="80fa5-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80fa5-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80fa5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80fa5-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="80fa5-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="80fa5-123">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="80fa5-123">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="80fa5-124">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="80fa5-124">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="80fa5-125">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="80fa5-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="80fa5-126">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="80fa5-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 





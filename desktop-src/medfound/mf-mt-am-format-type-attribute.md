---
description: Enthält eine DirectShow-Format-GUID für einen Medientyp.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: MF_MT_AM_FORMAT_TYPE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a8faf88128075e5c5b51c1b5ace39329d4e1fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344569"
---
# <a name="mf_mt_am_format_type-attribute"></a><span data-ttu-id="444ec-103">MF \_ MT \_ am \_ \_ formatType-Attribut</span><span class="sxs-lookup"><span data-stu-id="444ec-103">MF\_MT\_AM\_FORMAT\_TYPE attribute</span></span>

<span data-ttu-id="444ec-104">Enthält eine DirectShow-Format-GUID für einen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="444ec-104">Contains a DirectShow format GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="444ec-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="444ec-105">Data type</span></span>

<span data-ttu-id="444ec-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="444ec-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="444ec-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="444ec-107">Remarks</span></span>

<span data-ttu-id="444ec-108">Dieses Attribut kann festgelegt werden, wenn ein DirectShow-Medientyp in einen Media Foundation Medientyp konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="444ec-108">This attribute might be set when a DirectShow media type is converted into a Media Foundation media type.</span></span> <span data-ttu-id="444ec-109">Das-Attribut gibt den ursprünglichen DirectShow-Formattyp an.</span><span class="sxs-lookup"><span data-stu-id="444ec-109">The attribute indicates the original DirectShow format type.</span></span> <span data-ttu-id="444ec-110">Der Wert entspricht dem Format Type-Member der [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="444ec-110">The value corresponds to the formattype member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="444ec-111">Bei einem Audioformat kann das [**MF \_ MT- \_ Benutzer \_ Daten**](mf-mt-user-data-attribute.md) Attribut den ursprünglichen Format Block enthalten, wenn der DirectShow-Formattyp nicht erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="444ec-111">For an audio format, the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute might contain the original format block, if the DirectShow format type was not recognized.</span></span>

<span data-ttu-id="444ec-112">Legen Sie dieses Attribut nicht für einen Medientyp fest, es sei denn, Sie wandeln eine DirectShow-Format Struktur um.</span><span class="sxs-lookup"><span data-stu-id="444ec-112">Do not set this attribute on a media type unless you are converting a DirectShow format structure.</span></span>

<span data-ttu-id="444ec-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="444ec-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="444ec-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="444ec-114">Requirements</span></span>



| <span data-ttu-id="444ec-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="444ec-115">Requirement</span></span> | <span data-ttu-id="444ec-116">Wert</span><span class="sxs-lookup"><span data-stu-id="444ec-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="444ec-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="444ec-117">Minimum supported client</span></span><br/> | <span data-ttu-id="444ec-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="444ec-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="444ec-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="444ec-119">Minimum supported server</span></span><br/> | <span data-ttu-id="444ec-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="444ec-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="444ec-121">Header</span><span class="sxs-lookup"><span data-stu-id="444ec-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="444ec-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="444ec-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="444ec-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="444ec-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="444ec-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="444ec-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="444ec-125">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="444ec-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="444ec-126">Medientyp Konvertierungen</span><span class="sxs-lookup"><span data-stu-id="444ec-126">Media Type Conversions</span></span>](media-type-conversions.md)
</dt> <dt>

[<span data-ttu-id="444ec-127">Medientypen</span><span class="sxs-lookup"><span data-stu-id="444ec-127">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="444ec-128">**Imfattributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="444ec-128">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="444ec-129">**Imfattributes:: SetGuid**</span><span class="sxs-lookup"><span data-stu-id="444ec-129">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="444ec-130">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="444ec-130">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="444ec-131">**MF-Datei (MF)**</span><span class="sxs-lookup"><span data-stu-id="444ec-131">**MFCreateMediaTypeFromRepresentation**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 

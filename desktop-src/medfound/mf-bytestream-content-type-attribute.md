---
description: Gibt den MIME-Typ eines Bytestreams an.
ms.assetid: bcf86ece-2673-4ed8-98fd-cd0e2154b4a8
title: MF_BYTESTREAM_CONTENT_TYPE-Attribut (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7413fa6fd2ce74530432d60976e3c7ebf702af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347811"
---
# <a name="mf_bytestream_content_type-attribute"></a><span data-ttu-id="a240b-103">MF- \_ Bytestream- \_ \_ Inhaltstyp Attribut</span><span class="sxs-lookup"><span data-stu-id="a240b-103">MF\_BYTESTREAM\_CONTENT\_TYPE attribute</span></span>

<span data-ttu-id="a240b-104">Gibt den MIME-Typ eines Bytestreams an.</span><span class="sxs-lookup"><span data-stu-id="a240b-104">Specifies the MIME type of a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="a240b-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a240b-105">Data type</span></span>

<span data-ttu-id="a240b-106">Breitzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a240b-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="a240b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a240b-107">Remarks</span></span>

<span data-ttu-id="a240b-108">Um den Attribut Wert zu erhalten, Fragen Sie das Byte Datenstrom Objekt für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="a240b-108">To get the attribute value, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="a240b-109">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="a240b-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a240b-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a240b-110">Requirements</span></span>



| <span data-ttu-id="a240b-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a240b-111">Requirement</span></span> | <span data-ttu-id="a240b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a240b-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a240b-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a240b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a240b-114">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a240b-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="a240b-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a240b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a240b-116">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a240b-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="a240b-117">Header</span><span class="sxs-lookup"><span data-stu-id="a240b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a240b-118"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a240b-118"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a240b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a240b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a240b-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a240b-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a240b-121">Byte Datenstrom Attribute</span><span class="sxs-lookup"><span data-stu-id="a240b-121">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="a240b-122">**Imfattributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="a240b-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="a240b-123">**Imfattributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="a240b-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="a240b-124">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="a240b-124">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 





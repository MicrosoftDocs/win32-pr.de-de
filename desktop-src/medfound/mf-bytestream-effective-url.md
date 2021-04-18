---
description: Ruft die effektive URL eines Bytestreams ab.
ms.assetid: 0A83CFC0-7EAA-464B-BA39-50DF220AF683
title: MF_BYTESTREAM_EFFECTIVE_URL-Attribut (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95e01238f04c30f72d55f940b3f3105863247ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368126"
---
# <a name="mf_bytestream_effective_url-attribute"></a><span data-ttu-id="1c4b9-103">Effektive MF- \_ Bytestream- \_ URL- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="1c4b9-103">MF\_BYTESTREAM\_EFFECTIVE\_URL attribute</span></span>

<span data-ttu-id="1c4b9-104">Ruft die effektive URL eines Bytestreams ab.</span><span class="sxs-lookup"><span data-stu-id="1c4b9-104">Gets the effective URL of a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="1c4b9-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1c4b9-105">Data type</span></span>

## <a name="getset"></a><span data-ttu-id="1c4b9-106">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="1c4b9-106">Get/set</span></span>

<span data-ttu-id="1c4b9-107">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="1c4b9-107">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="1c4b9-108">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1c4b9-108">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="1c4b9-109">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="1c4b9-109">Applies to</span></span>

[<span data-ttu-id="1c4b9-110">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="1c4b9-110">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a><span data-ttu-id="1c4b9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c4b9-111">Remarks</span></span>

<span data-ttu-id="1c4b9-112">Die effektive URL kann sich von der ursprünglichen URL unterscheiden, wenn die ursprüngliche URL zusätzliche Informationen enthält, z. b. Such Zeichenfolgen oder Anker, oder wenn die Anforderung umgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="1c4b9-112">The effective URL can differ from the original URL if the original URL contains any extra information, such as search strings or anchors, or if the request was redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c4b9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c4b9-113">Requirements</span></span>



| <span data-ttu-id="1c4b9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c4b9-114">Requirement</span></span> | <span data-ttu-id="1c4b9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1c4b9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c4b9-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c4b9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1c4b9-117">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1c4b9-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                      |
| <span data-ttu-id="1c4b9-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c4b9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1c4b9-119">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1c4b9-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                            |
| <span data-ttu-id="1c4b9-120">Header</span><span class="sxs-lookup"><span data-stu-id="1c4b9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c4b9-121"><dt>Mfobjects. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c4b9-121"><dt>Mfobjects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c4b9-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c4b9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c4b9-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="1c4b9-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1c4b9-124">Byte Datenstrom Attribute</span><span class="sxs-lookup"><span data-stu-id="1c4b9-124">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="1c4b9-125">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="1c4b9-125">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 





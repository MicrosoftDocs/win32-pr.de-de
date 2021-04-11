---
description: Gibt die Sprache für einen Datenstrom an.
ms.assetid: b64a9554-a560-4212-8964-b68ebbadc046
title: MF_SD_LANGUAGE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad13ec4d7d17e715bd2583e499c686de26c7b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217540"
---
# <a name="mf_sd_language-attribute"></a><span data-ttu-id="a3830-103">MF \_ SD- \_ sprach Attribut</span><span class="sxs-lookup"><span data-stu-id="a3830-103">MF\_SD\_LANGUAGE attribute</span></span>

<span data-ttu-id="a3830-104">Gibt die Sprache für einen Datenstrom an.</span><span class="sxs-lookup"><span data-stu-id="a3830-104">Specifies the language for a stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="a3830-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a3830-105">Data type</span></span>

<span data-ttu-id="a3830-106">Breitzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a3830-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="a3830-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3830-107">Remarks</span></span>

<span data-ttu-id="a3830-108">Der Wert dieses Attributs ist ein RFC 1766-kompatibles Sprachtag.</span><span class="sxs-lookup"><span data-stu-id="a3830-108">The value of this attribute is an RFC 1766-compliant language tag.</span></span> <span data-ttu-id="a3830-109">Dieses Attribut gilt für streamdeskriptoren.</span><span class="sxs-lookup"><span data-stu-id="a3830-109">This attribute applies to stream descriptors.</span></span>

<span data-ttu-id="a3830-110">Eine Medienquelle (oder ein beliebiges Objekt, das einen streamdeskriptor erstellt) kann dieses Attribut festlegen, wenn der Stream eine bestimmte Sprache hat.</span><span class="sxs-lookup"><span data-stu-id="a3830-110">A media source (or any object that creates a stream descriptor) can set this attribute if the stream has a specified language.</span></span> <span data-ttu-id="a3830-111">Anwendungen können dieses Attribut Abfragen, um die Sprache zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a3830-111">Applications can query this attribute to get the language.</span></span> <span data-ttu-id="a3830-112">Wenn das-Attribut nicht festgelegt ist, hat der Stream keine bestimmte Sprache.</span><span class="sxs-lookup"><span data-stu-id="a3830-112">If the attribute is not set, the stream does not have a specified language.</span></span>

<span data-ttu-id="a3830-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="a3830-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3830-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3830-114">Requirements</span></span>



| <span data-ttu-id="a3830-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3830-115">Requirement</span></span> | <span data-ttu-id="a3830-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a3830-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3830-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3830-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a3830-118">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a3830-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a3830-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3830-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a3830-120">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a3830-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a3830-121">Header</span><span class="sxs-lookup"><span data-stu-id="a3830-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3830-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3830-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3830-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3830-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3830-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a3830-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a3830-125">**Imfattributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="a3830-125">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="a3830-126">**Imfattributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="a3830-126">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="a3830-127">**IMF-Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="a3830-127">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="a3830-128">Streamdeskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="a3830-128">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 





---
description: Enthält den Namen eines Streams.
ms.assetid: 80235820-761f-4deb-9bf6-82ef402b3ee4
title: MF_SD_STREAM_NAME-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734c2d20390ba1a450a40c03054b4c67c5c0409a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349119"
---
# <a name="mf_sd_stream_name-attribute"></a><span data-ttu-id="b0b11-103">\_SD-SD-Stream- \_ \_ Namensattribut</span><span class="sxs-lookup"><span data-stu-id="b0b11-103">MF\_SD\_STREAM\_NAME attribute</span></span>

<span data-ttu-id="b0b11-104">Enthält den Namen eines Streams.</span><span class="sxs-lookup"><span data-stu-id="b0b11-104">Contains the name of a stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="b0b11-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b0b11-105">Data type</span></span>

<span data-ttu-id="b0b11-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="b0b11-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="b0b11-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="b0b11-107">Get/set</span></span>

<span data-ttu-id="b0b11-108">Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="b0b11-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="b0b11-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b0b11-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b0b11-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="b0b11-110">Applies to</span></span>

[<span data-ttu-id="b0b11-111">**IMF-Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="b0b11-111">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a><span data-ttu-id="b0b11-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0b11-112">Remarks</span></span>

<span data-ttu-id="b0b11-113">Mit der AVI-Medienquelle wird dieses Attribut festgelegt, wenn die AVI-Datei ein "" "" ein "-Segment enthält.</span><span class="sxs-lookup"><span data-stu-id="b0b11-113">The AVI media source sets this attribute if the AVI file contains a 'strn' chunk.</span></span>

<span data-ttu-id="b0b11-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="b0b11-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b11-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0b11-115">Requirements</span></span>



| <span data-ttu-id="b0b11-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0b11-116">Requirement</span></span> | <span data-ttu-id="b0b11-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b0b11-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b11-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0b11-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b0b11-119">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b0b11-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b0b11-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0b11-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b0b11-121">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b0b11-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b0b11-122">Header</span><span class="sxs-lookup"><span data-stu-id="b0b11-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0b11-123"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0b11-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0b11-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0b11-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b11-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b0b11-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b0b11-126">Streamdeskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="b0b11-126">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 





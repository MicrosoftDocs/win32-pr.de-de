---
description: Enthält den ursprünglichen Codec FourCC für einen Videostream.
ms.assetid: 2e6ef198-5754-4ded-9fe3-61edd0742a17
title: MF_MT_ORIGINAL_4CC-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b374ba3ef74cb98925edcc5d809e1fd5e0b7fbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960412"
---
# <a name="mf_mt_original_4cc-attribute"></a><span data-ttu-id="58e19-103">MF \_ MT \_ ursprüngliches \_ 4CC-Attribut</span><span class="sxs-lookup"><span data-stu-id="58e19-103">MF\_MT\_ORIGINAL\_4CC attribute</span></span>

<span data-ttu-id="58e19-104">Enthält den ursprünglichen Codec FourCC für einen Videostream.</span><span class="sxs-lookup"><span data-stu-id="58e19-104">Contains the original codec FOURCC for a video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="58e19-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="58e19-105">Data type</span></span>

<span data-ttu-id="58e19-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="58e19-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="58e19-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="58e19-107">Get/set</span></span>

<span data-ttu-id="58e19-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="58e19-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="58e19-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="58e19-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="58e19-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="58e19-110">Applies to</span></span>

[<span data-ttu-id="58e19-111">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="58e19-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="58e19-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58e19-112">Remarks</span></span>

<span data-ttu-id="58e19-113">Abhängig von der Quelldatei kann die AVI-Medienquelle dieses Attribut auf den Medientypen festlegen, die es anbietet.</span><span class="sxs-lookup"><span data-stu-id="58e19-113">Depending on the source file, the AVI media source might set this attribute on the media types that it offers.</span></span>

<span data-ttu-id="58e19-114">Eine AVI-Datei enthält einen Streamheader für jeden Stream in der Datei.</span><span class="sxs-lookup"><span data-stu-id="58e19-114">An AVI file contains a stream header for each stream in the file.</span></span> <span data-ttu-id="58e19-115">Die AVI-Medienquelle übersetzt den Datenstrom Header in einen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="58e19-115">The AVI media source translates the stream header into a media type.</span></span> <span data-ttu-id="58e19-116">Für komprimierte Videostreams enthält der Stream-Header ein FourCC, das den Videocodec identifiziert.</span><span class="sxs-lookup"><span data-stu-id="58e19-116">For compressed video streams, the stream header contains a FOURCC that identifies the video codec.</span></span> <span data-ttu-id="58e19-117">In den meisten Fällen konvertiert die AVI-Medienquelle diesen FourCC direkt in eine Untertyp-GUID, wie im Thema [Video Untertyp-GUIDs](video-subtype-guids.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="58e19-117">In most cases, the AVI media source converts this FOURCC directly to a subtype GUID, as described in the topic [Video Subtype GUIDs](video-subtype-guids.md).</span></span> <span data-ttu-id="58e19-118">In einigen Fällen wird das ursprüngliche FourCC jedoch einem anderen FourCC zugeordnet, das Äquivalent ist.</span><span class="sxs-lookup"><span data-stu-id="58e19-118">In some cases, however, it maps the original FOURCC to another FOURCC that is equivalent.</span></span> <span data-ttu-id="58e19-119">Wenn dies der Fall ist, speichert die Medienquelle den ursprünglichen FourCC im Medientyp, wobei das MF \_ MT \_ Original \_ 4CC-Attribut verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58e19-119">If so, the media source stores the original FOURCC in the media type, using the MF\_MT\_ORIGINAL\_4CC attribute.</span></span>

<span data-ttu-id="58e19-120">Die FourCC-Zuordnungen werden in der Registrierung unter folgendem Schlüssel gespeichert:</span><span class="sxs-lookup"><span data-stu-id="58e19-120">The FOURCC mappings are stored in the Registry under the following key:</span></span>

<span data-ttu-id="58e19-121">**HKEY \_ Klassen- \_ root** \\ **mediafoundations** \\ **MapVideo4cc**</span><span class="sxs-lookup"><span data-stu-id="58e19-121">**HKEY\_CLASSES\_ROOT**\\**MediaFoundation**\\**MapVideo4cc**</span></span>

<span data-ttu-id="58e19-122">Jeder Eintrag ist ein **DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="58e19-122">Each entry is a **DWORD** value.</span></span> <span data-ttu-id="58e19-123">Der Name des Eintrags ist die hexadezimale Darstellung des FourCC ohne das Präfix "0x" und das erste Zeichen, das zuerst in der Zeichenfolge angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="58e19-123">The name of the entry is the hexadecimal representation of the FOURCC, without an "0x" prefix, and with the first character appearing first in the string.</span></span> <span data-ttu-id="58e19-124">Der FourCC-Code "abcd" würde z. b. als "61626364" angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="58e19-124">For example, the FOURCC code 'abcd' would appear as "61626364".</span></span> <span data-ttu-id="58e19-125">Der Wert des Eintrags ist der entsprechende FourCC-Code.</span><span class="sxs-lookup"><span data-stu-id="58e19-125">The value of the entry is the equivalent FOURCC code.</span></span>

<span data-ttu-id="58e19-126">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="58e19-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e19-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58e19-127">Requirements</span></span>



| <span data-ttu-id="58e19-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58e19-128">Requirement</span></span> | <span data-ttu-id="58e19-129">Wert</span><span class="sxs-lookup"><span data-stu-id="58e19-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58e19-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58e19-130">Minimum supported client</span></span><br/> | <span data-ttu-id="58e19-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58e19-131">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="58e19-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58e19-132">Minimum supported server</span></span><br/> | <span data-ttu-id="58e19-133">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58e19-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="58e19-134">Header</span><span class="sxs-lookup"><span data-stu-id="58e19-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="58e19-135"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="58e19-135"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e19-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58e19-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e19-137">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="58e19-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="58e19-138">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="58e19-138">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 





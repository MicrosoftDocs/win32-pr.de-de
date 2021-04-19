---
description: Enthält das ursprüngliche Wave-Formattag für einen Audiodatenstrom.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: MF_MT_ORIGINAL_WAVE_FORMAT_TAG-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba89171f9ae2bf3ab99df05bd3ae64b7d52be6d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357082"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a><span data-ttu-id="4fda7-103">Das MF \_ MT-Tag- \_ Attribut für ursprüngliches \_ Wellen \_ Format \_</span><span class="sxs-lookup"><span data-stu-id="4fda7-103">MF\_MT\_ORIGINAL\_WAVE\_FORMAT\_TAG attribute</span></span>

<span data-ttu-id="4fda7-104">Enthält das ursprüngliche Wave-Formattag für einen Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="4fda7-104">Contains the original WAVE format tag for an audio stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="4fda7-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4fda7-105">Data type</span></span>

<span data-ttu-id="4fda7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4fda7-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="4fda7-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="4fda7-107">Get/set</span></span>

<span data-ttu-id="4fda7-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="4fda7-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4fda7-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="4fda7-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="4fda7-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="4fda7-110">Applies to</span></span>

[<span data-ttu-id="4fda7-111">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="4fda7-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="4fda7-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fda7-112">Remarks</span></span>

<span data-ttu-id="4fda7-113">Abhängig von der Quelldatei kann die AVI-Medienquelle dieses Attribut auf den Medientypen festlegen, die es anbietet.</span><span class="sxs-lookup"><span data-stu-id="4fda7-113">Depending on the source file, the AVI media source might set this attribute on the media types that it offers.</span></span>

<span data-ttu-id="4fda7-114">Eine AVI-Datei enthält einen Streamheader für jeden Stream in der Datei.</span><span class="sxs-lookup"><span data-stu-id="4fda7-114">An AVI file contains a stream header for each stream in the file.</span></span> <span data-ttu-id="4fda7-115">Die AVI-Medienquelle übersetzt den Datenstrom Header in einen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="4fda7-115">The AVI media source translates the stream header into a media type.</span></span> <span data-ttu-id="4fda7-116">Für Audiostreams enthält der Stream-Header ein Formattag, das das Audioformat identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4fda7-116">For audio streams, the stream header contains a format tag that identifies the audio format.</span></span> <span data-ttu-id="4fda7-117">(Das Formattag ist im **wformattag** -Member der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur enthalten.) In den meisten Fällen konvertiert die AVI-Medienquelle das Formattag direkt in eine Untertyp-GUID, wie im Thema [**audiountertyp-GUIDs**](audio-subtype-guids.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4fda7-117">(The format tag is contained in the **wFormatTag** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.) In most cases, the AVI media source converts the format tag directly to a subtype GUID, as described in the topic [**Audio Subtype GUIDs**](audio-subtype-guids.md).</span></span> <span data-ttu-id="4fda7-118">In einigen Fällen wird das ursprüngliche Formattag jedoch einem anderen Format-Tag zugeordnet, das Äquivalent ist.</span><span class="sxs-lookup"><span data-stu-id="4fda7-118">In some cases, however, it maps the original format tag to another format tag that is equivalent.</span></span> <span data-ttu-id="4fda7-119">Wenn dies der Fall ist, speichert die Medienquelle das ursprüngliche Formatierungstag im Medientyp unter Verwendung des "MF \_ MT \_ Original \_ Wave Format"- \_ \_ tagattributs.</span><span class="sxs-lookup"><span data-stu-id="4fda7-119">If so, the media source stores the original format tag in the media type, using the MF\_MT\_ORIGINAL\_WAVE\_FORMAT\_TAG attribute.</span></span>

<span data-ttu-id="4fda7-120">Die Format Zuordnungen werden in der Registrierung unter dem folgenden Schlüssel gespeichert:</span><span class="sxs-lookup"><span data-stu-id="4fda7-120">The format mappings are stored in the Registry under the following key:</span></span>

<span data-ttu-id="4fda7-121">**HKEY \_ Klassen \_** Stamm \\ **mediafoundung** \\ **mapaudioformattag**</span><span class="sxs-lookup"><span data-stu-id="4fda7-121">**HKEY\_CLASSES\_ROOT**\\**MediaFoundation**\\**MapAudioFormatTag**</span></span>

<span data-ttu-id="4fda7-122">Jeder Eintrag ist ein **DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="4fda7-122">Each entry is a **DWORD** value.</span></span> <span data-ttu-id="4fda7-123">Der Name des Eintrags ist die Dezimal Darstellung des Formattags.</span><span class="sxs-lookup"><span data-stu-id="4fda7-123">The name of the entry is the decimal representation of the format tag.</span></span> <span data-ttu-id="4fda7-124">Der Wert des Eintrags ist das entsprechende Formattag.</span><span class="sxs-lookup"><span data-stu-id="4fda7-124">The value of the entry is the equivalent format tag.</span></span>

<span data-ttu-id="4fda7-125">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="4fda7-125">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fda7-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fda7-126">Requirements</span></span>



| <span data-ttu-id="4fda7-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fda7-127">Requirement</span></span> | <span data-ttu-id="4fda7-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4fda7-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4fda7-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fda7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4fda7-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fda7-130">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4fda7-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fda7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4fda7-132">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fda7-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4fda7-133">Header</span><span class="sxs-lookup"><span data-stu-id="4fda7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fda7-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fda7-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fda7-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fda7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fda7-136">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4fda7-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4fda7-137">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="4fda7-137">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 

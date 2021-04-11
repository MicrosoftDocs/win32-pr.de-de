---
description: Gibt in einem audiomedientyp die Zuweisung von Audiokanälen zu Redner Positionen an.
ms.assetid: fa5f6baa-0a21-4162-8870-38e71763aba0
title: MF_MT_AUDIO_CHANNEL_MASK-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5293f5387a2c293b97ee32db54fcfb3f3ff304d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041954"
---
# <a name="mf_mt_audio_channel_mask-attribute"></a><span data-ttu-id="2962a-103">MF \_ MT \_ - \_ Audiokanal- \_ Attribut Maske</span><span class="sxs-lookup"><span data-stu-id="2962a-103">MF\_MT\_AUDIO\_CHANNEL\_MASK attribute</span></span>

<span data-ttu-id="2962a-104">Gibt in einem audiomedientyp die Zuweisung von Audiokanälen zu Redner Positionen an.</span><span class="sxs-lookup"><span data-stu-id="2962a-104">In an audio media type, specifies the assignment of audio channels to speaker positions.</span></span>

## <a name="data-type"></a><span data-ttu-id="2962a-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2962a-105">Data type</span></span>

<span data-ttu-id="2962a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2962a-106">**UINT32**</span></span>

<span data-ttu-id="2962a-107">Der Wert dieses Attributs ist ein bitweises **or** der folgenden Flags, die in der Header Datei "mmreg. h" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2962a-107">The value of this attribute is a bitwise **OR** of the following flags, which are defined in the header file mmreg.h.</span></span>

<dl> <dt>

<span data-ttu-id="2962a-108"><span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**Sprecher \_ Front- \_ Links** (0x1)</span><span class="sxs-lookup"><span data-stu-id="2962a-108"><span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**SPEAKER\_FRONT\_LEFT** (0x1)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-109"><span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**Sprecher \_ Front- \_ right** (0x2)</span><span class="sxs-lookup"><span data-stu-id="2962a-109"><span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**SPEAKER\_FRONT\_RIGHT** (0x2)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-110"><span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**Sprecher \_ Front- \_ Center** (0x4)</span><span class="sxs-lookup"><span data-stu-id="2962a-110"><span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**SPEAKER\_FRONT\_CENTER** (0x4)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-111"><span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**Sprecher \_ Niedrige \_ Häufigkeit** (0x8)</span><span class="sxs-lookup"><span data-stu-id="2962a-111"><span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**SPEAKER\_LOW\_FREQUENCY** (0x8)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-112"><span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**Sprecher \_ Zurück \_ Links** (0x10)</span><span class="sxs-lookup"><span data-stu-id="2962a-112"><span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**SPEAKER\_BACK\_LEFT** (0x10)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-113"><span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**Sprecher \_ Zurück \_ Rechts** (0x20)</span><span class="sxs-lookup"><span data-stu-id="2962a-113"><span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**SPEAKER\_BACK\_RIGHT** (0x20)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-114"><span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**Sprecher \_ Vordere \_ linke \_ \_ Mitte** (0x40)</span><span class="sxs-lookup"><span data-stu-id="2962a-114"><span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**SPEAKER\_FRONT\_LEFT\_OF\_CENTER** (0x40)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-115"><span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**Sprecher \_ Vorder \_ Seite \_ von \_ Mitte** (0x80)</span><span class="sxs-lookup"><span data-stu-id="2962a-115"><span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**SPEAKER\_FRONT\_RIGHT\_OF\_CENTER** (0x80)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-116"><span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**Sprecher \_ \_Backcenter** (0x100)</span><span class="sxs-lookup"><span data-stu-id="2962a-116"><span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**SPEAKER\_BACK\_CENTER** (0x100)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-117"><span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**Sprecher \_ Seite \_ Links** (0x200)</span><span class="sxs-lookup"><span data-stu-id="2962a-117"><span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**SPEAKER\_SIDE\_LEFT** (0x200)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-118"><span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**Sprecher \_ Side \_ right** (0x400)</span><span class="sxs-lookup"><span data-stu-id="2962a-118"><span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**SPEAKER\_SIDE\_RIGHT** (0x400)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-119"><span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**Sprecher \_ Top \_ Center** (0x800)</span><span class="sxs-lookup"><span data-stu-id="2962a-119"><span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**SPEAKER\_TOP\_CENTER** (0x800)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-120"><span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**Sprecher \_ Obere \_ Vorder \_** Seite (0x1000)</span><span class="sxs-lookup"><span data-stu-id="2962a-120"><span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**SPEAKER\_TOP\_FRONT\_LEFT** (0x1000)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-121"><span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**Sprecher \_ Top- \_ Front- \_ Center** (0x2000)</span><span class="sxs-lookup"><span data-stu-id="2962a-121"><span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**SPEAKER\_TOP\_FRONT\_CENTER** (0x2000)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-122"><span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**Sprecher \_ Obere \_ Vorder \_** Seite (0x4000)</span><span class="sxs-lookup"><span data-stu-id="2962a-122"><span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**SPEAKER\_TOP\_FRONT\_RIGHT** (0x4000)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-123"><span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**Sprecher \_ Oben \_ \_ Links** (0X8000)</span><span class="sxs-lookup"><span data-stu-id="2962a-123"><span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**SPEAKER\_TOP\_BACK\_LEFT** (0x8000)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-124"><span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**Sprecher \_ Top- \_ Back- \_ Center** (0x10000)</span><span class="sxs-lookup"><span data-stu-id="2962a-124"><span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**SPEAKER\_TOP\_BACK\_CENTER** (0x10000)</span></span>
</dt> <dt>

<span data-ttu-id="2962a-125"><span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**Sprecher \_ Oben \_ \_ Rechts** (0x20000)</span><span class="sxs-lookup"><span data-stu-id="2962a-125"><span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**SPEAKER\_TOP\_BACK\_RIGHT** (0x20000)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2962a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2962a-126">Remarks</span></span>

<span data-ttu-id="2962a-127">Dieses Attribut entspricht dem **dwchannelmask** -Member der [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2962a-127">This attribute corresponds to the **dwChannelMask** member of the [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) structure.</span></span>

<span data-ttu-id="2962a-128">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="2962a-128">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2962a-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2962a-129">Requirements</span></span>



| <span data-ttu-id="2962a-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2962a-130">Requirement</span></span> | <span data-ttu-id="2962a-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2962a-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2962a-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2962a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2962a-133">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2962a-133">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2962a-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2962a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2962a-135">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2962a-135">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2962a-136">Header</span><span class="sxs-lookup"><span data-stu-id="2962a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2962a-137"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2962a-137"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2962a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2962a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2962a-139">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="2962a-139">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2962a-140">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2962a-140">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2962a-141">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2962a-141">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2962a-142">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="2962a-142">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="2962a-143">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="2962a-143">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 

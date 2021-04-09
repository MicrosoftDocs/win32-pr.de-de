---
description: Gibt die maximale Audiobitrate für die DLNA-Medien Senke (Digital Living Network Alliance) an.
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: MF_MP2DLNA_AUDIO_BIT_RATE-Attribut (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c61554f592aefbb863057339d807e23fc96567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959290"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a><span data-ttu-id="584b2-103">MF \_ MP2DLNA \_ \_ \_ Audiobitrate-Attribut</span><span class="sxs-lookup"><span data-stu-id="584b2-103">MF\_MP2DLNA\_AUDIO\_BIT\_RATE attribute</span></span>

<span data-ttu-id="584b2-104">Gibt die maximale Audiobitrate für die DLNA-Medien Senke (Digital Living Network Alliance) an.</span><span class="sxs-lookup"><span data-stu-id="584b2-104">Specifies the maximum audio bit rate for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="584b2-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="584b2-105">Data type</span></span>

<span data-ttu-id="584b2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="584b2-106">**UINT32**</span></span>

<span data-ttu-id="584b2-107">Der Wert ist die maximale Zielbitrate für den codierten Audiostream (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="584b2-107">The value is the target maximum bit rate for the encoded audio stream, in bits per second.</span></span> <span data-ttu-id="584b2-108">Der Wert muss eine der zulässigen Bitraten für das MPEG-2 Layer 2-Audioformat für DLNA sein.</span><span class="sxs-lookup"><span data-stu-id="584b2-108">The value must be one of the bit rates allowed for MPEG-2 layer 2 audio for DLNA.</span></span> <span data-ttu-id="584b2-109">Der Standardwert ist 192000 (192 Kbit/s).</span><span class="sxs-lookup"><span data-stu-id="584b2-109">The default value is 192000 (192 Kbps).</span></span>

## <a name="getset"></a><span data-ttu-id="584b2-110">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="584b2-110">Get/set</span></span>

<span data-ttu-id="584b2-111">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="584b2-111">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="584b2-112">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="584b2-112">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="584b2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="584b2-113">Remarks</span></span>

<span data-ttu-id="584b2-114">Wenn Sie dieses Attribut für die DLNA-Medien Senke festlegen möchten, Fragen Sie die Medien Senke nach der [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="584b2-114">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="584b2-115">Legen Sie das-Attribut vor Beginn des Streamings fest.</span><span class="sxs-lookup"><span data-stu-id="584b2-115">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="584b2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="584b2-116">Requirements</span></span>



| <span data-ttu-id="584b2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="584b2-117">Requirement</span></span> | <span data-ttu-id="584b2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="584b2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="584b2-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="584b2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="584b2-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="584b2-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="584b2-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="584b2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="584b2-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="584b2-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="584b2-123">Header</span><span class="sxs-lookup"><span data-stu-id="584b2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="584b2-124"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="584b2-124"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="584b2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="584b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="584b2-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="584b2-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





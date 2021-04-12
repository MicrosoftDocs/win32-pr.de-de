---
description: Gibt die maximale Video Bitrate für die DLNA-Medien Senke (Digital Living Network Alliance) an.
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: MF_MP2DLNA_VIDEO_BIT_RATE-Attribut (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 503625e6879b202f3fcd1f38bce38ebf48677d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215148"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a><span data-ttu-id="0f835-103">MF \_ MP2DLNA \_ Video \_ \_ Bitrate-Attribut</span><span class="sxs-lookup"><span data-stu-id="0f835-103">MF\_MP2DLNA\_VIDEO\_BIT\_RATE attribute</span></span>

<span data-ttu-id="0f835-104">Gibt die maximale Video Bitrate für die DLNA-Medien Senke (Digital Living Network Alliance) an.</span><span class="sxs-lookup"><span data-stu-id="0f835-104">Specifies the maximum video bit rate for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="0f835-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0f835-105">Data type</span></span>

<span data-ttu-id="0f835-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0f835-106">**UINT32**</span></span>

<span data-ttu-id="0f835-107">Der Wert ist die maximale Zielbitrate für den codierten Videostream (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="0f835-107">The value is the target maximum bit rate for the encoded video stream, in bits per second.</span></span> <span data-ttu-id="0f835-108">Der Höchstwert beträgt 9,8 Millionen (9,8 Mbit/s), der auch der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="0f835-108">The maximum value is 9800000 (9.8 Mbps), which is also the default value.</span></span>

## <a name="getset"></a><span data-ttu-id="0f835-109">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="0f835-109">Get/set</span></span>

<span data-ttu-id="0f835-110">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="0f835-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0f835-111">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="0f835-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f835-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f835-112">Remarks</span></span>

<span data-ttu-id="0f835-113">Wenn Sie dieses Attribut für die DLNA-Medien Senke festlegen möchten, Fragen Sie die Medien Senke nach der [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="0f835-113">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="0f835-114">Legen Sie das-Attribut vor Beginn des Streamings fest.</span><span class="sxs-lookup"><span data-stu-id="0f835-114">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f835-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f835-115">Requirements</span></span>



| <span data-ttu-id="0f835-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f835-116">Requirement</span></span> | <span data-ttu-id="0f835-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0f835-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f835-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f835-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0f835-119">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f835-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0f835-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f835-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0f835-121">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f835-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0f835-122">Header</span><span class="sxs-lookup"><span data-stu-id="0f835-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f835-123"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f835-123"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f835-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f835-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f835-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0f835-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





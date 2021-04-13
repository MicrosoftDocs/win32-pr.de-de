---
description: Gibt für einen Medientyp an, der einen MPEG-2-Transportdaten Strom (TS) beschreibt, gibt an, dass die Transport Pakete einen 4-Byte-Zeit Code enthalten.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: MF_MT_MPEG2_TIMECODE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc9db5d7b3c6e94f7845bec2bd98c569d1b1f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216883"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a><span data-ttu-id="7b36c-103">MF \_ MT-Attribut "- \_ \_ Zeit Leitzahl"</span><span class="sxs-lookup"><span data-stu-id="7b36c-103">MF\_MT\_MPEG2\_TIMECODE attribute</span></span>

<span data-ttu-id="7b36c-104">Gibt für einen Medientyp an, der einen MPEG-2-Transportdaten Strom (TS) beschreibt, gibt an, dass die Transport Pakete einen 4-Byte-Zeit Code enthalten.</span><span class="sxs-lookup"><span data-stu-id="7b36c-104">For a media type that describes an MPEG-2 transport stream (TS), specifies the transport packets contain a 4-byte time code.</span></span>

## <a name="data-type"></a><span data-ttu-id="7b36c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7b36c-105">Data type</span></span>

<span data-ttu-id="7b36c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7b36c-106">**UINT32**</span></span>



| <span data-ttu-id="7b36c-107">Wert</span><span class="sxs-lookup"><span data-stu-id="7b36c-107">Value</span></span>                                                                                                | <span data-ttu-id="7b36c-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7b36c-108">Meaning</span></span>                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="7b36c-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36c-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="7b36c-110">Es wurde kein Zeit Code hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7b36c-110">No time code is added.</span></span><br/>                                                                                                              |
| <span id="1"></span><dl> <span data-ttu-id="7b36c-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="7b36c-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="7b36c-112">Ein 4-Byte-Zeit Code wird zu Beginn jedes Transport Pakets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7b36c-112">A 4-byte time code is added at the start of each transport packet.</span></span> <span data-ttu-id="7b36c-113">Dieser Zeitaufwand wird für einige Digital TV-Standards benötigt.</span><span class="sxs-lookup"><span data-stu-id="7b36c-113">This time code is required by some digital television standards.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7b36c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b36c-114">Requirements</span></span>



| <span data-ttu-id="7b36c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b36c-115">Requirement</span></span> | <span data-ttu-id="7b36c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7b36c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b36c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b36c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7b36c-118">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7b36c-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="7b36c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b36c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7b36c-120">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7b36c-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7b36c-121">Header</span><span class="sxs-lookup"><span data-stu-id="7b36c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b36c-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b36c-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b36c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b36c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b36c-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7b36c-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





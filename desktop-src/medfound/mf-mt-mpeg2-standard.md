---
description: Gibt für einen Medientyp, der einen MPEG-2-Programm Datenstrom (PS) oder einen Transportstream (TS) beschreibt, den Standard an, der zum Durchsuchen des Streams verwendet wird.
ms.assetid: 3D4C1A81-A9BA-427F-93DB-F522A0616EAB
title: MF_MT_MPEG2_STANDARD-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0650a68975f449ea938b41872005e11d79922393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347945"
---
# <a name="mf_mt_mpeg2_standard-attribute"></a><span data-ttu-id="c1c3e-103">MF \_ MT \_ - \_ Standard Attribut</span><span class="sxs-lookup"><span data-stu-id="c1c3e-103">MF\_MT\_MPEG2\_STANDARD attribute</span></span>

<span data-ttu-id="c1c3e-104">Gibt für einen Medientyp, der einen MPEG-2-Programm Datenstrom (PS) oder einen Transportstream (TS) beschreibt, den Standard an, der zum Durchsuchen des Streams verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1c3e-104">For a media type that describes an MPEG-2 program stream (PS) or transport stream (TS), specifies the standard that is used to multiplex the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="c1c3e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c1c3e-105">Data type</span></span>

<span data-ttu-id="c1c3e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c1c3e-106">**UINT32**</span></span>



| <span data-ttu-id="c1c3e-107">Wert</span><span class="sxs-lookup"><span data-stu-id="c1c3e-107">Value</span></span>                                                                                                | <span data-ttu-id="c1c3e-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c1c3e-108">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="c1c3e-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="c1c3e-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="c1c3e-110">Standard-MPEG-2 PS oder TS.</span><span class="sxs-lookup"><span data-stu-id="c1c3e-110">Standard MPEG-2 PS or TS.</span></span><br/>                                       |
| <span id="1"></span><dl> <span data-ttu-id="c1c3e-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c1c3e-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c1c3e-112">Advanced TV Systems Committee (ATSC)-Standard.</span><span class="sxs-lookup"><span data-stu-id="c1c3e-112">Advanced Television Systems Committee (ATSC) standard.</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="c1c3e-113"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c1c3e-113"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c1c3e-114">Digital Video Broadcasting (DVB)-Standard.</span><span class="sxs-lookup"><span data-stu-id="c1c3e-114">Digital Video Broadcasting (DVB) standard.</span></span><br/>                      |
| <span id="3"></span><dl> <span data-ttu-id="c1c3e-115"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c1c3e-115"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c1c3e-116">Zuordnung von Radio Industrie und Unternehmen (ARIB) Standard.</span><span class="sxs-lookup"><span data-stu-id="c1c3e-116">Association of Radio Industries and Businesses (ARIB) standard.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c1c3e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1c3e-117">Requirements</span></span>



| <span data-ttu-id="c1c3e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1c3e-118">Requirement</span></span> | <span data-ttu-id="c1c3e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c1c3e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c3e-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1c3e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c1c3e-121">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c1c3e-121">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c1c3e-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1c3e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c1c3e-123">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c1c3e-123">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c1c3e-124">Header</span><span class="sxs-lookup"><span data-stu-id="c1c3e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1c3e-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1c3e-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1c3e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1c3e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c3e-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c1c3e-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





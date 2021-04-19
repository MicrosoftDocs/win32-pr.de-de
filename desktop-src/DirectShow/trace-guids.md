---
description: Die folgenden GUIDs werden für die Ereignis Ablauf Verfolgung in DirectShow verwendet.
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: Ablauf Verfolgungs-GUIDs (perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AUDIOBREAK
- GUID_DSHOW_CTL
- GUID_STREAMTRACE
- GUID_VIDEOREND
api_type:
- HeaderDef
api_location:
- PerfStruct.h
ms.openlocfilehash: 4b2f2a6a678c029d01d9bf55481837d81d48557e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369202"
---
# <a name="trace-guids"></a><span data-ttu-id="710fc-103">Ablauf Verfolgungs-GUIDs</span><span class="sxs-lookup"><span data-stu-id="710fc-103">Trace GUIDs</span></span>

<span data-ttu-id="710fc-104">Die folgenden GUIDs werden für die Ereignis Ablauf Verfolgung in DirectShow verwendet.</span><span class="sxs-lookup"><span data-stu-id="710fc-104">The following GUIDs are used for event tracing in DirectShow.</span></span>



| <span data-ttu-id="710fc-105">GUID</span><span class="sxs-lookup"><span data-stu-id="710fc-105">GUID</span></span>                                                                                                                                                                   | <span data-ttu-id="710fc-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="710fc-106">Description</span></span>                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <span data-ttu-id="710fc-107"><dt>**GUID- \_ audiobreak**</dt></span><span class="sxs-lookup"><span data-stu-id="710fc-107"><dt>**GUID\_AUDIOBREAK**</dt></span></span> </dl>    | <span data-ttu-id="710fc-108">Audioumbruch-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="710fc-108">Audio break event.</span></span> <span data-ttu-id="710fc-109">Ereignisse dieses Typs verwenden die [**perfinfo \_ DShow \_ audiobreak**](perfinfo-dshow-audiobreak.md) -Struktur für Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="710fc-109">Events of this type use the [**PERFINFO\_DSHOW\_AUDIOBREAK**](perfinfo-dshow-audiobreak.md) structure for event data.</span></span><br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <span data-ttu-id="710fc-110"><dt>**GUID \_ DShow \_ CTL**</dt></span><span class="sxs-lookup"><span data-stu-id="710fc-110"><dt>**GUID\_DSHOW\_CTL**</dt></span></span> </dl>      | <span data-ttu-id="710fc-111">DirectShow-Ereignis Anbieter.</span><span class="sxs-lookup"><span data-stu-id="710fc-111">DirectShow event provider.</span></span><br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <span data-ttu-id="710fc-112"><dt>**GUID- \_ streamtrace**</dt></span><span class="sxs-lookup"><span data-stu-id="710fc-112"><dt>**GUID\_STREAMTRACE**</dt></span></span> </dl> | <span data-ttu-id="710fc-113">Allgemeines streamingereignis.</span><span class="sxs-lookup"><span data-stu-id="710fc-113">General streaming event.</span></span> <span data-ttu-id="710fc-114">Ereignisse dieses Typs verwenden die [**perfinfo \_ DShow \_ streamtrace**](perfinfo-dshow-streamtrace.md) -Struktur für Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="710fc-114">Events of this type use the [**PERFINFO\_DSHOW\_STREAMTRACE**](perfinfo-dshow-streamtrace.md) structure for event data.</span></span><br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <span data-ttu-id="710fc-115"><dt>**GUID- \_ videorend**</dt></span><span class="sxs-lookup"><span data-stu-id="710fc-115"><dt>**GUID\_VIDEOREND**</dt></span></span> </dl>       | <span data-ttu-id="710fc-116">Videorenderingereignis.</span><span class="sxs-lookup"><span data-stu-id="710fc-116">Video rendering event.</span></span> <span data-ttu-id="710fc-117">Ereignisse dieses Typs verwenden die [**perfinfo \_ DShow \_ avrend**](perfinfo-dshow-avrend.md) -Struktur für Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="710fc-117">Events of this type use the [**PERFINFO\_DSHOW\_AVREND**](perfinfo-dshow-avrend.md) structure for event data.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="710fc-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="710fc-118">Requirements</span></span>



| <span data-ttu-id="710fc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="710fc-119">Requirement</span></span> | <span data-ttu-id="710fc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="710fc-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="710fc-121">Header</span><span class="sxs-lookup"><span data-stu-id="710fc-121">Header</span></span><br/> | <dl> <span data-ttu-id="710fc-122"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="710fc-122"><dt>PerfStruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="710fc-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="710fc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="710fc-124">Ereignis Ablauf Verfolgung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="710fc-124">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> </dl>

 

 





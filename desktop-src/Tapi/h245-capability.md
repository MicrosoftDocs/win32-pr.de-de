---
description: Die H245 \_ -funktionsenum beschreibt die Unterstützung für Audioformate und Videoformate.
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: H245_CAPABILITY-Enumeration (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7a6f81f87480f221f87680d9cf086120deb2de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372479"
---
# <a name="h245_capability-enumeration"></a><span data-ttu-id="e020b-103">H245- \_ funktionsenumeration</span><span class="sxs-lookup"><span data-stu-id="e020b-103">H245\_CAPABILITY enumeration</span></span>

<span data-ttu-id="e020b-104">\[**H245 \_ Die Funktion** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e020b-104">\[**H245\_CAPABILITY** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e020b-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="e020b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e020b-106">Die **H245 \_** -funktionsenum beschreibt die Unterstützung für Audioformate und Videoformate.</span><span class="sxs-lookup"><span data-stu-id="e020b-106">The **H245\_CAPABILITY** enum describes audio and video format support.</span></span>

## <a name="syntax"></a><span data-ttu-id="e020b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e020b-107">Syntax</span></span>


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a><span data-ttu-id="e020b-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e020b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e020b-109"><span id="HC_G711"></span><span id="hc_g711"></span>**HC \_ G711**</span><span class="sxs-lookup"><span data-stu-id="e020b-109"><span id="HC_G711"></span><span id="hc_g711"></span>**HC\_G711**</span></span>
</dt> <dd>

<span data-ttu-id="e020b-110">Das G. 711-Audioprotokoll wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e020b-110">The G.711 audio protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="e020b-111"><span id="HC_G723"></span><span id="hc_g723"></span>**HC \_ g723**</span><span class="sxs-lookup"><span data-stu-id="e020b-111"><span id="HC_G723"></span><span id="hc_g723"></span>**HC\_G723**</span></span>
</dt> <dd>

<span data-ttu-id="e020b-112">Das G. 723-Audioprotokoll wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e020b-112">The G.723 audio protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="e020b-113"><span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC \_ H263QCIF**</span><span class="sxs-lookup"><span data-stu-id="e020b-113"><span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC\_H263QCIF**</span></span>
</dt> <dd>

<span data-ttu-id="e020b-114">Das H. 263 Video-Protokoll wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e020b-114">The H.263 video protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="e020b-115"><span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC \_ H261QCIF**</span><span class="sxs-lookup"><span data-stu-id="e020b-115"><span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC\_H261QCIF**</span></span>
</dt> <dd>

<span data-ttu-id="e020b-116">Das H. 263 Video-Protokoll wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e020b-116">The H.263 video protocol is supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e020b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e020b-117">Requirements</span></span>



| <span data-ttu-id="e020b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e020b-118">Requirement</span></span> | <span data-ttu-id="e020b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e020b-119">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e020b-120">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="e020b-120">TAPI version</span></span><br/> | <span data-ttu-id="e020b-121">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e020b-121">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e020b-122">Header</span><span class="sxs-lookup"><span data-stu-id="e020b-122">Header</span></span><br/>       | <dl> <span data-ttu-id="e020b-123"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="e020b-123"><dt>H323priv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e020b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e020b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e020b-125">**IH323LineEx:: setdefaultcapabilityprefergenz**</span><span class="sxs-lookup"><span data-stu-id="e020b-125">**IH323LineEx::SetDefaultCapabilityPreferrence**</span></span>](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 





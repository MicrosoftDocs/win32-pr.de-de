---
title: DRM_HTTP_STATUS-Enumeration (drmexternals. h)
description: Der DRM- \_ http- \_ statusenumerationstyp definiert einen Bereich von Zuständen für eine DRM-Anforderung.
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- DRM_HTTP_STATUS-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d61803cab6cb80932402e429e77228a1611fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339997"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a><span data-ttu-id="27fa1-105">DRM_HTTP_STATUS-Enumeration (drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="27fa1-105">DRM_HTTP_STATUS enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="27fa1-106">Der **DRM- \_ http- \_ statusenumerationstyp** definiert einen Bereich von Zuständen für eine [*DRM*](wmformat-glossary.md) -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="27fa1-106">The **DRM\_HTTP\_STATUS** enumeration type defines a range of states for a [*DRM*](wmformat-glossary.md) request.</span></span>

## <a name="syntax"></a><span data-ttu-id="27fa1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="27fa1-107">Syntax</span></span>


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="27fa1-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="27fa1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="27fa1-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP \_ notinitiierte**</span><span class="sxs-lookup"><span data-stu-id="27fa1-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP\_NOTINITIATED**</span></span>
</dt> <dd>

<span data-ttu-id="27fa1-110">Die http-Vorgänge wurden nicht initiiert.</span><span class="sxs-lookup"><span data-stu-id="27fa1-110">The HTTP operations have not been initiated.</span></span>

</dd> <dt>

<span data-ttu-id="27fa1-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP- \_ Verbindung**</span><span class="sxs-lookup"><span data-stu-id="27fa1-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="27fa1-112">Die Verbindung wird hergestellt.</span><span class="sxs-lookup"><span data-stu-id="27fa1-112">The connection is being established.</span></span>

</dd> <dt>

<span data-ttu-id="27fa1-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="27fa1-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP\_REQUESTING**</span></span>
</dt> <dd>

<span data-ttu-id="27fa1-114">Es werden Daten angefordert.</span><span class="sxs-lookup"><span data-stu-id="27fa1-114">Data is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="27fa1-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP- \_ Empfang**</span><span class="sxs-lookup"><span data-stu-id="27fa1-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP\_RECEIVING**</span></span>
</dt> <dd>

<span data-ttu-id="27fa1-116">Daten werden empfangen.</span><span class="sxs-lookup"><span data-stu-id="27fa1-116">Data is being received.</span></span>

</dd> <dt>

<span data-ttu-id="27fa1-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="27fa1-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="27fa1-118">Die http-Vorgänge sind fertiggestellt.</span><span class="sxs-lookup"><span data-stu-id="27fa1-118">The HTTP operations are complete.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27fa1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27fa1-119">Remarks</span></span>

<span data-ttu-id="27fa1-120">Diese Enumeration wird von der [**WM \_ Individual \_ Status**](wm-individualize-status.md) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="27fa1-120">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="27fa1-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27fa1-121">Requirements</span></span>



| <span data-ttu-id="27fa1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27fa1-122">Requirement</span></span> | <span data-ttu-id="27fa1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="27fa1-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="27fa1-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27fa1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="27fa1-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27fa1-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="27fa1-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27fa1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="27fa1-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27fa1-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="27fa1-128">Version</span><span class="sxs-lookup"><span data-stu-id="27fa1-128">Version</span></span><br/>                  | <span data-ttu-id="27fa1-129">SDK für Windows Media-Format 7 oder höhere Versionen des SDKs</span><span class="sxs-lookup"><span data-stu-id="27fa1-129">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="27fa1-130">Header</span><span class="sxs-lookup"><span data-stu-id="27fa1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="27fa1-131"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="27fa1-131"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27fa1-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27fa1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27fa1-133">**DRM- \_ Individualisierungs \_ Status**</span><span class="sxs-lookup"><span data-stu-id="27fa1-133">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drm-individualization-status.md)
</dt> <dt>

[<span data-ttu-id="27fa1-134">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="27fa1-134">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 






---
title: DRM_HTTP_STATUS-Enumeration (wmdrmsdk. h)
description: Der DRM- \_ http- \_ statusenumerationstyp definiert einen Bereich von http-Zuständen für eine DRM-Anforderung.
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- DRM_HTTP_STATUS-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c5a40af45fd573f7f5033b9be3b037079cb30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356045"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a><span data-ttu-id="861be-105">DRM_HTTP_STATUS-Enumeration (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="861be-105">DRM_HTTP_STATUS enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="861be-106">Der **DRM- \_ http- \_ statusenumerationstyp** definiert einen Bereich von http-Zuständen für eine DRM-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="861be-106">The **DRM\_HTTP\_STATUS** enumeration type defines a range of HTTP states for a DRM request.</span></span>

## <a name="syntax"></a><span data-ttu-id="861be-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="861be-107">Syntax</span></span>


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="861be-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="861be-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="861be-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP \_ notinitiierte**</span><span class="sxs-lookup"><span data-stu-id="861be-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP\_NOTINITIATED**</span></span>
</dt> <dd>

<span data-ttu-id="861be-110">Die http-Vorgänge wurden nicht initiiert.</span><span class="sxs-lookup"><span data-stu-id="861be-110">The HTTP operations have not been initiated.</span></span>

</dd> <dt>

<span data-ttu-id="861be-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP- \_ Verbindung**</span><span class="sxs-lookup"><span data-stu-id="861be-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="861be-112">Die Verbindung wird hergestellt.</span><span class="sxs-lookup"><span data-stu-id="861be-112">The connection is being established.</span></span>

</dd> <dt>

<span data-ttu-id="861be-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="861be-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP\_REQUESTING**</span></span>
</dt> <dd>

<span data-ttu-id="861be-114">Es werden Daten angefordert.</span><span class="sxs-lookup"><span data-stu-id="861be-114">Data is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="861be-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP- \_ Empfang**</span><span class="sxs-lookup"><span data-stu-id="861be-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP\_RECEIVING**</span></span>
</dt> <dd>

<span data-ttu-id="861be-116">Daten werden empfangen.</span><span class="sxs-lookup"><span data-stu-id="861be-116">Data is being received.</span></span>

</dd> <dt>

<span data-ttu-id="861be-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="861be-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="861be-118">Die http-Vorgänge sind fertiggestellt.</span><span class="sxs-lookup"><span data-stu-id="861be-118">The HTTP operations are complete.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="861be-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="861be-119">Remarks</span></span>

<span data-ttu-id="861be-120">Diese Enumeration wird von der [**WM \_ Individual \_ Status**](drmwm-individualize-status.md) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="861be-120">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="861be-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="861be-121">Requirements</span></span>



| <span data-ttu-id="861be-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="861be-122">Requirement</span></span> | <span data-ttu-id="861be-123">Wert</span><span class="sxs-lookup"><span data-stu-id="861be-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="861be-124">Header</span><span class="sxs-lookup"><span data-stu-id="861be-124">Header</span></span><br/> | <dl> <span data-ttu-id="861be-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="861be-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="861be-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="861be-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="861be-127">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="861be-127">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 






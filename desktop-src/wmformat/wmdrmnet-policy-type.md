---
title: WMDRMNET_POLICY_TYPE-Enumeration (wmdrmsdk. h)
description: Der Enumerationstyp wmdrmnet- \_ \_ Richtlinientyp listet die Typen von Richtlinien auf, die für Windows Media DRM für Netzwerkgeräte Vorgänge verfügbar sind.
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- WMDRMNET_POLICY_TYPE-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964a3e938caa312f02f21074f046f3cf88d72de6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365710"
---
# <a name="wmdrmnet_policy_type-enumeration"></a><span data-ttu-id="bf82f-105">Wmdrmnet \_ - \_ Richtlinientyp-Enumeration</span><span class="sxs-lookup"><span data-stu-id="bf82f-105">WMDRMNET\_POLICY\_TYPE enumeration</span></span>

<span data-ttu-id="bf82f-106">Der Enumerationstyp **wmdrmnet- \_ \_ Richtlinientyp** listet die Typen von Richtlinien auf, die für Windows Media DRM für Netzwerkgeräte Vorgänge verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="bf82f-106">The **WMDRMNET\_POLICY\_TYPE** enumeration type lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf82f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf82f-107">Syntax</span></span>


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a><span data-ttu-id="bf82f-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="bf82f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bf82f-109"><span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**wmdrmnet \_ - \_ Richtlinientyp nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="bf82f-109"><span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**WMDRMNET\_POLICY\_TYPE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="bf82f-110">Nicht definierte Richtlinien Typen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bf82f-110">Undefined policy types are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="bf82f-111"><span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**wmdrmnet \_ - \_ Richtlinientyp \_ transryptplay**</span><span class="sxs-lookup"><span data-stu-id="bf82f-111"><span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**WMDRMNET\_POLICY\_TYPE\_TRANSCRYPTPLAY**</span></span>
</dt> <dd>

<span data-ttu-id="bf82f-112">Die Richtlinie steuert die Fähigkeit zum Konvertieren von Inhalten, die von Windows Media DRM geschützt werden, in geschützte Windows Media DRM für Netzwerkgeräte Daten und die Wiedergabe auf einem vernetzten Gerät.</span><span class="sxs-lookup"><span data-stu-id="bf82f-112">The policy governs the ability to convert content protected by Windows Media DRM into protected Windows Media DRM for Network Devices data and play it back on a networked device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf82f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf82f-113">Remarks</span></span>

<span data-ttu-id="bf82f-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="bf82f-114">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf82f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf82f-115">Requirements</span></span>



| <span data-ttu-id="bf82f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf82f-116">Requirement</span></span> | <span data-ttu-id="bf82f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bf82f-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf82f-118">Header</span><span class="sxs-lookup"><span data-stu-id="bf82f-118">Header</span></span><br/> | <dl> <span data-ttu-id="bf82f-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf82f-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf82f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf82f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf82f-121">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="bf82f-121">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="bf82f-122">**wmdrmnet- \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="bf82f-122">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 






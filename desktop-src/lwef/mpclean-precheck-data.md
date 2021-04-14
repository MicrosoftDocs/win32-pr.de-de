---
title: MPCLEAN_PRECHECK_DATA Struktur (mpclient. h)
description: Benachrichtigungs Daten wurden an eine Clean Vorüberprüfung-Rückruffunktion übermittelt.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- MPCLEAN_PRECHECK_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPCLEAN_PRECHECK_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPCLEAN_PRECHECK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3d67e0c71c95db49b633feeb3048cc9f104b2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476116"
---
# <a name="mpclean_precheck_data-structure"></a><span data-ttu-id="e647f-105">Mpclean- \_ \_ Datenstruktur (Precheck)</span><span class="sxs-lookup"><span data-stu-id="e647f-105">MPCLEAN\_PRECHECK\_DATA structure</span></span>

<span data-ttu-id="e647f-106">Benachrichtigungs Daten wurden an eine Clean Vorüberprüfung-Rückruffunktion übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e647f-106">Notification data passed to clean precheck callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e647f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e647f-107">Syntax</span></span>


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a><span data-ttu-id="e647f-108">Member</span><span class="sxs-lookup"><span data-stu-id="e647f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e647f-109">**Blockedresourceingefo**</span><span class="sxs-lookup"><span data-stu-id="e647f-109">**BlockedResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="e647f-110">Typ: **pmpresource- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="e647f-110">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="e647f-111">Ressourcen Informationen über die Ressource, die blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="e647f-111">Resource information about the resource being blocked.</span></span> <span data-ttu-id="e647f-112">Wenn der Status z. b. auf **mpnotify \_ Precheck- \_ Ressource \_ blockiert** ist.</span><span class="sxs-lookup"><span data-stu-id="e647f-112">For example, when progress is **MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**.</span></span> <span data-ttu-id="e647f-113">Informationen finden Sie unter [**mpresource- \_ Informationen**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="e647f-113">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="e647f-114">**Informationen zu pmpresource \_**</span><span class="sxs-lookup"><span data-stu-id="e647f-114">**PMPRESOURCE\_INFO**</span></span>
</dt> <dd>

<span data-ttu-id="e647f-115">Typ: **blockingresourceinfo**</span><span class="sxs-lookup"><span data-stu-id="e647f-115">Type: **BlockingResourceInfo**</span></span>

</dd> <dd>

<span data-ttu-id="e647f-116">Ressourcen Informationen über die Ressource, die blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="e647f-116">Resource information about the resource that is blocking.</span></span> <span data-ttu-id="e647f-117">Wenn der Status z. b. auf **mpnotify \_ Precheck- \_ Ressource \_ blockiert** ist.</span><span class="sxs-lookup"><span data-stu-id="e647f-117">For example, when progress is **MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**.</span></span> <span data-ttu-id="e647f-118">Informationen finden Sie unter [**mpresource- \_ Informationen**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="e647f-118">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e647f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e647f-119">Requirements</span></span>



| <span data-ttu-id="e647f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e647f-120">Requirement</span></span> | <span data-ttu-id="e647f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e647f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e647f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e647f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e647f-123">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e647f-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e647f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e647f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e647f-125">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e647f-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e647f-126">Header</span><span class="sxs-lookup"><span data-stu-id="e647f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e647f-127"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e647f-127"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e647f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e647f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e647f-129">**mpresource- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="e647f-129">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> </dl>

 

 






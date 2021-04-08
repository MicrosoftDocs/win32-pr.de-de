---
title: MPSCAN_RESOURCES Struktur (mpclient. h)
description: Während eines Scanvorgangs übergebenen Ressourcen Informationen.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- MPSCAN_RESOURCES Struktur Funktionen der Legacy-Windows-Umgebung
- PMPSCAN_RESOURCES Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSCAN_RESOURCES
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ee9ea259bca6bf66eb81fcd17b13d509d5a065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957195"
---
# <a name="mpscan_resources-structure"></a><span data-ttu-id="a1f07-105">Mpscan- \_ Ressourcenstruktur</span><span class="sxs-lookup"><span data-stu-id="a1f07-105">MPSCAN\_RESOURCES structure</span></span>

<span data-ttu-id="a1f07-106">Während eines Scanvorgangs übergebenen Ressourcen Informationen.</span><span class="sxs-lookup"><span data-stu-id="a1f07-106">Resource information passed during a scan operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f07-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1f07-107">Syntax</span></span>


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a><span data-ttu-id="a1f07-108">Member</span><span class="sxs-lookup"><span data-stu-id="a1f07-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1f07-109">**dwresourcecount**</span><span class="sxs-lookup"><span data-stu-id="a1f07-109">**dwResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="a1f07-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a1f07-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a1f07-111">Anzahl der Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a1f07-111">Count of resources.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-112">**präsourcelist**</span><span class="sxs-lookup"><span data-stu-id="a1f07-112">**pResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="a1f07-113">Typ: **pmpresource- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="a1f07-113">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="a1f07-114">Array von Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a1f07-114">Array of resources.</span></span> <span data-ttu-id="a1f07-115">Informationen finden Sie unter [**mpresource- \_ Informationen**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="a1f07-115">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1f07-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1f07-116">Requirements</span></span>



| <span data-ttu-id="a1f07-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1f07-117">Requirement</span></span> | <span data-ttu-id="a1f07-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a1f07-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f07-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1f07-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a1f07-120">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1f07-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a1f07-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1f07-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a1f07-122">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1f07-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1f07-123">Header</span><span class="sxs-lookup"><span data-stu-id="a1f07-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1f07-124"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1f07-124"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1f07-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1f07-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f07-126">**mpresource- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="a1f07-126">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> </dl>

 

 






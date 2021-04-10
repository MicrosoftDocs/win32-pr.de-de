---
title: Swarmstatus-Enumeration (deliveryoptimization. h)
description: Definiert den Status einer Datei innerhalb des Bereitstellungs Optimierungs Clients.
ms.assetid: D40ABDD3-5573-4A8D-8608-4CB0F396CCAD
keywords:
- Swarmstatus-Enumeration
topic_type:
- apiref
api_name:
- SwarmStatus
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3622f819679c2fd2b28d66e371a8b88e0a2d2f70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105320"
---
# <a name="swarmstatus-enumeration"></a><span data-ttu-id="9d9fc-104">Swarmstatus-Enumeration</span><span class="sxs-lookup"><span data-stu-id="9d9fc-104">SwarmStatus enumeration</span></span>

<span data-ttu-id="9d9fc-105">Definiert den Status einer Datei innerhalb des Bereitstellungs Optimierungs Clients.</span><span class="sxs-lookup"><span data-stu-id="9d9fc-105">Defines the status of a file within the delivery optimization client.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d9fc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d9fc-106">Syntax</span></span>


```C++
typedef enum _SwarmStatus { 
  SwarmStatus_Downloading  = 0,
  SwarmStatus_Complete     = 1,
  SwarmStatus_Caching      = 2,
  SwarmStatus_Paused       = 3
} SwarmStatus;
```



## <a name="constants"></a><span data-ttu-id="9d9fc-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="9d9fc-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9d9fc-108"><span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**</span><span class="sxs-lookup"><span data-stu-id="9d9fc-108"><span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**</span></span>
</dt> <dd>

<span data-ttu-id="9d9fc-109">Die Datei wird heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="9d9fc-109">The file is downloading.</span></span>

</dd> <dt>

<span data-ttu-id="9d9fc-110"><span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**</span><span class="sxs-lookup"><span data-stu-id="9d9fc-110"><span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**</span></span>
</dt> <dd>

<span data-ttu-id="9d9fc-111">Der Datei Download ist fertiggestellt.</span><span class="sxs-lookup"><span data-stu-id="9d9fc-111">The file download is complete.</span></span>

</dd> <dt>

<span data-ttu-id="9d9fc-112"><span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**</span><span class="sxs-lookup"><span data-stu-id="9d9fc-112"><span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**</span></span>
</dt> <dd>

<span data-ttu-id="9d9fc-113">Die Datei wird zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="9d9fc-113">The file is being cached.</span></span>

</dd> <dt>

<span data-ttu-id="9d9fc-114"><span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**</span><span class="sxs-lookup"><span data-stu-id="9d9fc-114"><span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**</span></span>
</dt> <dd>

<span data-ttu-id="9d9fc-115">Der Datei Download wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="9d9fc-115">The file download is paused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d9fc-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d9fc-116">Requirements</span></span>



| <span data-ttu-id="9d9fc-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d9fc-117">Requirement</span></span> | <span data-ttu-id="9d9fc-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9d9fc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d9fc-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d9fc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9d9fc-120">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d9fc-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9d9fc-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d9fc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9d9fc-122">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d9fc-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9d9fc-123">Header</span><span class="sxs-lookup"><span data-stu-id="9d9fc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d9fc-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d9fc-124"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 






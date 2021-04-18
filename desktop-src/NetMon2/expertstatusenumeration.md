---
description: Die expertstatusenumeration-Enumeration enthält Statuswerte. Sie wird vom Status-Member der Expertenstatus-Struktur und vom Status-Parameter in "Expertenstatus" verwendet.
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: Expertstatus usenumeration-Enumeration (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERT_STATUS_ENUMERATION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b634d4dad2e024c3c995216b5af7de23b14b7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345004"
---
# <a name="expertstatusenumeration-enumeration"></a><span data-ttu-id="77d28-104">Expertstatus usenumeration-Enumeration</span><span class="sxs-lookup"><span data-stu-id="77d28-104">EXPERTSTATUSENUMERATION enumeration</span></span>

<span data-ttu-id="77d28-105">Die **expertstatusenumeration** -Enumeration enthält Statuswerte.</span><span class="sxs-lookup"><span data-stu-id="77d28-105">The **EXPERTSTATUSENUMERATION** enumeration contains status values.</span></span> <span data-ttu-id="77d28-106">Sie wird vom **Status** -Member der [Expertenstatus](expertstatus.md) -Struktur und vom *Status* - [Parameter in "Expertenstatus"](expertindicatestatus.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="77d28-106">It is used by the **Status** member of [EXPERTSTATUS](expertstatus.md) structure and the *Status* parameter in [ExpertIndicateStatus](expertindicatestatus.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="77d28-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="77d28-107">Syntax</span></span>


```C++
typedef enum  { 
  EXPERTSTATUS_INACTIVE  = 0,
  EXPERTSTATUS_STARTING,
  EXPERTSTATUS_RUNNING,
  EXPERTSTATUS_PROBLEM,
  EXPERTSTATUS_ABORTED,
  EXPERTSTATUS_DONE
} EXPERT_STATUS_ENUMERATION;
```



## <a name="constants"></a><span data-ttu-id="77d28-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="77d28-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="77d28-109"><span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**Profil Status \_ inaktiv**</span><span class="sxs-lookup"><span data-stu-id="77d28-109"><span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS\_INACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="77d28-110">Der Experte wurde nie gestartet.</span><span class="sxs-lookup"><span data-stu-id="77d28-110">The expert never started.</span></span>

</dd> <dt>

<span data-ttu-id="77d28-111"><span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**Profil Status wird \_ gestartet**</span><span class="sxs-lookup"><span data-stu-id="77d28-111"><span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**EXPERTSTATUS\_STARTING**</span></span>
</dt> <dd>

<span data-ttu-id="77d28-112">Der Experte wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="77d28-112">The expert is starting.</span></span>

</dd> <dt>

<span data-ttu-id="77d28-113"><span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**Profil Status wird \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="77d28-113"><span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="77d28-114">Der Experte wird normal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77d28-114">The expert is running normally.</span></span>

</dd> <dt>

<span data-ttu-id="77d28-115"><span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**expertstatus- \_ Problem**</span><span class="sxs-lookup"><span data-stu-id="77d28-115"><span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**EXPERTSTATUS\_PROBLEM**</span></span>
</dt> <dd>

<span data-ttu-id="77d28-116">Der Experte hat ein im *unter Status* angegebenes Problem beendet.</span><span class="sxs-lookup"><span data-stu-id="77d28-116">A problem specified in *SubStatus* stopped the expert.</span></span>

</dd> <dt>

<span data-ttu-id="77d28-117"><span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**der Expertenstatus wurde \_ abgebrochen.**</span><span class="sxs-lookup"><span data-stu-id="77d28-117"><span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="77d28-118">Netzwerkmonitor den Experten beendet.</span><span class="sxs-lookup"><span data-stu-id="77d28-118">Network Monitor stopped the expert.</span></span>

</dd> <dt>

<span data-ttu-id="77d28-119"><span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**Profil Status \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="77d28-119"><span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS\_DONE**</span></span>
</dt> <dd>

<span data-ttu-id="77d28-120">Der Experte wurde erfolgreich beendet.</span><span class="sxs-lookup"><span data-stu-id="77d28-120">The expert finished successfully.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77d28-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77d28-121">Requirements</span></span>



| <span data-ttu-id="77d28-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77d28-122">Requirement</span></span> | <span data-ttu-id="77d28-123">Wert</span><span class="sxs-lookup"><span data-stu-id="77d28-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="77d28-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77d28-124">Minimum supported client</span></span><br/> | <span data-ttu-id="77d28-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77d28-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="77d28-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77d28-126">Minimum supported server</span></span><br/> | <span data-ttu-id="77d28-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77d28-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="77d28-128">Header</span><span class="sxs-lookup"><span data-stu-id="77d28-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="77d28-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="77d28-129"><dt>Netmon.h</dt></span></span> </dl> |



 

 





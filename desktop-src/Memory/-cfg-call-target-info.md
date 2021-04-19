---
description: Stellt Informationen über callziele für den Ablauf Steuerungs Schutz (Control Flow Guard, cfg) dar.
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: CFG_CALL_TARGET_INFO Struktur (ntmmapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359025"
---
# <a name="cfg_call_target_info-structure"></a><span data-ttu-id="7de91-103">CFG \_ - \_ Aufrufziel- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="7de91-103">CFG\_CALL\_TARGET\_INFO structure</span></span>

<span data-ttu-id="7de91-104">Stellt Informationen über callziele für den Ablauf Steuerungs Schutz (Control Flow Guard, cfg) dar.</span><span class="sxs-lookup"><span data-stu-id="7de91-104">Represents information about call targets for Control Flow Guard (CFG).</span></span>

## <a name="syntax"></a><span data-ttu-id="7de91-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7de91-105">Syntax</span></span>


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a><span data-ttu-id="7de91-106">Member</span><span class="sxs-lookup"><span data-stu-id="7de91-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7de91-107">**Offset**</span><span class="sxs-lookup"><span data-stu-id="7de91-107">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="7de91-108">Offset relativ zu einer angegebenen (Start-) virtuellen Adresse.</span><span class="sxs-lookup"><span data-stu-id="7de91-108">Offset relative to a provided (start) virtual address.</span></span> <span data-ttu-id="7de91-109">Dieser Offset sollte 16 Byte ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="7de91-109">This offset should be 16 byte aligned.</span></span>

</dd> <dt>

<span data-ttu-id="7de91-110">**Flags**</span><span class="sxs-lookup"><span data-stu-id="7de91-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="7de91-111">Flags, die den Vorgang beschreiben, der für die Adresse ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7de91-111">Flags describing the operation to be performed on the address.</span></span> <span data-ttu-id="7de91-112">Wenn das **cfg- \_ \_ Aufrufziel \_ gültig** ist, wird die Adresse für cfg als gültig gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7de91-112">If **CFG\_CALL\_TARGET\_VALID** is set, then the address will be marked valid for CFG.</span></span> <span data-ttu-id="7de91-113">Andernfalls wird er als ungültiges aufrufsziel gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7de91-113">Otherwise, it will be marked an invalid call target.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7de91-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7de91-114">Requirements</span></span>



| <span data-ttu-id="7de91-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7de91-115">Requirement</span></span> | <span data-ttu-id="7de91-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7de91-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7de91-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7de91-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7de91-118">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7de91-118">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7de91-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7de91-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7de91-120">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7de91-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7de91-121">Header</span><span class="sxs-lookup"><span data-stu-id="7de91-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7de91-122"><dt>Ntmmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7de91-122"><dt>Ntmmapi.h</dt></span></span> </dl> |



 

 





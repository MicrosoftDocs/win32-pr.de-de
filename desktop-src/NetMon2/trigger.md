---
description: Die triggerstruktur zeigt eine Aktion an, die vom Treiber zu einem bestimmten Zeitpunkt ausgeführt werden soll.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: Auslöse Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TRIGGER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d9b385557e3c34bdf75f2bf959d4e5e3e47e0750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349592"
---
# <a name="trigger-structure"></a><span data-ttu-id="dc7ca-103">Auslöse Struktur</span><span class="sxs-lookup"><span data-stu-id="dc7ca-103">TRIGGER structure</span></span>

<span data-ttu-id="dc7ca-104">Die **triggerstruktur** zeigt eine Aktion an, die vom Treiber zu einem bestimmten Zeitpunkt ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc7ca-104">The **TRIGGER** structure indicates an action to be taken by the driver at a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc7ca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc7ca-105">Syntax</span></span>


```C++
typedef struct _TRIGGER {
  BOOL         TriggerActive;
  BYTE         TriggerType;
  BYTE         TriggerAction;
  DWORD        TriggerFlags;
  PATTERNMATCH TriggerPatternMatch;
  DWORD        TriggerBufferSize;
  DWORD        Reserved;
} TRIGGER, *LPTRIGGER;
```



## <a name="members"></a><span data-ttu-id="dc7ca-106">Member</span><span class="sxs-lookup"><span data-stu-id="dc7ca-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc7ca-107">**Triggeractive**</span><span class="sxs-lookup"><span data-stu-id="dc7ca-107">**TriggerActive**</span></span>
</dt> <dd>

<span data-ttu-id="dc7ca-108">Ein boolescher Wert, der bestimmt, ob der-Treiber dem Treiber Aufmerksamkeit geschenkt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="dc7ca-108">A Boolean value that determines if the trigger should be paid attention to by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="dc7ca-109">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="dc7ca-109">**TriggerType**</span></span>
</dt> <dd>

<span data-ttu-id="dc7ca-110">Der OP-Code des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="dc7ca-110">The op code of the trigger.</span></span>

</dd> <dt>

<span data-ttu-id="dc7ca-111">**TriggerAction**</span><span class="sxs-lookup"><span data-stu-id="dc7ca-111">**TriggerAction**</span></span>
</dt> <dd>

<span data-ttu-id="dc7ca-112">Aktion, die der-Triggervorgang ausführen soll, wenn er ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="dc7ca-112">Action that the trigger is to take if it is fired.</span></span>

</dd> <dt>

<span data-ttu-id="dc7ca-113">**Triggerflags**</span><span class="sxs-lookup"><span data-stu-id="dc7ca-113">**TriggerFlags**</span></span>
</dt> <dd>

<span data-ttu-id="dc7ca-114">Auslöserflags.</span><span class="sxs-lookup"><span data-stu-id="dc7ca-114">Trigger flags.</span></span>

</dd> <dt>

<span data-ttu-id="dc7ca-115">**Triggerpatternmatch**</span><span class="sxs-lookup"><span data-stu-id="dc7ca-115">**TriggerPatternMatch**</span></span>
</dt> <dd>

<span data-ttu-id="dc7ca-116">Die auslösende Muster Übereinstimmung</span><span class="sxs-lookup"><span data-stu-id="dc7ca-116">The trigger pattern match.</span></span>

</dd> <dt>

<span data-ttu-id="dc7ca-117">**Triggerbuffersize**</span><span class="sxs-lookup"><span data-stu-id="dc7ca-117">**TriggerBufferSize**</span></span>
</dt> <dd>

<span data-ttu-id="dc7ca-118">Puffergröße des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="dc7ca-118">Trigger buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="dc7ca-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="dc7ca-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="dc7ca-120">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="dc7ca-120">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc7ca-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc7ca-121">Requirements</span></span>



| <span data-ttu-id="dc7ca-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc7ca-122">Requirement</span></span> | <span data-ttu-id="dc7ca-123">Wert</span><span class="sxs-lookup"><span data-stu-id="dc7ca-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dc7ca-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc7ca-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dc7ca-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc7ca-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dc7ca-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc7ca-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dc7ca-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc7ca-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dc7ca-128">Header</span><span class="sxs-lookup"><span data-stu-id="dc7ca-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc7ca-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc7ca-129"><dt>Netmon.h</dt></span></span> </dl> |



 

 





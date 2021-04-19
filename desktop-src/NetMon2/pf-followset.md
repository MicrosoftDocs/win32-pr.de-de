---
description: Die PF-nach \_ Verfolgungs Struktur definiert die Protokolle, die möglicherweise vor oder nach einem Protokoll stehen.
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: PF_FOLLOWSET Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f5c286d3b137df24f7da7f0fc5ae269a7a3d946d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373136"
---
# <a name="pf_followset-structure"></a><span data-ttu-id="07527-103">PF-nach Verfolgungs \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="07527-103">PF\_FOLLOWSET structure</span></span>

<span data-ttu-id="07527-104">Die **PF \_** -nach Verfolgungs Struktur definiert die Protokolle, die möglicherweise vor oder nach einem Protokoll stehen.</span><span class="sxs-lookup"><span data-stu-id="07527-104">The **PF\_FOLLOWSET** structure defines the protocols that may precede or follow a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="07527-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07527-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWSET {
  DWORD          nEntries;
  PF_FOLLOWENTRY Entry[];
} PF_FOLLOWSET, *PPF_FOLLOWSET;
```



## <a name="members"></a><span data-ttu-id="07527-106">Member</span><span class="sxs-lookup"><span data-stu-id="07527-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="07527-107">**nentries**</span><span class="sxs-lookup"><span data-stu-id="07527-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="07527-108">Anzahl der Protokolle in der Liste.</span><span class="sxs-lookup"><span data-stu-id="07527-108">Number of protocols in the list.</span></span>

</dd> <dt>

<span data-ttu-id="07527-109">**Eingabe**</span><span class="sxs-lookup"><span data-stu-id="07527-109">**Entry**</span></span>
</dt> <dd>

<span data-ttu-id="07527-110">[ \_ Ein](pf-followentry.md) Array von PF-nach Verfolgungs Strukturen, die die einzelnen Protokolle beschreiben.</span><span class="sxs-lookup"><span data-stu-id="07527-110">Array of [PF\_FOLLOWENTRY](pf-followentry.md) structures that describe each protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07527-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07527-111">Remarks</span></span>

<span data-ttu-id="07527-112">Die [PF \_ parserinfo](pf-parserinfo.md) -Struktur verwendet die PF-nach Verfolgungs Struktur, um die Protokolle aufzulisten, die möglicherweise dem vom Parser erkannten Protokoll vorangestellt sind. **\_**</span><span class="sxs-lookup"><span data-stu-id="07527-112">The [PF\_PARSERINFO](pf-parserinfo.md) structure uses the **PF\_FOLLOWSET** structure to list the protocols that may precede or follow the protocol that the parser detects.</span></span>

<span data-ttu-id="07527-113">In Netzwerkmonitor werden die Informationen in der **PF- \_ nachfolg** enden Struktur verwendet, um die folgenden Sätze spezifischer Parser zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="07527-113">Network Monitor uses the information in the **PF\_FOLLOWSET** structure to update the follow sets of specific parsers.</span></span> <span data-ttu-id="07527-114">Die PF-nach Verfolgungs Struktur muss mithilfe von **heapzuw** zugeordnet werden. **\_**</span><span class="sxs-lookup"><span data-stu-id="07527-114">The **PF\_FOLLOWSET** structure must be allocated using **HeapAlloc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="07527-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07527-115">Requirements</span></span>



| <span data-ttu-id="07527-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07527-116">Requirement</span></span> | <span data-ttu-id="07527-117">Wert</span><span class="sxs-lookup"><span data-stu-id="07527-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="07527-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07527-118">Minimum supported client</span></span><br/> | <span data-ttu-id="07527-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07527-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="07527-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07527-120">Minimum supported server</span></span><br/> | <span data-ttu-id="07527-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07527-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="07527-122">Header</span><span class="sxs-lookup"><span data-stu-id="07527-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="07527-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="07527-123"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07527-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07527-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07527-125">PF-nach \_ Verfolgung</span><span class="sxs-lookup"><span data-stu-id="07527-125">PF\_FOLLOWENTRY</span></span>](pf-followentry.md)
</dt> <dt>

[<span data-ttu-id="07527-126">PF-Parameter \_ Info</span><span class="sxs-lookup"><span data-stu-id="07527-126">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> </dl>

 

 





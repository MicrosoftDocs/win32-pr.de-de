---
description: Die PF- \_ handoffset-Struktur definiert die Protokolle, die an den Parser übergeben werden, oder die Protokolle, an die der Parser übergibt.
ms.assetid: 2fda399d-a09e-47b4-bb2e-95996de9f950
title: PF_HANDOFFSET Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1b5dc9620f3b1860b27af973432aa4218c05b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368041"
---
# <a name="pf_handoffset-structure"></a><span data-ttu-id="8edff-103">PF- \_ handoffset-Struktur</span><span class="sxs-lookup"><span data-stu-id="8edff-103">PF\_HANDOFFSET structure</span></span>

<span data-ttu-id="8edff-104">Die **PF- \_ handoffset** -Struktur definiert die Protokolle, die an den Parser übergeben werden, oder die Protokolle, an die der Parser übergibt.</span><span class="sxs-lookup"><span data-stu-id="8edff-104">The **PF\_HANDOFFSET** structure defines the protocols that hand off to the parser, or the protocols that the parser hands off to.</span></span>

## <a name="syntax"></a><span data-ttu-id="8edff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8edff-105">Syntax</span></span>


```C++
typedef struct _PF_HANDOFFSET {
  DWORD           nEntries;
  PF_HANDOFFENTRY Entry[];
} PF_HANDOFFSET, *PPF_HANDOFFSET;
```



## <a name="members"></a><span data-ttu-id="8edff-106">Member</span><span class="sxs-lookup"><span data-stu-id="8edff-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8edff-107">**nentries**</span><span class="sxs-lookup"><span data-stu-id="8edff-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="8edff-108">Anzahl von Protokollen.</span><span class="sxs-lookup"><span data-stu-id="8edff-108">Number of protocols.</span></span>

</dd> <dt>

<span data-ttu-id="8edff-109">**Eingabe**</span><span class="sxs-lookup"><span data-stu-id="8edff-109">**Entry**</span></span>
</dt> <dd>

<span data-ttu-id="8edff-110">Ein Array von [PF- \_ handoffentry](pf-handoffentry.md) -Strukturen, die jedes Protokoll definieren.</span><span class="sxs-lookup"><span data-stu-id="8edff-110">An array of [PF\_HANDOFFENTRY](pf-handoffentry.md) structures that define each protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8edff-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8edff-111">Remarks</span></span>

<span data-ttu-id="8edff-112">Die [PF \_](pf-parserinfo.md) -Parameter Info-Struktur verwendet die **PF- \_ handoffset** -Struktur, um Folgendes aufzulisten:</span><span class="sxs-lookup"><span data-stu-id="8edff-112">The [PF\_PARSERINFO](pf-parserinfo.md) structure uses the **PF\_HANDOFFSET** structure to list the following:</span></span>

-   <span data-ttu-id="8edff-113">Die Protokolle, die an den Parser übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8edff-113">Which protocols hand off to the parser.</span></span>
-   <span data-ttu-id="8edff-114">Die Protokolle, an die der Parser übergibt.</span><span class="sxs-lookup"><span data-stu-id="8edff-114">Which protocols the parser hands off to.</span></span>

<span data-ttu-id="8edff-115">Die **PF- \_ handoffset** -Struktur muss mithilfe von **heapzuzuordnungs** zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="8edff-115">The **PF\_HANDOFFSET** structure must be allocated using **HeapAlloc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8edff-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8edff-116">Requirements</span></span>



| <span data-ttu-id="8edff-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8edff-117">Requirement</span></span> | <span data-ttu-id="8edff-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8edff-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8edff-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8edff-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8edff-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8edff-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8edff-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8edff-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8edff-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8edff-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8edff-123">Header</span><span class="sxs-lookup"><span data-stu-id="8edff-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8edff-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8edff-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8edff-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8edff-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8edff-126">PF-Parameter \_ Info</span><span class="sxs-lookup"><span data-stu-id="8edff-126">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> <dt>

[<span data-ttu-id="8edff-127">PF- \_ handoffentry</span><span class="sxs-lookup"><span data-stu-id="8edff-127">PF\_HANDOFFENTRY</span></span>](pf-handoffentry.md)
</dt> </dl>

 

 





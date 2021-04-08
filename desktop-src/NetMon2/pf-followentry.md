---
description: Die PF- \_ nach Verfolgungs Struktur definiert ein Protokoll, das Netzwerkmonitor dem nachfolgenden Satz eines Parsers hinzufügt.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: PF_FOLLOWENTRY Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f93ec4784fc8d0f92f68fdff3914e230ffd3cdce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866263"
---
# <a name="pf_followentry-structure"></a><span data-ttu-id="0fb89-103">PF-nach Verfolgungs \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="0fb89-103">PF\_FOLLOWENTRY structure</span></span>

<span data-ttu-id="0fb89-104">Die **PF \_** -nach Verfolgungs Struktur definiert ein Protokoll, das Netzwerkmonitor dem nachfolgenden Satz eines Parsers hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="0fb89-104">The **PF\_FOLLOWENTRY** structure defines a protocol that Network Monitor adds to the follow set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fb89-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fb89-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a><span data-ttu-id="0fb89-106">Member</span><span class="sxs-lookup"><span data-stu-id="0fb89-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0fb89-107">**szprotocol**</span><span class="sxs-lookup"><span data-stu-id="0fb89-107">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="0fb89-108">Der Name des Protokolls.</span><span class="sxs-lookup"><span data-stu-id="0fb89-108">The name of the protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fb89-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fb89-109">Remarks</span></span>

<span data-ttu-id="0fb89-110">Die [PF \_](pf-followset.md) -nach Verfolgungs Struktur verwendet ein Array von **PF \_** -after-Entry-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="0fb89-110">The [PF\_FOLLOWSET](pf-followset.md) structure uses an array of **PF\_FOLLOWENTRY** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fb89-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fb89-111">Requirements</span></span>



| <span data-ttu-id="0fb89-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fb89-112">Requirement</span></span> | <span data-ttu-id="0fb89-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0fb89-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0fb89-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fb89-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0fb89-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fb89-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0fb89-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fb89-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0fb89-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fb89-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0fb89-118">Header</span><span class="sxs-lookup"><span data-stu-id="0fb89-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fb89-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fb89-119"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fb89-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fb89-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fb89-121">PF-nach \_ Verfolgung</span><span class="sxs-lookup"><span data-stu-id="0fb89-121">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> </dl>

 

 





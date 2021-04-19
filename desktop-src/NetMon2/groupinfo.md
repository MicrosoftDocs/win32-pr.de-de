---
description: Ordnet einen Gruppennamen und sein Handle zu.
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: GroupInfo-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GROUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5152b0a621a34e49d6f1024a81b7e91aed94a06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343040"
---
# <a name="groupinfo-structure"></a><span data-ttu-id="a73d9-103">GroupInfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="a73d9-103">GROUPINFO structure</span></span>

<span data-ttu-id="a73d9-104">Die **groupInfo** -Struktur ordnet einen Gruppennamen und sein Handle zu.</span><span class="sxs-lookup"><span data-stu-id="a73d9-104">The **GROUPINFO** structure associates a group name and its handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73d9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a73d9-105">Syntax</span></span>


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a><span data-ttu-id="a73d9-106">Member</span><span class="sxs-lookup"><span data-stu-id="a73d9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a73d9-107">**szgroupname**</span><span class="sxs-lookup"><span data-stu-id="a73d9-107">**szGroupName**</span></span>
</dt> <dd>

<span data-ttu-id="a73d9-108">Inkrementierter Wert eines Arrays in der **GroupName** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a73d9-108">Incremented value of an array in the **GROUPNAME** structure.</span></span>

</dd> <dt>

<span data-ttu-id="a73d9-109">**hGroup**</span><span class="sxs-lookup"><span data-stu-id="a73d9-109">**hGroup**</span></span>
</dt> <dd>

<span data-ttu-id="a73d9-110">Handle für eine Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a73d9-110">Handle to a group.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a73d9-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a73d9-111">Requirements</span></span>



| <span data-ttu-id="a73d9-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a73d9-112">Requirement</span></span> | <span data-ttu-id="a73d9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a73d9-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a73d9-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a73d9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a73d9-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a73d9-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a73d9-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a73d9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a73d9-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a73d9-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a73d9-118">Header</span><span class="sxs-lookup"><span data-stu-id="a73d9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a73d9-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a73d9-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 





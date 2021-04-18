---
description: Die Bereichs Struktur definiert einen Bereich gültiger Eigenschaftswerte.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Bereichs Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RANGE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bf465636f315e60e43350bb370e2002b8a96e635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347118"
---
# <a name="range-structure"></a><span data-ttu-id="e138e-103">Bereichs Struktur</span><span class="sxs-lookup"><span data-stu-id="e138e-103">RANGE structure</span></span>

<span data-ttu-id="e138e-104">Die **Bereichs** Struktur definiert einen Bereich gültiger Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="e138e-104">The **RANGE** structure defines a range of valid property values.</span></span>

## <a name="syntax"></a><span data-ttu-id="e138e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e138e-105">Syntax</span></span>


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a><span data-ttu-id="e138e-106">Member</span><span class="sxs-lookup"><span data-stu-id="e138e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e138e-107">**MinValue**</span><span class="sxs-lookup"><span data-stu-id="e138e-107">**MinValue**</span></span>
</dt> <dd>

<span data-ttu-id="e138e-108">Der niedrigste mögliche Wert in einem Bereich.</span><span class="sxs-lookup"><span data-stu-id="e138e-108">Lowest possible value in a range.</span></span>

</dd> <dt>

<span data-ttu-id="e138e-109">**MaxValue**</span><span class="sxs-lookup"><span data-stu-id="e138e-109">**MaxValue**</span></span>
</dt> <dd>

<span data-ttu-id="e138e-110">Höchstmöglicher Wert in einem Bereich.</span><span class="sxs-lookup"><span data-stu-id="e138e-110">Highest possible value in a range.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e138e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e138e-111">Remarks</span></span>

<span data-ttu-id="e138e-112">Die **Bereichs** Struktur wird verwendet, um einen gültigen Bereich von Zahlen für eine Protokoll Eigenschaft anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e138e-112">The **RANGE** structure is used to specify a valid range of numbers for a protocol property.</span></span> <span data-ttu-id="e138e-113">Wenn das **dataqualifier** -Element der **PropertyInfo** -Struktur auf den **Prop-Wert \_ \_ Bereich** festgelegt ist, muss der **lprange** -Member der [PropertyInfo](propertyinfo.md) -Struktur einen Zeiger auf eine **Bereichs** Struktur bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e138e-113">If the **DataQualifier** member of the **PROPERTYINFO** structure is set to **PROP\_QUAL\_RANGE**, the **lpRange** member of the [PROPERTYINFO](propertyinfo.md) structure must provide a pointer to a **RANGE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e138e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e138e-114">Requirements</span></span>



| <span data-ttu-id="e138e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e138e-115">Requirement</span></span> | <span data-ttu-id="e138e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e138e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e138e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e138e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e138e-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e138e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e138e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e138e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e138e-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e138e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e138e-121">Header</span><span class="sxs-lookup"><span data-stu-id="e138e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e138e-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e138e-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e138e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e138e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e138e-124">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="e138e-124">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> </dl>

 

 





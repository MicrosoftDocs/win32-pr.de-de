---
title: min-Makro (minwindef. h)
description: Das min-Makro vergleicht zwei Werte und gibt den kleineren Wert zurück. Der Datentyp kann ein beliebiger numerischer Datentyp sein, mit oder ohne Vorzeichen. Der Datentyp der Argumente und der Rückgabewert sind identisch.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- Min. Makro Windows Multimedia
topic_type:
- apiref
api_name:
- min
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b50680d5902ae2dc895f53f023c4b229b03c7e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743928"
---
# <a name="min-macro"></a><span data-ttu-id="147cd-106">min-Makro</span><span class="sxs-lookup"><span data-stu-id="147cd-106">min macro</span></span>

<span data-ttu-id="147cd-107">Das **Min** -Makro vergleicht zwei Werte und gibt den kleineren Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="147cd-107">The **min** macro compares two values and returns the smaller one.</span></span> <span data-ttu-id="147cd-108">Der Datentyp kann ein beliebiger numerischer Datentyp sein, mit oder ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="147cd-108">The data type can be any numeric data type, signed or unsigned.</span></span> <span data-ttu-id="147cd-109">Der Datentyp der Argumente und der Rückgabewert sind identisch.</span><span class="sxs-lookup"><span data-stu-id="147cd-109">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="147cd-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="147cd-110">Syntax</span></span>


```C++
 min(
    value1,
    value2
);
```



## <a name="parameters"></a><span data-ttu-id="147cd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="147cd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="147cd-112">*value1*</span><span class="sxs-lookup"><span data-stu-id="147cd-112">*value1*</span></span> 
</dt> <dd>

<span data-ttu-id="147cd-113">Gibt den ersten von zwei Werten an.</span><span class="sxs-lookup"><span data-stu-id="147cd-113">Specifies the first of two values.</span></span>

</dd> <dt>

<span data-ttu-id="147cd-114">*value2*</span><span class="sxs-lookup"><span data-stu-id="147cd-114">*value2*</span></span> 
</dt> <dd>

<span data-ttu-id="147cd-115">Gibt die zweite von zwei-Werten an.</span><span class="sxs-lookup"><span data-stu-id="147cd-115">Specifies the second of two values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="147cd-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="147cd-116">Return value</span></span>

<span data-ttu-id="147cd-117">Der Rückgabewert ist der kleinere der beiden angegebenen-Werte.</span><span class="sxs-lookup"><span data-stu-id="147cd-117">The return value is the smaller of the two specified values.</span></span>

## <a name="remarks"></a><span data-ttu-id="147cd-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="147cd-118">Remarks</span></span>

<span data-ttu-id="147cd-119">Das **Min** -Makro wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="147cd-119">The **min** macro is defined as follows:</span></span>


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a><span data-ttu-id="147cd-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="147cd-120">Requirements</span></span>



| <span data-ttu-id="147cd-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="147cd-121">Requirement</span></span> | <span data-ttu-id="147cd-122">Wert</span><span class="sxs-lookup"><span data-stu-id="147cd-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="147cd-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="147cd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="147cd-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="147cd-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="147cd-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="147cd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="147cd-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="147cd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="147cd-127">Header</span><span class="sxs-lookup"><span data-stu-id="147cd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="147cd-128"><dt>Minwindef. h</dt></span><span class="sxs-lookup"><span data-stu-id="147cd-128"><dt>Minwindef.h</dt></span></span> </dl> |



 

 






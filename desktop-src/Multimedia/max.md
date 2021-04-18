---
title: Maximales Makro (minwindef. h)
description: Das Maximum-Makro vergleicht zwei Werte und gibt den größeren Wert zurück. Der Datentyp kann ein beliebiger numerischer Datentyp sein, mit oder ohne Vorzeichen. Der Datentyp der Argumente und der Rückgabewert sind identisch.
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- Maximales Makro Windows Multimedia
topic_type:
- apiref
api_name:
- max
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b484f2505958aca04745c63ca63a0dd131a51ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517633"
---
# <a name="max-macro"></a><span data-ttu-id="5c34b-106">max-Makro</span><span class="sxs-lookup"><span data-stu-id="5c34b-106">max macro</span></span>

<span data-ttu-id="5c34b-107">Das **Maximum** -Makro vergleicht zwei Werte und gibt den größeren Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5c34b-107">The **max** macro compares two values and returns the larger one.</span></span> <span data-ttu-id="5c34b-108">Der Datentyp kann ein beliebiger numerischer Datentyp sein, mit oder ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="5c34b-108">The data type can be any numeric data type, signed or unsigned.</span></span> <span data-ttu-id="5c34b-109">Der Datentyp der Argumente und der Rückgabewert sind identisch.</span><span class="sxs-lookup"><span data-stu-id="5c34b-109">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c34b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c34b-110">Syntax</span></span>


```C++
 max(
    value1,
    value2
);
```



## <a name="parameters"></a><span data-ttu-id="5c34b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c34b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c34b-112">*value1*</span><span class="sxs-lookup"><span data-stu-id="5c34b-112">*value1*</span></span> 
</dt> <dd>

<span data-ttu-id="5c34b-113">Gibt den ersten von zwei Werten an.</span><span class="sxs-lookup"><span data-stu-id="5c34b-113">Specifies the first of two values.</span></span>

</dd> <dt>

<span data-ttu-id="5c34b-114">*value2*</span><span class="sxs-lookup"><span data-stu-id="5c34b-114">*value2*</span></span> 
</dt> <dd>

<span data-ttu-id="5c34b-115">Gibt die zweite von zwei-Werten an.</span><span class="sxs-lookup"><span data-stu-id="5c34b-115">Specifies the second of two values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c34b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c34b-116">Return value</span></span>

<span data-ttu-id="5c34b-117">Der Rückgabewert ist der größere der beiden angegebenen-Werte.</span><span class="sxs-lookup"><span data-stu-id="5c34b-117">The return value is the greater of the two specified values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c34b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c34b-118">Remarks</span></span>

<span data-ttu-id="5c34b-119">Das **Maximum** -Makro wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="5c34b-119">The **max** macro is defined as follows:</span></span>


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a><span data-ttu-id="5c34b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c34b-120">Requirements</span></span>



| <span data-ttu-id="5c34b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c34b-121">Requirement</span></span> | <span data-ttu-id="5c34b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5c34b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c34b-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c34b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5c34b-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c34b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5c34b-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c34b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5c34b-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c34b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5c34b-127">Header</span><span class="sxs-lookup"><span data-stu-id="5c34b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c34b-128"><dt>Minwindef. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c34b-128"><dt>Minwindef.h</dt></span></span> </dl> |



 

 






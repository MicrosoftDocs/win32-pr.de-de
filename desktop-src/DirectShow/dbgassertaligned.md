---
description: Testet, ob ein Zeiger an einer angegebenen Grenze ausgerichtet ist. Andernfalls ruft dieses Makro das ASSERT-Makro auf. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: Dbgassertaligned-Makro (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgAssertAligned
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 22b357f7f28e9df04ce36636e3972dbadc3036a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361485"
---
# <a name="dbgassertaligned-macro"></a><span data-ttu-id="2950f-105">Dbgassertaligned-Makro</span><span class="sxs-lookup"><span data-stu-id="2950f-105">DbgAssertAligned macro</span></span>

<span data-ttu-id="2950f-106">Testet, ob ein Zeiger an einer angegebenen Grenze ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="2950f-106">Tests whether a pointer is aligned to a specified boundary.</span></span> <span data-ttu-id="2950f-107">Andernfalls ruft dieses Makro das [**Assert**](assert.md) -Makro auf.</span><span class="sxs-lookup"><span data-stu-id="2950f-107">If not, this macro invokes the [**ASSERT**](assert.md) macro.</span></span> <span data-ttu-id="2950f-108">Wird in Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2950f-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="2950f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2950f-109">Syntax</span></span>


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a><span data-ttu-id="2950f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2950f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2950f-111">*ptr*</span><span class="sxs-lookup"><span data-stu-id="2950f-111">*ptr*</span></span> 
</dt> <dd>

<span data-ttu-id="2950f-112">Die Zeiger Variable.</span><span class="sxs-lookup"><span data-stu-id="2950f-112">Pointer variable.</span></span>

</dd> <dt>

<span data-ttu-id="2950f-113">*Richt*</span><span class="sxs-lookup"><span data-stu-id="2950f-113">*alignment*</span></span> 
</dt> <dd>

<span data-ttu-id="2950f-114">Erforderliche Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="2950f-114">Required alignment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2950f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2950f-115">Return value</span></span>

<span data-ttu-id="2950f-116">Dieses Makro gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2950f-116">This macro does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2950f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2950f-117">Requirements</span></span>



| <span data-ttu-id="2950f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2950f-118">Requirement</span></span> | <span data-ttu-id="2950f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2950f-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2950f-120">Header</span><span class="sxs-lookup"><span data-stu-id="2950f-120">Header</span></span><br/> | <dl> <span data-ttu-id="2950f-121"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2950f-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2950f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2950f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2950f-123">Assert-und breakpointmakros</span><span class="sxs-lookup"><span data-stu-id="2950f-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 





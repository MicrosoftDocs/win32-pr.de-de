---
description: Wertet einen Ausdruck aus und verursacht eine breakpointausnahme, wenn der Ausdruck false ist. Der Text des Ausdrucks, der Name der Quelldatei und die Zeilennummer werden mithilfe des dbglog-Makros protokolliert. Wird in Einzelhandels Builds ignoriert.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: Kassert-Makro (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: f797e60a6175a86f2c1c9d675e9607a48a58c14a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362159"
---
# <a name="kassert-macro"></a><span data-ttu-id="8ec31-105">Kassert-Makro</span><span class="sxs-lookup"><span data-stu-id="8ec31-105">KASSERT macro</span></span>

<span data-ttu-id="8ec31-106">Wertet einen Ausdruck aus und verursacht eine breakpointausnahme, wenn der Ausdruck **false** ist.</span><span class="sxs-lookup"><span data-stu-id="8ec31-106">Evaluates an expression, and causes a breakpoint exception if the expression is **FALSE**.</span></span> <span data-ttu-id="8ec31-107">Der Text des Ausdrucks, der Name der Quelldatei und die Zeilennummer werden mithilfe des [**dbglog**](dbglog.md) -Makros protokolliert.</span><span class="sxs-lookup"><span data-stu-id="8ec31-107">The text of the expression, the name of the source file, and the line number are logged using the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="8ec31-108">Wird in Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8ec31-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ec31-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ec31-109">Syntax</span></span>


```C++
void KASSERT(
    cond
);
```



## <a name="parameters"></a><span data-ttu-id="8ec31-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ec31-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ec31-111">*cond*</span><span class="sxs-lookup"><span data-stu-id="8ec31-111">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec31-112">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="8ec31-112">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ec31-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ec31-113">Return value</span></span>

<span data-ttu-id="8ec31-114">Dieses Makro gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8ec31-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ec31-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ec31-115">Remarks</span></span>

<span data-ttu-id="8ec31-116">Im Gegensatz zu den Makros [**Assert**](assert.md) und [**Execute \_ Assert**](execute-assert.md) zeigt dieses Makro kein Meldungs Feld an, in dem der Benutzer dazu aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="8ec31-116">Unlike the [**ASSERT**](assert.md) and [**EXECUTE\_ASSERT**](execute-assert.md) macros, this macro does not display a message box prompting the user.</span></span> <span data-ttu-id="8ec31-117">Wenn in Debugbuilds der Ausdruck **false** lautet, bewirkt das Makro automatisch, dass eine breakpointausnahme auftritt.</span><span class="sxs-lookup"><span data-stu-id="8ec31-117">In debug builds, if the expression is **FALSE**, the macro automatically causes a breakpoint exception to occur.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ec31-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ec31-118">Requirements</span></span>



| <span data-ttu-id="8ec31-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ec31-119">Requirement</span></span> | <span data-ttu-id="8ec31-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8ec31-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec31-121">Header</span><span class="sxs-lookup"><span data-stu-id="8ec31-121">Header</span></span><br/> | <dl> <span data-ttu-id="8ec31-122"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ec31-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ec31-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ec31-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec31-124">Assert-und breakpointmakros</span><span class="sxs-lookup"><span data-stu-id="8ec31-124">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 





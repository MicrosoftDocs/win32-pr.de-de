---
description: Wertet einen Ausdruck in Debug-und Retail-Builds aus. In Debugbuilds zeigt eine Diagnose Meldung an, wenn der Ausdruck false ist.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: EXECUTE_ASSERT-Makro (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXECUTE_ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 5db5e78d198cc9f66aa5de6fdb0160e325b82591
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365833"
---
# <a name="execute_assert-macro"></a><span data-ttu-id="3bb66-104">\_ASSERT-Makro ausführen</span><span class="sxs-lookup"><span data-stu-id="3bb66-104">EXECUTE\_ASSERT macro</span></span>

<span data-ttu-id="3bb66-105">Wertet einen Ausdruck in Debug-und Retail-Builds aus.</span><span class="sxs-lookup"><span data-stu-id="3bb66-105">Evaluates an expression in debug and retail builds.</span></span> <span data-ttu-id="3bb66-106">In Debugbuilds zeigt eine Diagnose Meldung an, wenn der Ausdruck **false** ist.</span><span class="sxs-lookup"><span data-stu-id="3bb66-106">In debug builds, displays a diagnostic message if the expression is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bb66-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bb66-107">Syntax</span></span>


```C++
void EXECUTE_ASSERT(
    cond
);
```



## <a name="parameters"></a><span data-ttu-id="3bb66-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bb66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bb66-109">*cond*</span><span class="sxs-lookup"><span data-stu-id="3bb66-109">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb66-110">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="3bb66-110">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bb66-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3bb66-111">Return value</span></span>

<span data-ttu-id="3bb66-112">Dieses Makro gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3bb66-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bb66-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3bb66-113">Remarks</span></span>

<span data-ttu-id="3bb66-114">Im Gegensatz zum [**Assert**](assert.md) -Makro wertet dieses Makro den Ausdruck in Einzelhandels Builds aus.</span><span class="sxs-lookup"><span data-stu-id="3bb66-114">Unlike the [**ASSERT**](assert.md) macro, this macro evaluates the expression in retail builds.</span></span> <span data-ttu-id="3bb66-115">Wenn in Debugbuilds der Ausdruck **false** ist, zeigt das Makro ein Meldungs Feld mit dem Text des Ausdrucks, dem Namen der Quelldatei und der Zeilennummer an.</span><span class="sxs-lookup"><span data-stu-id="3bb66-115">In debug builds, if the expression is **FALSE**, the macro displays a message box with the text of the expression, the name of the source file, and the line number.</span></span> <span data-ttu-id="3bb66-116">Der Benutzer kann die-Übersetzung ignorieren, den Debugger eingeben oder die Anwendung beenden.</span><span class="sxs-lookup"><span data-stu-id="3bb66-116">The user can ignore the assertion, enter the debugger, or quit the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bb66-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bb66-117">Requirements</span></span>



| <span data-ttu-id="3bb66-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bb66-118">Requirement</span></span> | <span data-ttu-id="3bb66-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3bb66-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb66-120">Header</span><span class="sxs-lookup"><span data-stu-id="3bb66-120">Header</span></span><br/> | <dl> <span data-ttu-id="3bb66-121"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3bb66-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bb66-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bb66-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bb66-123">Assert-und breakpointmakros</span><span class="sxs-lookup"><span data-stu-id="3bb66-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 





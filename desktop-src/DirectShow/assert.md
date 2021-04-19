---
description: Wertet einen Ausdruck aus und zeigt eine Diagnose Meldung an, wenn der Ausdruck false ist. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: Assert-Makro (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 8617d1c86f655cc9b44ea6619931f73888ae2a67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359381"
---
# <a name="assert-macro"></a><span data-ttu-id="82ce4-104">ASSERT-Makro</span><span class="sxs-lookup"><span data-stu-id="82ce4-104">ASSERT macro</span></span>

<span data-ttu-id="82ce4-105">Wertet einen Ausdruck aus und zeigt eine Diagnose Meldung an, wenn der Ausdruck **false** ist.</span><span class="sxs-lookup"><span data-stu-id="82ce4-105">Evaluates an expression, and displays a diagnostic message if the expression is **FALSE**.</span></span> <span data-ttu-id="82ce4-106">Wird in Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="82ce4-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="82ce4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="82ce4-107">Syntax</span></span>


```C++
void ASSERT(
   BOOL cond
);
```



## <a name="parameters"></a><span data-ttu-id="82ce4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="82ce4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82ce4-109">*cond*</span><span class="sxs-lookup"><span data-stu-id="82ce4-109">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="82ce4-110">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="82ce4-110">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82ce4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82ce4-111">Return value</span></span>

<span data-ttu-id="82ce4-112">Dieses Makro gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="82ce4-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82ce4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82ce4-113">Remarks</span></span>

<span data-ttu-id="82ce4-114">Wenn in Debugbuilds der Ausdruck **false** ist, zeigt dieses Makro ein Meldungs Feld mit dem Text des Ausdrucks, dem Namen der Quelldatei und der Zeilennummer an.</span><span class="sxs-lookup"><span data-stu-id="82ce4-114">In debug builds, if the expression is **FALSE**, this macro displays a message box with the text of the expression, the name of the source file, and the line number.</span></span> <span data-ttu-id="82ce4-115">Der Benutzer kann die-Übersetzung ignorieren, den Debugger eingeben oder die Anwendung beenden.</span><span class="sxs-lookup"><span data-stu-id="82ce4-115">The user can ignore the assertion, enter the debugger, or quit the application.</span></span>

## <a name="examples"></a><span data-ttu-id="82ce4-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="82ce4-116">Examples</span></span>


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a><span data-ttu-id="82ce4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82ce4-117">Requirements</span></span>



| <span data-ttu-id="82ce4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82ce4-118">Requirement</span></span> | <span data-ttu-id="82ce4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="82ce4-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82ce4-120">Header</span><span class="sxs-lookup"><span data-stu-id="82ce4-120">Header</span></span><br/> | <dl> <span data-ttu-id="82ce4-121"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82ce4-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82ce4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82ce4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82ce4-123">Assert-und breakpointmakros</span><span class="sxs-lookup"><span data-stu-id="82ce4-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 





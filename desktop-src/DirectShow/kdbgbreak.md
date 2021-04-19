---
description: Verursacht eine breakpointausnahme und protokolliert die angegebene Zeichenfolge mit dem dbglog-Makro. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: Kdbgbreak-Makro (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KDbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 9631dc8d956652137810b25ae5923cc1c6927bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357531"
---
# <a name="kdbgbreak-macro"></a><span data-ttu-id="22170-104">Kdbgbreak-Makro</span><span class="sxs-lookup"><span data-stu-id="22170-104">KDbgBreak macro</span></span>

<span data-ttu-id="22170-105">Verursacht eine breakpointausnahme und protokolliert die angegebene Zeichenfolge mit dem [**dbglog**](dbglog.md) -Makro.</span><span class="sxs-lookup"><span data-stu-id="22170-105">Causes a breakpoint exception, and logs the specified string using the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="22170-106">Wird in Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="22170-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="22170-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="22170-107">Syntax</span></span>


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="22170-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="22170-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22170-109">*"Straume"*</span><span class="sxs-lookup"><span data-stu-id="22170-109">*strLiteral*</span></span> 
</dt> <dd>

<span data-ttu-id="22170-110">Text Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="22170-110">Text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22170-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22170-111">Return value</span></span>

<span data-ttu-id="22170-112">Dieses Makro gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="22170-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22170-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22170-113">Remarks</span></span>

<span data-ttu-id="22170-114">Im Gegensatz zum [**dbgbreak**](dbgbreak.md) -Makro zeigt dieses Makro kein Meldungs Feld an, in dem der Benutzer dazu aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="22170-114">Unlike the [**DbgBreak**](dbgbreak.md) macro, this macro does not display a message box prompting the user.</span></span> <span data-ttu-id="22170-115">In Debugbuilds bewirkt dies automatisch, dass eine breakpointausnahme auftritt.</span><span class="sxs-lookup"><span data-stu-id="22170-115">In debug builds, it automatically causes a breakpoint exception to occur.</span></span>

## <a name="requirements"></a><span data-ttu-id="22170-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22170-116">Requirements</span></span>



| <span data-ttu-id="22170-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22170-117">Requirement</span></span> | <span data-ttu-id="22170-118">Wert</span><span class="sxs-lookup"><span data-stu-id="22170-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22170-119">Header</span><span class="sxs-lookup"><span data-stu-id="22170-119">Header</span></span><br/> | <dl> <span data-ttu-id="22170-120"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22170-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22170-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22170-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22170-122">Assert-und breakpointmakros</span><span class="sxs-lookup"><span data-stu-id="22170-122">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 





---
description: Das Note-Makro sendet eine Zeichenfolge an den debugausgabespeicherort. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: Hinweis (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NOTE
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 898d31c48807c3bf0826dc643d89126db36b0f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361480"
---
# <a name="note"></a><span data-ttu-id="0dea9-104">HINWEIS</span><span class="sxs-lookup"><span data-stu-id="0dea9-104">NOTE</span></span>

<span data-ttu-id="0dea9-105">Das- `NOTE` Makro sendet eine Zeichenfolge an den debugausgabeort.</span><span class="sxs-lookup"><span data-stu-id="0dea9-105">The `NOTE` macro sends a string to the debug output location.</span></span> <span data-ttu-id="0dea9-106">Wird in Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0dea9-106">Ignored in retail builds.</span></span>

``` syntax
NOTE(
    pFormat
);

NOTEn(
    pFormat,
    arg1 ... arg5
);
```

## <a name="parameters"></a><span data-ttu-id="0dea9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0dea9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dea9-108"><span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pformat*</span><span class="sxs-lookup"><span data-stu-id="0dea9-108"><span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*</span></span>
</dt> <dd>

<span data-ttu-id="0dea9-109">Eine Format Zeichenfolge im printf-Format.</span><span class="sxs-lookup"><span data-stu-id="0dea9-109">A printf -style format string.</span></span>

</dd> <dt>

<span data-ttu-id="0dea9-110"><span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*</span><span class="sxs-lookup"><span data-stu-id="0dea9-110"><span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*</span></span>
</dt> <dd>

<span data-ttu-id="0dea9-111">Zusätzliche Argumente für die Format Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0dea9-111">Additional arguments for the format string.</span></span> <span data-ttu-id="0dea9-112">Die Anzahl der Argumente muss mit dem Namen des Makros identisch sein.</span><span class="sxs-lookup"><span data-stu-id="0dea9-112">The number of arguments must match the macro name.</span></span> <span data-ttu-id="0dea9-113">Beispielsweise übernimmt **NOTE1** ein Argument, und **NOTE5** übernimmt fünf Argumente.</span><span class="sxs-lookup"><span data-stu-id="0dea9-113">For example, **NOTE1** takes one argument, and **NOTE5** takes five arguments.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0dea9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0dea9-114">Remarks</span></span>

<span data-ttu-id="0dea9-115">Diese Makros sind Varianten des [**dbglog**](dbglog.md) -Makros.</span><span class="sxs-lookup"><span data-stu-id="0dea9-115">These macros are variants of the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="0dea9-116">Sie generieren Protokoll-Ablauf \_ Verfolgungs Meldungen der Ebene 5.</span><span class="sxs-lookup"><span data-stu-id="0dea9-116">They generate level 5 LOG\_TRACE messages.</span></span>

## <a name="example"></a><span data-ttu-id="0dea9-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0dea9-117">Example</span></span>


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
```



## <a name="requirements"></a><span data-ttu-id="0dea9-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0dea9-118">Requirements</span></span>



| <span data-ttu-id="0dea9-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0dea9-119">Requirement</span></span> | <span data-ttu-id="0dea9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0dea9-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dea9-121">Header</span><span class="sxs-lookup"><span data-stu-id="0dea9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0dea9-122"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0dea9-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0dea9-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0dea9-123">Library</span></span><br/> | <dl> <span data-ttu-id="0dea9-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0dea9-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dea9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dea9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dea9-126">Debug-Ausgabefunktionen</span><span class="sxs-lookup"><span data-stu-id="0dea9-126">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 





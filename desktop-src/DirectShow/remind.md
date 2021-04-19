---
description: Das Erinnerungs Makro generiert zum Zeitpunkt der Kompilierung eine Erinnerung. Dieses Makro generiert eine Zeichenfolge, die die Parameter Zeichenfolge, den Namen der Quelldatei und die Zeilennummer enthält.
ms.assetid: 12043df5-ed68-4980-91aa-7598d8ab1951
title: Erinnerung (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- REMIND
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 305e5df628244293b643da8882f57dd83041c4c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372074"
---
# <a name="remind"></a><span data-ttu-id="d4d7e-104">Erinnern</span><span class="sxs-lookup"><span data-stu-id="d4d7e-104">REMIND</span></span>

<span data-ttu-id="d4d7e-105">Das `REMIND` Makro generiert zum Zeitpunkt der Kompilierung eine Erinnerung.</span><span class="sxs-lookup"><span data-stu-id="d4d7e-105">The `REMIND` macro generates a reminder at compile time.</span></span> <span data-ttu-id="d4d7e-106">Dieses Makro generiert eine Zeichenfolge, die die Parameter Zeichenfolge, den Namen der Quelldatei und die Zeilennummer enthält.</span><span class="sxs-lookup"><span data-stu-id="d4d7e-106">This macro generates a string that includes the parameter string, the name of the source file, and the line number.</span></span>

``` syntax
REMIND(strLiteral);
```

## <a name="parameters"></a><span data-ttu-id="d4d7e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4d7e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4d7e-108"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*"Straume"*</span><span class="sxs-lookup"><span data-stu-id="d4d7e-108"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span></span>
</dt> <dd>

<span data-ttu-id="d4d7e-109">Text Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d4d7e-109">Text string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4d7e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4d7e-110">Remarks</span></span>

<span data-ttu-id="d4d7e-111">Dieses Makro ist nützlich zum Erzeugen von Warnungen zur Kompilierzeit:</span><span class="sxs-lookup"><span data-stu-id="d4d7e-111">This macro is useful for generating compile-time warnings:</span></span>


```C++
#pragma message (REMIND("TO DO: Add support for IDispatch."))
```



## <a name="requirements"></a><span data-ttu-id="d4d7e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4d7e-112">Requirements</span></span>



| <span data-ttu-id="d4d7e-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4d7e-113">Requirement</span></span> | <span data-ttu-id="d4d7e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d4d7e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d7e-115">Header</span><span class="sxs-lookup"><span data-stu-id="d4d7e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d4d7e-116"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4d7e-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d4d7e-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d4d7e-117">Library</span></span><br/> | <dl> <span data-ttu-id="d4d7e-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d4d7e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4d7e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4d7e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d7e-120">Debug-Ausgabefunktionen</span><span class="sxs-lookup"><span data-stu-id="d4d7e-120">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 





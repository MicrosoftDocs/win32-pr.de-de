---
description: Die dbgcheckmodulelevel-Funktion überprüft, ob die Protokollierung für die angegebenen Nachrichten Typen und die angegebene Ebene aktiviert ist. Wird in Einzelhandels Builds ignoriert.
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: Dbgcheckmodulelevel-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgCheckModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79df8cd06617cf9b17fa9933d4d7a87954a6e2b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373978"
---
# <a name="dbgcheckmodulelevel-function"></a><span data-ttu-id="e8a87-104">Dbgcheckmodulelevel-Funktion</span><span class="sxs-lookup"><span data-stu-id="e8a87-104">DbgCheckModuleLevel function</span></span>

<span data-ttu-id="e8a87-105">Die `DbgCheckModuleLevel` -Funktion überprüft, ob die Protokollierung für die angegebenen Nachrichten Typen und-Ebenen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e8a87-105">The `DbgCheckModuleLevel` function checks whether logging is enabled for the given message types and level.</span></span> <span data-ttu-id="e8a87-106">Wird in Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e8a87-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a87-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8a87-107">Syntax</span></span>


```C++
BOOL DbgCheckModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="e8a87-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8a87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8a87-109">*Typen*</span><span class="sxs-lookup"><span data-stu-id="e8a87-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a87-110">Bitweise Kombination von einem oder mehreren Nachrichten Typen.</span><span class="sxs-lookup"><span data-stu-id="e8a87-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="e8a87-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="e8a87-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a87-112">Protokolliergrad</span><span class="sxs-lookup"><span data-stu-id="e8a87-112">Logging level</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8a87-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8a87-113">Return value</span></span>

<span data-ttu-id="e8a87-114">Gibt **true** zurück, wenn die Protokollierung für einen der angegebenen Nachrichten Typen auf die angegebene Ebene oder höher festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e8a87-114">Returns **TRUE** if logging for any of the specified message types is set to the specified level or higher.</span></span> <span data-ttu-id="e8a87-115">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e8a87-115">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8a87-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8a87-116">Requirements</span></span>



| <span data-ttu-id="e8a87-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8a87-117">Requirement</span></span> | <span data-ttu-id="e8a87-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e8a87-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a87-119">Header</span><span class="sxs-lookup"><span data-stu-id="e8a87-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e8a87-120"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8a87-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e8a87-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e8a87-121">Library</span></span><br/> | <dl> <span data-ttu-id="e8a87-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e8a87-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8a87-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8a87-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a87-124">Debug-Ausgabefunktionen</span><span class="sxs-lookup"><span data-stu-id="e8a87-124">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 





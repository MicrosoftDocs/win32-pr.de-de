---
description: Die dbgsetmodulelevel-Funktion legt den Protokolliergrad für einen oder mehrere Nachrichten Typen fest. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 89d25106-8018-4089-8b77-d3c87529e984
title: Dbgsetmodulelevel-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d6623793b150c600eb00f0c0843dd72c68deb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358381"
---
# <a name="dbgsetmodulelevel-function"></a><span data-ttu-id="a3191-104">Dbgsetmodulelevel-Funktion</span><span class="sxs-lookup"><span data-stu-id="a3191-104">DbgSetModuleLevel function</span></span>

<span data-ttu-id="a3191-105">Die **dbgsetmodulelevel** -Funktion legt den Protokolliergrad für einen oder mehrere Nachrichten Typen fest.</span><span class="sxs-lookup"><span data-stu-id="a3191-105">The **DbgSetModuleLevel** function sets the logging level for one or more message types.</span></span> <span data-ttu-id="a3191-106">Wird in Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a3191-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3191-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3191-107">Syntax</span></span>


```C++
void DbgSetModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="a3191-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3191-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3191-109">*Typen*</span><span class="sxs-lookup"><span data-stu-id="a3191-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="a3191-110">Bitweise Kombination von einem oder mehreren Nachrichten Typen.</span><span class="sxs-lookup"><span data-stu-id="a3191-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="a3191-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="a3191-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="a3191-112">Protokolliergrad für die angegebenen Nachrichten Typen.</span><span class="sxs-lookup"><span data-stu-id="a3191-112">Logging level for the specified message types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3191-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3191-113">Return value</span></span>

<span data-ttu-id="a3191-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a3191-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3191-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3191-115">Requirements</span></span>



| <span data-ttu-id="a3191-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3191-116">Requirement</span></span> | <span data-ttu-id="a3191-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a3191-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3191-118">Header</span><span class="sxs-lookup"><span data-stu-id="a3191-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a3191-119"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3191-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a3191-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a3191-120">Library</span></span><br/> | <dl> <span data-ttu-id="a3191-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a3191-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3191-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3191-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3191-123">Debug-Ausgabefunktionen</span><span class="sxs-lookup"><span data-stu-id="a3191-123">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 





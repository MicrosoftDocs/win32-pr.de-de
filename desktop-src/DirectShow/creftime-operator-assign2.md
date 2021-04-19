---
description: Der Operator = weist eine neue Bezugszeit zu. Diese Methode verwendet den *ll* -Parameter.
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: "\"Kref time. Operator = Method (Ref time. h)-ll\"-Parameter"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d09cb957e06d8b075cff3d831a7f68fbbdf662a8
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106372806"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a><span data-ttu-id="10299-104">"Kref time. Operator = Method (Ref time. h)-ll"-Parameter</span><span class="sxs-lookup"><span data-stu-id="10299-104">CRefTime.operator= method (Reftime.h) - ll parameter</span></span>

<span data-ttu-id="10299-105">Der Operator = weist eine neue Bezugszeit zu.</span><span class="sxs-lookup"><span data-stu-id="10299-105">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="10299-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="10299-106">Syntax</span></span>


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a><span data-ttu-id="10299-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="10299-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10299-108">*ll*</span><span class="sxs-lookup"><span data-stu-id="10299-108">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="10299-109">Neue Verweis Zeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="10299-109">New reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10299-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10299-110">Return value</span></span>

<span data-ttu-id="10299-111">Gibt einen Verweis auf das-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="10299-111">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="10299-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10299-112">Requirements</span></span>



| <span data-ttu-id="10299-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10299-113">Requirement</span></span> | <span data-ttu-id="10299-114">Wert</span><span class="sxs-lookup"><span data-stu-id="10299-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10299-115">Header</span><span class="sxs-lookup"><span data-stu-id="10299-115">Header</span></span>  | <span data-ttu-id="10299-116">Ref time. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="10299-116">Reftime.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="10299-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="10299-117">Library</span></span> | <span data-ttu-id="10299-118">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="10299-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



 

 





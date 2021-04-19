---
description: Die aligndown-Methode verkürzt einen Wert auf eine angegebene Ausrichtungs Grenze.
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: Cpullpin. aligndown-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1383517f4931fa153fd141878475cc8775a61045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359392"
---
# <a name="cpullpinaligndown-method"></a><span data-ttu-id="409f0-103">Cpullpin. aligndown-Methode</span><span class="sxs-lookup"><span data-stu-id="409f0-103">CPullPin.AlignDown method</span></span>

<span data-ttu-id="409f0-104">Die- `AlignDown` Methode verkürzt einen Wert auf eine angegebene Ausrichtungs Grenze.</span><span class="sxs-lookup"><span data-stu-id="409f0-104">The `AlignDown` method truncates a value to a specified alignment boundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="409f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="409f0-105">Syntax</span></span>


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a><span data-ttu-id="409f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="409f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="409f0-107">*ll*</span><span class="sxs-lookup"><span data-stu-id="409f0-107">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="409f0-108">Gibt die Zahl an, die ausgerichtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="409f0-108">Specifies the number to align.</span></span>

</dd> <dt>

<span data-ttu-id="409f0-109">*lalign*</span><span class="sxs-lookup"><span data-stu-id="409f0-109">*lAlign*</span></span> 
</dt> <dd>

<span data-ttu-id="409f0-110">Gibt die Ausrichtungs Grenze an.</span><span class="sxs-lookup"><span data-stu-id="409f0-110">Specifies the alignment boundary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="409f0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="409f0-111">Return value</span></span>

<span data-ttu-id="409f0-112">Gibt das ausgerichtete Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="409f0-112">Returns the aligned result.</span></span>

## <a name="requirements"></a><span data-ttu-id="409f0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="409f0-113">Requirements</span></span>



| <span data-ttu-id="409f0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="409f0-114">Requirement</span></span> | <span data-ttu-id="409f0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="409f0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="409f0-116">Header</span><span class="sxs-lookup"><span data-stu-id="409f0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="409f0-117"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="409f0-117"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="409f0-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="409f0-118">Library</span></span><br/> | <dl> <span data-ttu-id="409f0-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="409f0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="409f0-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="409f0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="409f0-121">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="409f0-121">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 





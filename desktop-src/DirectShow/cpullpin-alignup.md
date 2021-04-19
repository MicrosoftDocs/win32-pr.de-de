---
description: Die alignup-Methode rundet einen Wert auf eine angegebene Ausrichtungs Grenze. Beachten Sie, dass in Windows 7 entfernt wurde. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: Cpullpin. alignup-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignUp
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4f33ae2b7434d90d909315edda4d49e07d8adab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370719"
---
# <a name="cpullpinalignup-method"></a><span data-ttu-id="04589-104">Cpullpin. alignup-Methode</span><span class="sxs-lookup"><span data-stu-id="04589-104">CPullPin.AlignUp method</span></span>

<span data-ttu-id="04589-105">Die **alignup** -Methode rundet einen Wert auf eine angegebene Ausrichtungs Grenze.</span><span class="sxs-lookup"><span data-stu-id="04589-105">The **AlignUp** method rounds a value up to a specified alignment boundary.</span></span>

> [!Note]  
> <span data-ttu-id="04589-106">In Windows 7 entfernt.</span><span class="sxs-lookup"><span data-stu-id="04589-106">Removed in Windows 7.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="04589-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="04589-107">Syntax</span></span>


```C++
LONGLONG AlignUp(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a><span data-ttu-id="04589-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="04589-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04589-109">*ll*</span><span class="sxs-lookup"><span data-stu-id="04589-109">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="04589-110">Gibt die Zahl an, die ausgerichtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="04589-110">Specifies the number to align.</span></span>

</dd> <dt>

<span data-ttu-id="04589-111">*lalign*</span><span class="sxs-lookup"><span data-stu-id="04589-111">*lAlign*</span></span> 
</dt> <dd>

<span data-ttu-id="04589-112">Gibt die Ausrichtungs Grenze an.</span><span class="sxs-lookup"><span data-stu-id="04589-112">Specifies the alignment boundary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04589-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04589-113">Return value</span></span>

<span data-ttu-id="04589-114">Gibt das ausgerichtete Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="04589-114">Returns the aligned result.</span></span>

## <a name="remarks"></a><span data-ttu-id="04589-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04589-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="04589-116">Diese Methode kann einen numerischen Überlauf verursachen, wenn *ll* + (*lalign* -1) überläuft.</span><span class="sxs-lookup"><span data-stu-id="04589-116">This method can cause numeric overflow if *ll* + (*lAlign* - 1) overflows.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="04589-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04589-117">Requirements</span></span>



| <span data-ttu-id="04589-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04589-118">Requirement</span></span> | <span data-ttu-id="04589-119">Wert</span><span class="sxs-lookup"><span data-stu-id="04589-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04589-120">Header</span><span class="sxs-lookup"><span data-stu-id="04589-120">Header</span></span><br/>  | <dl> <span data-ttu-id="04589-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="04589-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="04589-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="04589-122">Library</span></span><br/> | <dl> <span data-ttu-id="04589-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="04589-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04589-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04589-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04589-125">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="04589-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 





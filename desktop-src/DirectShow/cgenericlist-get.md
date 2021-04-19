---
description: Die Get-Methode ruft das Element an der angegebenen Position ab.
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: Cgenericlist. Get-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Get
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02af7d57d2219e6eb0506a8ab11521b4cf3570eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370192"
---
# <a name="cgenericlistget-method"></a><span data-ttu-id="46b26-103">Cgenericlist. Get-Methode</span><span class="sxs-lookup"><span data-stu-id="46b26-103">CGenericList.Get method</span></span>

<span data-ttu-id="46b26-104">Die- `Get` Methode ruft das Element an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="46b26-104">The `Get` method retrieves the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="46b26-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46b26-105">Syntax</span></span>


```C++
OBJECT* Get(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="46b26-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="46b26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46b26-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="46b26-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="46b26-108">Positionsindikator für das Element, das abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="46b26-108">Position indicator for the item to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46b26-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46b26-109">Return value</span></span>

<span data-ttu-id="46b26-110">Gibt einen Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp) zurück.</span><span class="sxs-lookup"><span data-stu-id="46b26-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="46b26-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46b26-111">Remarks</span></span>

<span data-ttu-id="46b26-112">Wenn *POS* **null** ist, gibt die Methode **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="46b26-112">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="46b26-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46b26-113">Requirements</span></span>



| <span data-ttu-id="46b26-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46b26-114">Requirement</span></span> | <span data-ttu-id="46b26-115">Wert</span><span class="sxs-lookup"><span data-stu-id="46b26-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46b26-116">Header</span><span class="sxs-lookup"><span data-stu-id="46b26-116">Header</span></span><br/>  | <dl> <span data-ttu-id="46b26-117"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46b26-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="46b26-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="46b26-118">Library</span></span><br/> | <dl> <span data-ttu-id="46b26-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="46b26-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46b26-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46b26-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46b26-121">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="46b26-121">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





---
description: Konstruktormethode.
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Cunknown. cunknown-Konstruktor (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b500e7f12a2242b6c05367bc061f50680d2d608b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356386"
---
# <a name="cunknowncunknown-constructor"></a><span data-ttu-id="a3bb0-103">Cunknown. cunknown-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="a3bb0-103">CUnknown.CUnknown constructor</span></span>

<span data-ttu-id="a3bb0-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="a3bb0-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3bb0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3bb0-105">Syntax</span></span>


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="a3bb0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3bb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3bb0-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="a3bb0-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="a3bb0-108">Zeichenfolge, die den Namen des Objekts enthält. wird im [**cbaseobject**](cbaseobject.md) -Konstruktor für das Debuggen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3bb0-108">String containing the name of the object; used in the [**CBaseObject**](cbaseobject.md) constructor for debugging.</span></span>

</dd> <dt>

<span data-ttu-id="a3bb0-109">*Kro*</span><span class="sxs-lookup"><span data-stu-id="a3bb0-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="a3bb0-110">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="a3bb0-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="a3bb0-111">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die IUnknown-Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="a3bb0-111">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="a3bb0-112">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="a3bb0-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3bb0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3bb0-113">Remarks</span></span>

<span data-ttu-id="a3bb0-114">Das Objekt wird mit einem Verweis Zähler von NULL initialisiert.</span><span class="sxs-lookup"><span data-stu-id="a3bb0-114">The object is initialized with a reference count of zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3bb0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3bb0-115">Requirements</span></span>



| <span data-ttu-id="a3bb0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3bb0-116">Requirement</span></span> | <span data-ttu-id="a3bb0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a3bb0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3bb0-118">Header</span><span class="sxs-lookup"><span data-stu-id="a3bb0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a3bb0-119"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3bb0-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a3bb0-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a3bb0-120">Library</span></span><br/> | <dl> <span data-ttu-id="a3bb0-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a3bb0-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





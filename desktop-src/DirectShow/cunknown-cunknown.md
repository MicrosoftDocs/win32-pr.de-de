---
description: 'CUnknown.CUnknown-Konstruktor : Konstruktormethode.'
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: CUnknown.CUnknown-Konstruktor (Combase.h)
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
ms.openlocfilehash: 32859871f8ef69ce357fe204f0741356314fbb06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084608"
---
# <a name="cunknowncunknown-constructor"></a><span data-ttu-id="3a683-103">CUnknown.CUnknown-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="3a683-103">CUnknown.CUnknown constructor</span></span>

<span data-ttu-id="3a683-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="3a683-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a683-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a683-105">Syntax</span></span>


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="3a683-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a683-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a683-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="3a683-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3a683-108">Eine Zeichenfolge, die den Namen des Objekts enthält. wird im [**CBaseObject-Konstruktor zum**](cbaseobject.md) Debuggen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a683-108">String containing the name of the object; used in the [**CBaseObject**](cbaseobject.md) constructor for debugging.</span></span>

</dd> <dt>

<span data-ttu-id="3a683-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="3a683-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="3a683-110">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="3a683-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="3a683-111">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die IUnknown-Schnittstelle des aggregierenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="3a683-111">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="3a683-112">Legen Sie andernfalls diesen Parameter auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="3a683-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a683-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a683-113">Remarks</span></span>

<span data-ttu-id="3a683-114">Das -Objekt wird mit einem Verweiszähler von 0 (null) initialisiert.</span><span class="sxs-lookup"><span data-stu-id="3a683-114">The object is initialized with a reference count of zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a683-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a683-115">Requirements</span></span>



| <span data-ttu-id="3a683-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a683-116">Requirement</span></span> | <span data-ttu-id="3a683-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3a683-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a683-118">Header</span><span class="sxs-lookup"><span data-stu-id="3a683-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3a683-119"><dt>Combase.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a683-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3a683-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3a683-120">Library</span></span><br/> | <dl> <span data-ttu-id="3a683-121"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3a683-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





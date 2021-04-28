---
description: CMemAllocator.CMemAllocator-Konstruktor – Konstruktormethode.
ms.assetid: 2340b39a-cab6-4524-b8cd-b22d4bdd24d0
title: CMemAllocator.CMemAllocator-Konstruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1151572c32efe69cceb89e7a5ea5a045955b5f43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095398"
---
# <a name="cmemallocatorcmemallocator-constructor"></a><span data-ttu-id="0feb6-103">CMemAllocator.CMemAllocator-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="0feb6-103">CMemAllocator.CMemAllocator constructor</span></span>

<span data-ttu-id="0feb6-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="0feb6-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0feb6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0feb6-105">Syntax</span></span>


```C++
CMemAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="0feb6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0feb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0feb6-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="0feb6-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0feb6-108">Zeiger auf eine Zeichenfolge, die den Namen der Zuweisung enthält.</span><span class="sxs-lookup"><span data-stu-id="0feb6-108">Pointer to a string containing the name of the allocator.</span></span>

</dd> <dt>

<span data-ttu-id="0feb6-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="0feb6-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0feb6-110">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="0feb6-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="0feb6-111">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle** des aggregierenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="0feb6-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="0feb6-112">Legen Sie andernfalls diesen Parameter auf **NULL** fest.</span><span class="sxs-lookup"><span data-stu-id="0feb6-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0feb6-113">*Phr*</span><span class="sxs-lookup"><span data-stu-id="0feb6-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0feb6-114">Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="0feb6-114">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0feb6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0feb6-115">Requirements</span></span>



| <span data-ttu-id="0feb6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0feb6-116">Requirement</span></span> | <span data-ttu-id="0feb6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0feb6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0feb6-118">Header</span><span class="sxs-lookup"><span data-stu-id="0feb6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0feb6-119"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="0feb6-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0feb6-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0feb6-120">Library</span></span><br/> | <dl> <span data-ttu-id="0feb6-121"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0feb6-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0feb6-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0feb6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0feb6-123">**CMemAllocator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0feb6-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 





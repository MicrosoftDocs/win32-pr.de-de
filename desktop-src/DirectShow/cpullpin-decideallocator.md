---
description: Die decidezuzuordcator-Methode aushandiert eine Zuweisung mit der Ausgabepin.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: Cpullpin. decidezucator-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91ffa139b916b1594e0729a0f8d52f07c62eda12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371682"
---
# <a name="cpullpindecideallocator-method"></a><span data-ttu-id="41881-103">Cpullpin. decidezucator-Methode</span><span class="sxs-lookup"><span data-stu-id="41881-103">CPullPin.DecideAllocator method</span></span>

<span data-ttu-id="41881-104">Die- `DecideAllocator` Methode aushandiert eine Zuweisung mit der Ausgabepin.</span><span class="sxs-lookup"><span data-stu-id="41881-104">The `DecideAllocator` method negotiates an allocator with the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="41881-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="41881-105">Syntax</span></span>


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="41881-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="41881-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41881-107">*palloc*</span><span class="sxs-lookup"><span data-stu-id="41881-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="41881-108">Ein Zeiger auf die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle der bevorzugten Zuweisung der Eingabe-PIN oder **null**.</span><span class="sxs-lookup"><span data-stu-id="41881-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the input pin's preferred allocator, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="41881-109">*p-Eigenschaften*</span><span class="sxs-lookup"><span data-stu-id="41881-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="41881-110">Zeiger auf eine optionale [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die Puffer Anforderungen der Eingabe-PIN enthält.</span><span class="sxs-lookup"><span data-stu-id="41881-110">Pointer to an optional [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41881-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41881-111">Return value</span></span>

<span data-ttu-id="41881-112">Gibt \_ bei Erfolg S OK oder andernfalls einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="41881-112">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="41881-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41881-113">Remarks</span></span>

<span data-ttu-id="41881-114">Diese Methode ruft die Methode [**iasynkreader:: requestzuweisung**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) auf, um eine Zuweisung auszuhandeln.</span><span class="sxs-lookup"><span data-stu-id="41881-114">This method calls the [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) method to negotiate an allocator.</span></span> <span data-ttu-id="41881-115">Er übergibt den *palloc* -Parameter direkt an die **requestzuweisung** -Methode.</span><span class="sxs-lookup"><span data-stu-id="41881-115">It passes the *pAlloc* parameter directly to the **RequestAllocator** method.</span></span> <span data-ttu-id="41881-116">Der Parameter " *prequiers* " wird an **requestzuweisung** übergeben, wenn " *prequiors* " nicht **null** ist. Andernfalls wird eine **zuordnereigenschaftenstruktur \_** mit einer Standard Anforderung von drei 64-KB-Puffern erstellt.</span><span class="sxs-lookup"><span data-stu-id="41881-116">It passes the *pProps* parameter to **RequestAllocator** if *pProps* is non-**NULL**; otherwise, it creates an **ALLOCATOR\_PROPERTIES** structure with a default request of three 64K buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="41881-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41881-117">Requirements</span></span>



| <span data-ttu-id="41881-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41881-118">Requirement</span></span> | <span data-ttu-id="41881-119">Wert</span><span class="sxs-lookup"><span data-stu-id="41881-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41881-120">Header</span><span class="sxs-lookup"><span data-stu-id="41881-120">Header</span></span><br/>  | <dl> <span data-ttu-id="41881-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="41881-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="41881-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="41881-122">Library</span></span><br/> | <dl> <span data-ttu-id="41881-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="41881-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41881-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41881-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41881-125">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="41881-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> <dt>

[<span data-ttu-id="41881-126">**Cpullpin:: Connect**</span><span class="sxs-lookup"><span data-stu-id="41881-126">**CPullPin::Connect**</span></span>](cpullpin-connect.md)
</dt> </dl>

 

 





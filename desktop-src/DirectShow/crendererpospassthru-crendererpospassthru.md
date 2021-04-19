---
description: Konstruktormethode.
ms.assetid: 9d6f40ee-31bf-4334-bee5-4be834f1f269
title: Crendererpospassthru. crendererpospassthru-Konstruktor (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97b21ba3ad9438189f97c3e0bb9f011b210a0195
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359684"
---
# <a name="crendererpospassthrucrendererpospassthru-constructor"></a><span data-ttu-id="daa58-103">Crendererpospassthru. crendererpospassthru-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="daa58-103">CRendererPosPassThru.CRendererPosPassThru constructor</span></span>

<span data-ttu-id="daa58-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="daa58-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="daa58-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="daa58-105">Syntax</span></span>


```C++
CRendererPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="daa58-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="daa58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daa58-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="daa58-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="daa58-108">Zeiger auf den Namen des Objekts, zu Debuggingzwecken.</span><span class="sxs-lookup"><span data-stu-id="daa58-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="daa58-109">Weisen Sie diesen Parameter im statischen Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="daa58-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="daa58-110">*Kro*</span><span class="sxs-lookup"><span data-stu-id="daa58-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="daa58-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="daa58-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="daa58-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="daa58-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="daa58-113">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="daa58-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="daa58-114">*PHR*</span><span class="sxs-lookup"><span data-stu-id="daa58-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="daa58-115">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="daa58-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="daa58-116">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="daa58-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="daa58-117">*ppin*</span><span class="sxs-lookup"><span data-stu-id="daa58-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="daa58-118">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Eingabe-PIN des Filters.</span><span class="sxs-lookup"><span data-stu-id="daa58-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="daa58-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="daa58-119">Requirements</span></span>



| <span data-ttu-id="daa58-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="daa58-120">Requirement</span></span> | <span data-ttu-id="daa58-121">Wert</span><span class="sxs-lookup"><span data-stu-id="daa58-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daa58-122">Header</span><span class="sxs-lookup"><span data-stu-id="daa58-122">Header</span></span><br/>  | <dl> <span data-ttu-id="daa58-123"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="daa58-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="daa58-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="daa58-124">Library</span></span><br/> | <dl> <span data-ttu-id="daa58-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="daa58-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





---
description: Die Funktion "anatepospassthru" erstellt ein cpospassthru-Objekt oder ein crendererpospassthru-Objekt.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: Funktion "kreatepospassthru" (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePosPassThru
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08735a0bac2cc5aa8f5bb61461f10097435ad9c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361635"
---
# <a name="createpospassthru-function"></a><span data-ttu-id="51cc2-103">Funktion "kreatepospassthru"</span><span class="sxs-lookup"><span data-stu-id="51cc2-103">CreatePosPassThru function</span></span>

<span data-ttu-id="51cc2-104">Die- `CreatePosPassThru` Funktion erstellt ein [**cpospassthru**](cpospassthru.md) -Objekt oder ein [**crendererpospassthru**](crendererpospassthru.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="51cc2-104">The `CreatePosPassThru` function creates a [**CPosPassThru**](cpospassthru.md) object or [**CRendererPosPassThru**](crendererpospassthru.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="51cc2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="51cc2-105">Syntax</span></span>


```C++
STDAPI CreatePosPassThru(
   LPUNKNOWN pAgg,
   BOOL      bRenderer,
   IPin      *pPin,
   IUnknown  **ppPassThru
);
```



## <a name="parameters"></a><span data-ttu-id="51cc2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="51cc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51cc2-107">*pagg*</span><span class="sxs-lookup"><span data-stu-id="51cc2-107">*pAgg*</span></span> 
</dt> <dd>

<span data-ttu-id="51cc2-108">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="51cc2-108">Pointer to the owner of this object.</span></span> <span data-ttu-id="51cc2-109">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="51cc2-109">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="51cc2-110">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="51cc2-110">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="51cc2-111">*brenderer*</span><span class="sxs-lookup"><span data-stu-id="51cc2-111">*bRenderer*</span></span> 
</dt> <dd>

<span data-ttu-id="51cc2-112">Boolescher Wert, der angibt, ob der Filter ein Renderer ist.</span><span class="sxs-lookup"><span data-stu-id="51cc2-112">Boolean value that specifies whether the filter is a renderer.</span></span> <span data-ttu-id="51cc2-113">Verwenden Sie den Wert **true** , wenn der Filter ein Renderer ist, und andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="51cc2-113">Use the value **TRUE** if the filter is a renderer, or **FALSE** otherwise.</span></span> <span data-ttu-id="51cc2-114">Wenn der Wert **true** ist, erstellt diese Methode eine Instanz der [**crendererpospassthru**](crendererpospassthru.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="51cc2-114">If the value is **TRUE**, this method creates an instance of the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span> <span data-ttu-id="51cc2-115">Wenn der Wert **false** ist, erstellt die Methode eine Instanz der **cpospassthru** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="51cc2-115">If the value is **FALSE**, the method creates an instance of the **CPosPassThru** class.</span></span>

</dd> <dt>

<span data-ttu-id="51cc2-116">*ppin*</span><span class="sxs-lookup"><span data-stu-id="51cc2-116">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="51cc2-117">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle für die Eingabe-PIN des Filters.</span><span class="sxs-lookup"><span data-stu-id="51cc2-117">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface on the filter's input pin.</span></span>

</dd> <dt>

<span data-ttu-id="51cc2-118">*pppassthru*</span><span class="sxs-lookup"><span data-stu-id="51cc2-118">*ppPassThru*</span></span> 
</dt> <dd>

<span data-ttu-id="51cc2-119">Adresse einer Variablen, die einen Zeiger auf die **IUnknown** -Schnittstelle des Objekts empfängt.</span><span class="sxs-lookup"><span data-stu-id="51cc2-119">Address of a variable that receives a pointer to the object's **IUnknown** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51cc2-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51cc2-120">Return value</span></span>

<span data-ttu-id="51cc2-121">Gibt \_ bei Erfolg S OK zurück.</span><span class="sxs-lookup"><span data-stu-id="51cc2-121">Returns S\_OK if successful.</span></span> <span data-ttu-id="51cc2-122">Andernfalls wird ein **HRESULT** -Wert zurückgegeben, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="51cc2-122">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="51cc2-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51cc2-123">Remarks</span></span>

<span data-ttu-id="51cc2-124">Diese Methode verwendet die [**iseekingpassthru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) -Schnittstelle zum Erstellen des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="51cc2-124">This method uses the [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) interface to create the object.</span></span> <span data-ttu-id="51cc2-125">Das Objekt wird dynamisch aus Quartz.dll geladen.</span><span class="sxs-lookup"><span data-stu-id="51cc2-125">The object is loaded dynamically from Quartz.dll.</span></span>

<span data-ttu-id="51cc2-126">Wenn die Funktion erfolgreich ausgeführt wird, weist die zurückgegebene **IUnknown** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="51cc2-126">If the function succeeds, the returned **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="51cc2-127">Der Aufrufer muss die-Schnittstelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="51cc2-127">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="51cc2-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51cc2-128">Requirements</span></span>



| <span data-ttu-id="51cc2-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51cc2-129">Requirement</span></span> | <span data-ttu-id="51cc2-130">Wert</span><span class="sxs-lookup"><span data-stu-id="51cc2-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51cc2-131">Header</span><span class="sxs-lookup"><span data-stu-id="51cc2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="51cc2-132"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51cc2-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="51cc2-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="51cc2-133">Library</span></span><br/> | <dl> <span data-ttu-id="51cc2-134">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="51cc2-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51cc2-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51cc2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51cc2-136">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="51cc2-136">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





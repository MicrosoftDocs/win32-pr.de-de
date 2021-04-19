---
description: Die Init-Methode initialisiert das-Objekt.
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: CSeekingPassThru.Init-Methode (seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78176a6966f379240b5b7edd1ef5b73d7fa75b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370543"
---
# <a name="cseekingpassthruinit-method"></a><span data-ttu-id="c4f47-103">CSeekingPassThru.Init-Methode</span><span class="sxs-lookup"><span data-stu-id="c4f47-103">CSeekingPassThru.Init method</span></span>

<span data-ttu-id="c4f47-104">Die- `Init` Methode initialisiert das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c4f47-104">The `Init` method initializes the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4f47-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4f47-105">Syntax</span></span>


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="c4f47-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4f47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4f47-107">*bsupportrendering* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4f47-107">*bSupportRendering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4f47-108">Boolescher Wert, der angibt, ob der Filter ein Renderer ist.</span><span class="sxs-lookup"><span data-stu-id="c4f47-108">Boolean value that specifies whether the filter is a renderer.</span></span> <span data-ttu-id="c4f47-109">Verwenden Sie den Wert **true** , wenn der Filter ein Renderer ist, und andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="c4f47-109">Use the value **TRUE** if the filter is a renderer, or **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="c4f47-110">*ppin*</span><span class="sxs-lookup"><span data-stu-id="c4f47-110">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="c4f47-111">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle für die Eingabe-PIN des Filters.</span><span class="sxs-lookup"><span data-stu-id="c4f47-111">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface on the filter's input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4f47-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4f47-112">Return value</span></span>

<span data-ttu-id="c4f47-113">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c4f47-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="c4f47-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c4f47-114">Return code</span></span>                                                                                   | <span data-ttu-id="c4f47-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4f47-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="c4f47-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c4f47-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c4f47-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="c4f47-117">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="c4f47-118"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="c4f47-118"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="c4f47-119">Das Objekt wurde bereits initialisiert.</span><span class="sxs-lookup"><span data-stu-id="c4f47-119">Object was already initialized.</span></span><br/>         |
| <dl> <span data-ttu-id="c4f47-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="c4f47-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c4f47-121">Nicht genügend Arbeitsspeicher zum Erstellen des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c4f47-121">Not enough memory to create the object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c4f47-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4f47-122">Remarks</span></span>

<span data-ttu-id="c4f47-123">Wenn der Wert von *bsupportrendering* **true** ist, erstellt diese Methode eine Instanz der [**crendererpospassthru**](crendererpospassthru.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="c4f47-123">If the value of *bSupportRendering* is **TRUE**, this method creates an instance of the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span> <span data-ttu-id="c4f47-124">Andernfalls wird eine Instanz der [**cpospassthru**](cpospassthru.md) -Klasse erstellt.</span><span class="sxs-lookup"><span data-stu-id="c4f47-124">Otherwise, it creates an instance of the [**CPosPassThru**](cpospassthru.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4f47-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4f47-125">Requirements</span></span>



| <span data-ttu-id="c4f47-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4f47-126">Requirement</span></span> | <span data-ttu-id="c4f47-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c4f47-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4f47-128">Header</span><span class="sxs-lookup"><span data-stu-id="c4f47-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c4f47-129"><dt>Seekpt. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4f47-129"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c4f47-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c4f47-130">Library</span></span><br/> | <dl> <span data-ttu-id="c4f47-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c4f47-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4f47-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4f47-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4f47-133">**Cseekingpassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c4f47-133">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 





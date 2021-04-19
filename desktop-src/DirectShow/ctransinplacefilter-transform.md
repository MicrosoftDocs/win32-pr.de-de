---
description: Die Transform-Methode transformiert ein Beispiel direkt.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: Ctransinplacefilter. Transform-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5b84f326807f730745268a217b6066dacb9aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372511"
---
# <a name="ctransinplacefiltertransform-method"></a><span data-ttu-id="2c1e2-103">Ctransinplacefilter. Transform-Methode</span><span class="sxs-lookup"><span data-stu-id="2c1e2-103">CTransInPlaceFilter.Transform method</span></span>

<span data-ttu-id="2c1e2-104">Die- `Transform` Methode transformiert ein Beispiel direkt.</span><span class="sxs-lookup"><span data-stu-id="2c1e2-104">The `Transform` method transforms a sample in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c1e2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c1e2-105">Syntax</span></span>


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="2c1e2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c1e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c1e2-107">*psample*</span><span class="sxs-lookup"><span data-stu-id="2c1e2-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="2c1e2-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="2c1e2-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c1e2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c1e2-109">Return value</span></span>

<span data-ttu-id="2c1e2-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2c1e2-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2c1e2-111">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c1e2-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="2c1e2-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2c1e2-112">Return code</span></span>                                                                             | <span data-ttu-id="2c1e2-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c1e2-113">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="2c1e2-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2c1e2-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="2c1e2-115">Stellen Sie dieses Beispiel nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="2c1e2-115">Do not deliver this sample.</span></span><br/> |
| <dl> <span data-ttu-id="2c1e2-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2c1e2-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="2c1e2-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="2c1e2-117">Success.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="2c1e2-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c1e2-118">Remarks</span></span>

<span data-ttu-id="2c1e2-119">Diese Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="2c1e2-119">The derived class must implement this method.</span></span> <span data-ttu-id="2c1e2-120">Transformieren Sie die Beispiel Daten an Ort und Stelle.</span><span class="sxs-lookup"><span data-stu-id="2c1e2-120">Transform the sample data in place.</span></span> <span data-ttu-id="2c1e2-121">Wenn der Filter zwei Zuweisungen verwendet, kopiert er die Daten aus dem Eingabe Beispiel in ein neues Beispiel und übergibt die Kopie an diese Methode.</span><span class="sxs-lookup"><span data-stu-id="2c1e2-121">If the filter is using two allocators, it copies the data from the input sample to a new sample, and passes the copy to this method.</span></span>

<span data-ttu-id="2c1e2-122">Wenn der Filter dieses Beispiel nicht bereitstellt (z. b. zur Unterstützung der Qualitätskontrolle), sollte die Methode den Wert S false zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="2c1e2-122">If the filter should not deliver this sample (for example, to support quality control), the method should return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c1e2-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c1e2-123">Requirements</span></span>



| <span data-ttu-id="2c1e2-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c1e2-124">Requirement</span></span> | <span data-ttu-id="2c1e2-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2c1e2-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c1e2-126">Header</span><span class="sxs-lookup"><span data-stu-id="2c1e2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2c1e2-127"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c1e2-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2c1e2-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2c1e2-128">Library</span></span><br/> | <dl> <span data-ttu-id="2c1e2-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2c1e2-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c1e2-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c1e2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c1e2-131">**Ctransinplacefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2c1e2-131">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 





---
description: Die Transform-Methode transformiert ein Eingabe Beispiel, um ein Ausgabe Beispiel zu erhalten.
ms.assetid: 30ef8c0c-e834-481a-93ff-d06e6fa1ddeb
title: Ctransformfilter. Transform-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498a9a6ce266e0646dbbdcb4f322c093d6e0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351263"
---
# <a name="ctransformfiltertransform-method"></a><span data-ttu-id="9d635-103">Ctransformfilter. Transform-Methode</span><span class="sxs-lookup"><span data-stu-id="9d635-103">CTransformFilter.Transform method</span></span>

<span data-ttu-id="9d635-104">Die- `Transform` Methode transformiert ein Eingabe Beispiel, um ein Ausgabe Beispiel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9d635-104">The `Transform` method transforms an input sample to produce an output sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d635-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d635-105">Syntax</span></span>


```C++
virtual HRESULT Transform(
   IMediaSample *pIn,
   IMediaSample *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="9d635-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d635-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d635-107">*kehren*</span><span class="sxs-lookup"><span data-stu-id="9d635-107">*pIn*</span></span> 
</dt> <dd>

<span data-ttu-id="9d635-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle der Eingabe Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="9d635-108">Pointer to the input sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="9d635-109">*Schmollmund*</span><span class="sxs-lookup"><span data-stu-id="9d635-109">*pOut*</span></span> 
</dt> <dd>

<span data-ttu-id="9d635-110">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Ausgabe Beispiels.</span><span class="sxs-lookup"><span data-stu-id="9d635-110">Pointer to the output sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d635-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d635-111">Return value</span></span>

<span data-ttu-id="9d635-112">Die Basisklasse gibt "E unerwartete" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="9d635-112">The base class returns E\_UNEXPECTED.</span></span>

<span data-ttu-id="9d635-113">Die abgeleitete Klasse sollte einen **HRESULT** -Wert zurückgeben, der den Erfolg oder Misserfolg angibt.</span><span class="sxs-lookup"><span data-stu-id="9d635-113">The derived class should return an **HRESULT** value, indicating success or failure.</span></span> <span data-ttu-id="9d635-114">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d635-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="9d635-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9d635-115">Return code</span></span>                                                                             | <span data-ttu-id="9d635-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d635-116">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="9d635-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9d635-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="9d635-118">Stellen Sie dieses Beispiel nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="9d635-118">Do not deliver this sample.</span></span><br/> |
| <dl> <span data-ttu-id="9d635-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9d635-119"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="9d635-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="9d635-120">Success.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="9d635-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d635-121">Remarks</span></span>

<span data-ttu-id="9d635-122">Überschreiben Sie diese Methode, um Ausgabedaten zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="9d635-122">Override this method to produce output data.</span></span> <span data-ttu-id="9d635-123">Lesen Sie die Eingabedaten aus dem im *pIn* -Parameter angegebenen Beispiel, und schreiben Sie die neuen Daten in das durch den *Pout* -Parameter angegebene Beispiel.</span><span class="sxs-lookup"><span data-stu-id="9d635-123">Read the input data from the sample specified by the *pIn* parameter, and write the new data into the sample specified by the *pOut* parameter.</span></span>

<span data-ttu-id="9d635-124">Bevor der Filter diese Methode aufruft, werden die Eigenschaften aus dem Eingabe Beispiel in das Ausgabe Beispiel kopiert.</span><span class="sxs-lookup"><span data-stu-id="9d635-124">Before the filter calls this method, it copies the properties from the input sample to the output sample.</span></span> <span data-ttu-id="9d635-125">Die- `Transform` Methode sollte alle Eigenschaften festlegen, die sich zwischen den beiden Beispielen unterscheiden, mithilfe von **imediasample** -Methoden oder der [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) -Schnittstelle (falls verfügbar).</span><span class="sxs-lookup"><span data-stu-id="9d635-125">The `Transform` method should set any properties that differ between the two samples, using **IMediaSample** methods or the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface (if available).</span></span>

<span data-ttu-id="9d635-126">Wenn der Filter dieses Beispiel nicht bereitstellt (z. b. zur Unterstützung der Qualitätskontrolle), sollte die Methode den Wert S false zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="9d635-126">If the filter should not deliver this sample (for example, to support quality control), the method should return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d635-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d635-127">Requirements</span></span>



| <span data-ttu-id="9d635-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d635-128">Requirement</span></span> | <span data-ttu-id="9d635-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9d635-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d635-130">Header</span><span class="sxs-lookup"><span data-stu-id="9d635-130">Header</span></span><br/>  | <dl> <span data-ttu-id="9d635-131"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d635-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9d635-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d635-132">Library</span></span><br/> | <dl> <span data-ttu-id="9d635-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9d635-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d635-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d635-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d635-135">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9d635-135">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





---
description: 'CTransformInputPin.Receive-Methode: Die Receive-Methode empfängt das nächste Medienbeispiel im Stream. Diese Methode implementiert die IMemInputPin::Receive-Methode.'
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: CTransformInputPin.Receive-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a6a3c5dd4c9f11d45e1b719498d515a536e5ef8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084968"
---
# <a name="ctransforminputpinreceive-method"></a><span data-ttu-id="0c04c-104">CTransformInputPin.Receive-Methode</span><span class="sxs-lookup"><span data-stu-id="0c04c-104">CTransformInputPin.Receive method</span></span>

<span data-ttu-id="0c04c-105">Die `Receive` -Methode empfängt das nächste Medienbeispiel im Stream.</span><span class="sxs-lookup"><span data-stu-id="0c04c-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="0c04c-106">Diese Methode implementiert die [**IMemInputPin::Receive-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)</span><span class="sxs-lookup"><span data-stu-id="0c04c-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c04c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c04c-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="0c04c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c04c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c04c-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="0c04c-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="0c04c-110">Zeiger auf die [**IMediaSample-Schnittstelle des**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Beispiels.</span><span class="sxs-lookup"><span data-stu-id="0c04c-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c04c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c04c-111">Return value</span></span>

<span data-ttu-id="0c04c-112">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="0c04c-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0c04c-113">Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="0c04c-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0c04c-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0c04c-114">Return code</span></span>                                                                             | <span data-ttu-id="0c04c-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c04c-115">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="0c04c-116"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="0c04c-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="0c04c-117">Pin wird gerade geleert. Das Beispiel wurde abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="0c04c-117">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="0c04c-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0c04c-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="0c04c-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="0c04c-119">Success.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="0c04c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c04c-120">Remarks</span></span>

<span data-ttu-id="0c04c-121">Diese Methode ruft die [**CBaseInputPin::Receive-Methode**](cbaseinputpin-receive.md) des Pins auf, die den Streamingzustand des Pins überprüft und auf Formatänderungen im Medientyp überprüft.</span><span class="sxs-lookup"><span data-stu-id="0c04c-121">This method calls the pin's [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, which checks the pin's streaming state and checks for format changes in the media type.</span></span> <span data-ttu-id="0c04c-122">Anschließend wird die [**CTransformFilter::Receive-Methode**](ctransformfilter-receive.md) des Filters aufgerufen, die das Beispiel verarbeitet und nachgeschaltet übergibt.</span><span class="sxs-lookup"><span data-stu-id="0c04c-122">Then it calls the filter's [**CTransformFilter::Receive**](ctransformfilter-receive.md) method, which processes the sample and delivers it downstream.</span></span>

<span data-ttu-id="0c04c-123">Wenn der Filter nach der Rückgabe dieser Methode auf das Beispiel zugreifen muss, sollte er einen Verweiszähler durch Aufrufen der **IUnknown::AddRef-Methode** für das Beispiel besitzen.</span><span class="sxs-lookup"><span data-stu-id="0c04c-123">If the filter needs to access the sample after this method returns, it should hold a reference count by calling the **IUnknown::AddRef** method on the sample.</span></span> <span data-ttu-id="0c04c-124">Beispielsweise benötigen einige Decoderfilter das aktuelle Beispiel, um das nächste Beispiel zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="0c04c-124">For example, some decoder filters need the current sample in order to decode the next sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c04c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c04c-125">Requirements</span></span>



| <span data-ttu-id="0c04c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c04c-126">Requirement</span></span> | <span data-ttu-id="0c04c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0c04c-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c04c-128">Header</span><span class="sxs-lookup"><span data-stu-id="0c04c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0c04c-129"><dt>Transfrm.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="0c04c-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0c04c-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c04c-130">Library</span></span><br/> | <dl> <span data-ttu-id="0c04c-131"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0c04c-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





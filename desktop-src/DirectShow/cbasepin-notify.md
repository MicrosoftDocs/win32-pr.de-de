---
description: 'CBasePin.Notify-Methode: Die Notify-Methode benachrichtigt den Pin, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die IQualityControl::Notify-Methode.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: CBasePin.Notify-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35e751fb583010402df53e1a85eca11f751eda24
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096018"
---
# <a name="cbasepinnotify-method"></a><span data-ttu-id="f8ed1-104">CBasePin.Notify-Methode</span><span class="sxs-lookup"><span data-stu-id="f8ed1-104">CBasePin.Notify method</span></span>

<span data-ttu-id="f8ed1-105">Die `Notify` -Methode benachrichtigt den Pin, dass eine Qualitätsänderung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="f8ed1-106">Diese Methode implementiert die [**IQualityControl::Notify-Methode.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)</span><span class="sxs-lookup"><span data-stu-id="f8ed1-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ed1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8ed1-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="f8ed1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8ed1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8ed1-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="f8ed1-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="f8ed1-110">Zeiger auf die [**IBaseFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) des Filters, der die Qualitätskontrollmeldung übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="f8ed1-111">*Q*</span><span class="sxs-lookup"><span data-stu-id="f8ed1-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="f8ed1-112">Gibt eine [**Quality-Struktur**](/windows/win32/api/strmif/ns-strmif-quality) an, die die Qualitätskontrollmeldung enthält.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-112">Specifies a [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8ed1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8ed1-113">Return value</span></span>

<span data-ttu-id="f8ed1-114">Die Basisklasse gibt E \_ NOTIMPL zurück.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-114">The base class returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ed1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8ed1-115">Remarks</span></span>

<span data-ttu-id="f8ed1-116">Ausgabepins sollten diese Methode überschreiben, um Qualitätskontrollmeldungen zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-116">Output pins should override this method to accept quality-control messages.</span></span>

<span data-ttu-id="f8ed1-117">Wenn ein externer Qualitäts-Manager installiert wurde (siehe [**CBasePin::SetSink),**](cbasepin-setsink.md)übergeben Sie die Nachricht an diesen Qualitäts-Manager.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-117">If an external quality manager was installed (see [**CBasePin::SetSink**](cbasepin-setsink.md)), pass the message to that quality manager.</span></span> <span data-ttu-id="f8ed1-118">Andernfalls sollte der Filter die Nachricht selbst verarbeiten oder die Nachricht upstream übergeben.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-118">Otherwise, the filter should handle the message itself, or pass the message upstream.</span></span> <span data-ttu-id="f8ed1-119">Weitere Informationen finden Sie unter [Qualitätskontrollverwaltung.](quality-control-management.md)</span><span class="sxs-lookup"><span data-stu-id="f8ed1-119">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ed1-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8ed1-120">Requirements</span></span>



| <span data-ttu-id="f8ed1-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8ed1-121">Requirement</span></span> | <span data-ttu-id="f8ed1-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f8ed1-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ed1-123">Header</span><span class="sxs-lookup"><span data-stu-id="f8ed1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f8ed1-124"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f8ed1-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f8ed1-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f8ed1-125">Library</span></span><br/> | <dl> <span data-ttu-id="f8ed1-126"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f8ed1-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8ed1-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f8ed1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ed1-128">**CBasePin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f8ed1-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





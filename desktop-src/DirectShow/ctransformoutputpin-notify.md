---
description: 'CTransformOutputPin.Notify-Methode: Die Notify-Methode benachrichtigt den Pin, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die IQualityControl::Notify-Methode.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: CTransformOutputPin.Notify-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a55e493c737b5a5864ec0a8dd38eee3abbfa586
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084808"
---
# <a name="ctransformoutputpinnotify-method"></a><span data-ttu-id="fa877-104">CTransformOutputPin.Notify-Methode</span><span class="sxs-lookup"><span data-stu-id="fa877-104">CTransformOutputPin.Notify method</span></span>

<span data-ttu-id="fa877-105">Die `Notify` -Methode benachrichtigt den Pin, dass eine Qualitätsänderung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="fa877-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="fa877-106">Diese Methode implementiert die [**IQualityControl::Notify-Methode.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)</span><span class="sxs-lookup"><span data-stu-id="fa877-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa877-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa877-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="fa877-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa877-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa877-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="fa877-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="fa877-110">Zeiger auf die [**IBaseFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) des Filters, der die Qualitätskontrollnachricht übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="fa877-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality control message.</span></span>

</dd> <dt>

<span data-ttu-id="fa877-111">*Q*</span><span class="sxs-lookup"><span data-stu-id="fa877-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="fa877-112">[**Qualitätsstruktur,**](/windows/win32/api/strmif/ns-strmif-quality) die die Qualitätskontrollmeldung enthält.</span><span class="sxs-lookup"><span data-stu-id="fa877-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa877-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa877-113">Return value</span></span>

<span data-ttu-id="fa877-114">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="fa877-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fa877-115">Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="fa877-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="fa877-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fa877-116">Return code</span></span>                                                                                       | <span data-ttu-id="fa877-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa877-117">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="fa877-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa877-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="fa877-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="fa877-119">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="fa877-120"><dt>**VFW \_ E \_ NICHT \_ GEFUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="fa877-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="fa877-121">Es wurde kein Objekt zum Akzeptieren der Nachricht finden.</span><span class="sxs-lookup"><span data-stu-id="fa877-121">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fa877-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa877-122">Remarks</span></span>

<span data-ttu-id="fa877-123">Diese Methode ruft die [**CTransformFilter::AlterQuality-Methode**](ctransformfilter-alterquality.md) des Filters auf.</span><span class="sxs-lookup"><span data-stu-id="fa877-123">This method calls the filter's [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span> <span data-ttu-id="fa877-124">Wenn der Filter die Qualitätsnachricht nicht verarbeitet, ruft diese Methode die [**CBaseInputPin::P assNotify-Methode**](cbaseinputpin-passnotify.md) auf dem Eingabepin des Filters auf.</span><span class="sxs-lookup"><span data-stu-id="fa877-124">If the filter does not handle the quality message, this method calls the [**CBaseInputPin::PassNotify**](cbaseinputpin-passnotify.md) method on the filter's input pin.</span></span> <span data-ttu-id="fa877-125">Die **PassNotify-Methode** übergibt die Qualitätsmeldung upstream (oder an einen benutzerdefinierten Qualitäts-Manager, sofern installiert).</span><span class="sxs-lookup"><span data-stu-id="fa877-125">The **PassNotify** method passes the quality message upstream (or to a custom quality manager, if one was installed).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa877-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa877-126">Requirements</span></span>



| <span data-ttu-id="fa877-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa877-127">Requirement</span></span> | <span data-ttu-id="fa877-128">Wert</span><span class="sxs-lookup"><span data-stu-id="fa877-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa877-129">Header</span><span class="sxs-lookup"><span data-stu-id="fa877-129">Header</span></span><br/>  | <dl> <span data-ttu-id="fa877-130"><dt>Transfrm.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="fa877-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fa877-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fa877-131">Library</span></span><br/> | <dl> <span data-ttu-id="fa877-132"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fa877-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





---
description: 'Die Benachrichtigungs Methode benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die iqualitycontrol:: Notify-Methode.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: Ctransformoutputpin. Notify-Methode (Transfrm. h)
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
ms.openlocfilehash: d6ace7e25f1413f6e17a4d19ef937732ea8c689a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371245"
---
# <a name="ctransformoutputpinnotify-method"></a><span data-ttu-id="51206-104">Ctransformoutputpin. Notify-Methode</span><span class="sxs-lookup"><span data-stu-id="51206-104">CTransformOutputPin.Notify method</span></span>

<span data-ttu-id="51206-105">Die- `Notify` Methode benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="51206-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="51206-106">Diese Methode implementiert die [**iqualitycontrol:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) -Methode.</span><span class="sxs-lookup"><span data-stu-id="51206-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51206-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="51206-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="51206-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="51206-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51206-109">*pself*</span><span class="sxs-lookup"><span data-stu-id="51206-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="51206-110">Ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Filters, der die Qualitäts Steuerungs Meldung übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="51206-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality control message.</span></span>

</dd> <dt>

<span data-ttu-id="51206-111">*Q1*</span><span class="sxs-lookup"><span data-stu-id="51206-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="51206-112">[**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur, die die Qualitäts Steuerungs Meldung enthält.</span><span class="sxs-lookup"><span data-stu-id="51206-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51206-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51206-113">Return value</span></span>

<span data-ttu-id="51206-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="51206-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="51206-115">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="51206-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="51206-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="51206-116">Return code</span></span>                                                                                       | <span data-ttu-id="51206-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51206-117">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="51206-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="51206-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="51206-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="51206-119">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="51206-120"><dt>**VFW \_ E \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="51206-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="51206-121">Es konnte kein Objekt gefunden werden, um die Nachricht zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="51206-121">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="51206-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51206-122">Remarks</span></span>

<span data-ttu-id="51206-123">Diese Methode ruft die [**ctransformfilter:: alterquality**](ctransformfilter-alterquality.md) -Methode des Filters auf.</span><span class="sxs-lookup"><span data-stu-id="51206-123">This method calls the filter's [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span> <span data-ttu-id="51206-124">Wenn der Filter die Qualitäts Meldung nicht verarbeitet, ruft diese Methode die [**cbaseinputpin::P assnotify**](cbaseinputpin-passnotify.md) -Methode für die Eingabe-PIN des Filters auf.</span><span class="sxs-lookup"><span data-stu-id="51206-124">If the filter does not handle the quality message, this method calls the [**CBaseInputPin::PassNotify**](cbaseinputpin-passnotify.md) method on the filter's input pin.</span></span> <span data-ttu-id="51206-125">Die **passnotify** -Methode übergibt den upstreamnachrichten-Upstreamdienst (oder an einen benutzerdefinierten Quality Manager, wenn eine installiert wurde).</span><span class="sxs-lookup"><span data-stu-id="51206-125">The **PassNotify** method passes the quality message upstream (or to a custom quality manager, if one was installed).</span></span>

## <a name="requirements"></a><span data-ttu-id="51206-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51206-126">Requirements</span></span>



| <span data-ttu-id="51206-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51206-127">Requirement</span></span> | <span data-ttu-id="51206-128">Wert</span><span class="sxs-lookup"><span data-stu-id="51206-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51206-129">Header</span><span class="sxs-lookup"><span data-stu-id="51206-129">Header</span></span><br/>  | <dl> <span data-ttu-id="51206-130"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51206-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="51206-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="51206-131">Library</span></span><br/> | <dl> <span data-ttu-id="51206-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="51206-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





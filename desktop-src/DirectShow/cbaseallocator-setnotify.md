---
description: 'Die setnotify-Methode legt einen Rückruf für die Zuweisung fest oder entfernt ihn. Die Zuweisung Ruft die Rückruf Methode auf, wenn die imemzuzuordcator:: ReleaseBuffer-Methode der Zuweisung aufgerufen wird.'
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: Cbasezucator. setnotify-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8269112325d470cae59cff6e615f04fbdfab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360986"
---
# <a name="cbaseallocatorsetnotify-method"></a><span data-ttu-id="199a3-104">Cbasezucator. setnotify-Methode</span><span class="sxs-lookup"><span data-stu-id="199a3-104">CBaseAllocator.SetNotify method</span></span>

<span data-ttu-id="199a3-105">\[[**Setnotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) kann in nachfolgenden Versionen geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="199a3-105">\[[**SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="199a3-106">Die- `SetNotify` Methode legt einen Rückruf für die Zuweisung fest oder entfernt ihn.</span><span class="sxs-lookup"><span data-stu-id="199a3-106">The `SetNotify` method sets or removes a callback on the allocator.</span></span> <span data-ttu-id="199a3-107">Die Zuweisung Ruft die Rückruf Methode auf, wenn die [**imemzuzuordcator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) -Methode der Zuweisung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="199a3-107">The allocator calls the callback method whenever the allocator's [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="199a3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="199a3-108">Syntax</span></span>


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a><span data-ttu-id="199a3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="199a3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="199a3-110">*pnotify*</span><span class="sxs-lookup"><span data-stu-id="199a3-110">*pNotify*</span></span> 
</dt> <dd>

<span data-ttu-id="199a3-111">Ein Zeiger auf die Schnittstelle [**imemzucallbacktemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) , die für den Rückruf verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="199a3-111">Pointer to the [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) interface that will be used for the callback.</span></span> <span data-ttu-id="199a3-112">Der Aufrufer muss die-Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="199a3-112">The caller must implement the interface.</span></span> <span data-ttu-id="199a3-113">Verwenden Sie den Wert **null** , um den Rückruf zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="199a3-113">Use the value **NULL** to remove the callback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="199a3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="199a3-114">Return value</span></span>

<span data-ttu-id="199a3-115">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="199a3-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="199a3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="199a3-116">Remarks</span></span>

<span data-ttu-id="199a3-117">Diese Methode implementiert die [**imemzuzucallorcallbacktemp:: setnotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) -Methode.</span><span class="sxs-lookup"><span data-stu-id="199a3-117">This method implements the [**IMemAllocatorCallbackTemp::SetNotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) method.</span></span> <span data-ttu-id="199a3-118">[**Die Zuweisung**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) wird von der Zuweisung nicht verfügbar gemacht, es sei denn, das *fenablereleasecallback* -Flag ist im [**cbasezucator**](cbaseallocator.md) -Konstruktor auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="199a3-118">The allocator does not expose the [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) interface unless the *fEnableReleaseCallback* flag is set to **TRUE** in the [**CBaseAllocator**](cbaseallocator.md) constructor.</span></span>

<span data-ttu-id="199a3-119">Diese Methode legt die [**cbasezucator:: m \_ pnotify**](cbaseallocator-m-pnotify.md) -Member-Variable auf *pnotify* fest und erhöht den Verweis Zähler für die Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="199a3-119">This method sets the [**CBaseAllocator::m\_pNotify**](cbaseallocator-m-pnotify.md) member variable equal to *pNotify* and increments the reference count on the interface.</span></span> <span data-ttu-id="199a3-120">Wenn *m \_ pnotify* nicht **null** ist, ruft die **ReleaseBuffer** -Methode des zuordcators [**imemzucatornotifycallbacktemp:: notifyrelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease)auf.</span><span class="sxs-lookup"><span data-stu-id="199a3-120">If *m\_pNotify* is non-**NULL**, the allocator's **ReleaseBuffer** method calls [**IMemAllocatorNotifyCallbackTemp::NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease).</span></span> <span data-ttu-id="199a3-121">Weitere Informationen zum Implementieren des Rückrufs finden Sie im Abschnitt "Hinweise" in dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="199a3-121">See the Remarks section in that method for information about implementing the callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="199a3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="199a3-122">Requirements</span></span>



| <span data-ttu-id="199a3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="199a3-123">Requirement</span></span> | <span data-ttu-id="199a3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="199a3-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="199a3-125">Header</span><span class="sxs-lookup"><span data-stu-id="199a3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="199a3-126"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="199a3-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="199a3-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="199a3-127">Library</span></span><br/> | <dl> <span data-ttu-id="199a3-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="199a3-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="199a3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="199a3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="199a3-130">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="199a3-130">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 





---
description: Konstruktormethode.
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Cbasecontrolvideo. cbasecontrolvideo-Konstruktor (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dea0548079f8eb703f0c17557cab6a5e634cf242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356457"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a><span data-ttu-id="72364-103">Cbasecontrolvideo. cbasecontrolvideo-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="72364-103">CBaseControlVideo.CBaseControlVideo constructor</span></span>

<span data-ttu-id="72364-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="72364-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="72364-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="72364-105">Syntax</span></span>


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="72364-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72364-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72364-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="72364-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="72364-108">Zeiger auf das besitzende Medienfilter Objekt.</span><span class="sxs-lookup"><span data-stu-id="72364-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="72364-109">*pinterfakelock*</span><span class="sxs-lookup"><span data-stu-id="72364-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="72364-110">Zeiger auf den kritischen Abschnitt, der zum Sperren verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72364-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="72364-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="72364-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="72364-112">Zeiger auf die Objektbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="72364-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="72364-113">*Kro*</span><span class="sxs-lookup"><span data-stu-id="72364-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="72364-114">Ein Zeiger auf die steuernde **IUnknown** -Schnittstelle, wenn das Objekt Teil eines Aggregats ist. Andernfalls muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="72364-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="72364-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="72364-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="72364-116">Ein Zeiger auf eine Variable, die einen HRESULT-Wert empfängt, der angibt, ob die Konstruktormethode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="72364-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72364-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72364-117">Remarks</span></span>

<span data-ttu-id="72364-118">Das-Objekt implementiert die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Steuerelement Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="72364-118">The object implements the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) control interface.</span></span>

<span data-ttu-id="72364-119">Alle Schnittstellen Methoden aus [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) , die von dieser Klasse implementiert werden, erfordern, dass der Filter ordnungsgemäß verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="72364-119">All the interface methods from [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) that this class implements require that the filter be connected correctly.</span></span> <span data-ttu-id="72364-120">Aus diesem Grund wird der Klasse eine PIN übergeben, mit der Sie synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="72364-120">For this reason, the class is passed a pin with which it should synchronize with.</span></span> <span data-ttu-id="72364-121">Wenn eine Schnittstellen Methode aufgerufen wird, bestimmt das Objekt, dass die PIN noch verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="72364-121">Whenever an interface method is called, the object determines that the pin is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="72364-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72364-122">Requirements</span></span>



| <span data-ttu-id="72364-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72364-123">Requirement</span></span> | <span data-ttu-id="72364-124">Wert</span><span class="sxs-lookup"><span data-stu-id="72364-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72364-125">Header</span><span class="sxs-lookup"><span data-stu-id="72364-125">Header</span></span><br/>  | <dl> <span data-ttu-id="72364-126"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72364-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="72364-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="72364-127">Library</span></span><br/> | <dl> <span data-ttu-id="72364-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="72364-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72364-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72364-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72364-130">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="72364-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





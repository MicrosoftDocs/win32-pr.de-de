---
description: Konstruktormethode.
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: Cmediaevent. cmediaevent-Konstruktor (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.CMediaEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77b87fa589728592874b0dea96f7b6efca501471
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354168"
---
# <a name="cmediaeventcmediaevent-constructor"></a><span data-ttu-id="17f51-103">Cmediaevent. cmediaevent-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="17f51-103">CMediaEvent.CMediaEvent constructor</span></span>

<span data-ttu-id="17f51-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="17f51-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="17f51-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17f51-105">Syntax</span></span>


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="17f51-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17f51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17f51-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="17f51-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="17f51-108">Zeiger auf den Namen des Objekts zu Debuggingzwecken.</span><span class="sxs-lookup"><span data-stu-id="17f51-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="17f51-109">*Kro*</span><span class="sxs-lookup"><span data-stu-id="17f51-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="17f51-110">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="17f51-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17f51-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17f51-111">Remarks</span></span>

<span data-ttu-id="17f51-112">Weisen Sie den *PName* -Parameter im statischen Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="17f51-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="17f51-113">Dieser Name wird beim Erstellen und Löschen des Objekts im Terminal Debuggen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17f51-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="17f51-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17f51-114">Requirements</span></span>



| <span data-ttu-id="17f51-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17f51-115">Requirement</span></span> | <span data-ttu-id="17f51-116">Wert</span><span class="sxs-lookup"><span data-stu-id="17f51-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f51-117">Header</span><span class="sxs-lookup"><span data-stu-id="17f51-117">Header</span></span><br/>  | <dl> <span data-ttu-id="17f51-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17f51-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="17f51-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="17f51-119">Library</span></span><br/> | <dl> <span data-ttu-id="17f51-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="17f51-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17f51-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17f51-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f51-122">**Cmediaevent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="17f51-122">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 





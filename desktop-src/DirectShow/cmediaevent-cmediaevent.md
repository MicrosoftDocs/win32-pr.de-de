---
description: 'CMediaEvent.CMediaEvent-Konstruktor : Konstruktormethode.'
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: CMediaEvent.CMediaEvent-Konstruktor (Ctlutil.h)
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
ms.openlocfilehash: 36cd82b086241012542701001c4de1fe16ac2d8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095558"
---
# <a name="cmediaeventcmediaevent-constructor"></a><span data-ttu-id="ffc7a-103">CMediaEvent.CMediaEvent-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="ffc7a-103">CMediaEvent.CMediaEvent constructor</span></span>

<span data-ttu-id="ffc7a-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ffc7a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffc7a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffc7a-105">Syntax</span></span>


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="ffc7a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffc7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffc7a-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="ffc7a-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ffc7a-108">Zeiger auf den Namen des Objekts zu Debugzwecken.</span><span class="sxs-lookup"><span data-stu-id="ffc7a-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="ffc7a-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="ffc7a-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ffc7a-110">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="ffc7a-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffc7a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffc7a-111">Remarks</span></span>

<span data-ttu-id="ffc7a-112">Ordnen Sie den *pName-Parameter* im statischen Speicher zu.</span><span class="sxs-lookup"><span data-stu-id="ffc7a-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="ffc7a-113">Dieser Name wird beim Erstellen und Löschen des Objekts im Debugterminal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ffc7a-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffc7a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffc7a-114">Requirements</span></span>



| <span data-ttu-id="ffc7a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffc7a-115">Requirement</span></span> | <span data-ttu-id="ffc7a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ffc7a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffc7a-117">Header</span><span class="sxs-lookup"><span data-stu-id="ffc7a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ffc7a-118"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc7a-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ffc7a-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ffc7a-119">Library</span></span><br/> | <dl> <span data-ttu-id="ffc7a-120"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc7a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffc7a-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ffc7a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffc7a-122">**CMediaEvent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ffc7a-122">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 





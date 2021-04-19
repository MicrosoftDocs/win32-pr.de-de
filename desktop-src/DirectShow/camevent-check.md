---
description: Die Check-Methode überprüft, ob das Ereignis festgelegt ist, ohne zu blockieren.
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: Camevent. Check-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Check
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a112d1b9484acb4d7e9cc2992b8dee629f40e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367437"
---
# <a name="cameventcheck-method"></a><span data-ttu-id="0b74e-103">Camevent. Check-Methode</span><span class="sxs-lookup"><span data-stu-id="0b74e-103">CAMEvent.Check method</span></span>

<span data-ttu-id="0b74e-104">Die- `Check` Methode überprüft, ob das Ereignis festgelegt ist, ohne zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="0b74e-104">The `Check` method checks whether the event is set, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b74e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b74e-105">Syntax</span></span>


```C++
BOOL Check();
```



## <a name="parameters"></a><span data-ttu-id="0b74e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b74e-106">Parameters</span></span>

<span data-ttu-id="0b74e-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0b74e-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b74e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b74e-108">Remarks</span></span>

<span data-ttu-id="0b74e-109">Gibt " **true** " zurück, wenn das Ereignis festgelegt ist, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="0b74e-109">Returns **TRUE** if the event is set, or **FALSE** otherwise.</span></span> <span data-ttu-id="0b74e-110">Diese Methode ruft die Methode " [**camevent:: Wait**](camevent-wait.md) " mit einem Timeout von 0 (null) auf.</span><span class="sxs-lookup"><span data-stu-id="0b74e-110">This method calls the [**CAMEvent::Wait**](camevent-wait.md) method with a time-out of zero.</span></span> <span data-ttu-id="0b74e-111">Wenn das Objekt ein automatisches Zurücksetzungs Ereignis ist, setzt diese Methode das Ereignis zurück.</span><span class="sxs-lookup"><span data-stu-id="0b74e-111">If the object is an auto-reset event, this method resets the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b74e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b74e-112">Requirements</span></span>



| <span data-ttu-id="0b74e-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b74e-113">Requirement</span></span> | <span data-ttu-id="0b74e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="0b74e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b74e-115">Header</span><span class="sxs-lookup"><span data-stu-id="0b74e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="0b74e-116"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b74e-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0b74e-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0b74e-117">Library</span></span><br/> | <dl> <span data-ttu-id="0b74e-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0b74e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b74e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b74e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b74e-120">**Camevent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0b74e-120">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 





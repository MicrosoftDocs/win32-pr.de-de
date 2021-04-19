---
description: Die changestart-Methode wird aufgerufen, wenn sich die Startposition ändert.
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: Csourceseeking. changestart-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0a2751cf0ad1ecc6fddeeffd97b97c32b4a31b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367191"
---
# <a name="csourceseekingchangestart-method"></a><span data-ttu-id="bcbe2-103">Csourceseeking. changestart-Methode</span><span class="sxs-lookup"><span data-stu-id="bcbe2-103">CSourceSeeking.ChangeStart method</span></span>

<span data-ttu-id="bcbe2-104">Die- `ChangeStart` Methode wird aufgerufen, wenn sich die Startposition ändert.</span><span class="sxs-lookup"><span data-stu-id="bcbe2-104">The `ChangeStart` method is called when the start position changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcbe2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcbe2-105">Syntax</span></span>


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a><span data-ttu-id="bcbe2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcbe2-106">Parameters</span></span>

<span data-ttu-id="bcbe2-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bcbe2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bcbe2-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bcbe2-108">Return value</span></span>

<span data-ttu-id="bcbe2-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bcbe2-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcbe2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bcbe2-110">Remarks</span></span>

<span data-ttu-id="bcbe2-111">Die [**csourceseeking:: setpositions**](csourceseeking-setpositions.md) -Methode ruft diese Methode auf, wenn sich die Startposition ändert.</span><span class="sxs-lookup"><span data-stu-id="bcbe2-111">The [**CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) method calls this method if the start position changes.</span></span> <span data-ttu-id="bcbe2-112">Diese Methode ist rein virtuell. Diese Klasse muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="bcbe2-112">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="bcbe2-113">Nach einem Suchvorgang sollten Zeitstempel von Null neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="bcbe2-113">After a seek operation, time stamps should restart from zero.</span></span> <span data-ttu-id="bcbe2-114">Medien Zeiten sollten die neue Startzeit widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="bcbe2-114">Media times should reflect the new start time.</span></span> <span data-ttu-id="bcbe2-115">Das folgende Beispiel zeigt eine mögliche Implementierung:</span><span class="sxs-lookup"><span data-stu-id="bcbe2-115">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeStart( )
{
    m_rtSampleTime = 0;          // Reset the time stamps.
    m_rtMediaTime = m_rtStart;   // Reset the media times.
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="bcbe2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bcbe2-116">Requirements</span></span>



| <span data-ttu-id="bcbe2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bcbe2-117">Requirement</span></span> | <span data-ttu-id="bcbe2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bcbe2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbe2-119">Header</span><span class="sxs-lookup"><span data-stu-id="bcbe2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bcbe2-120"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bcbe2-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bcbe2-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bcbe2-121">Library</span></span><br/> | <dl> <span data-ttu-id="bcbe2-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bcbe2-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcbe2-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcbe2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcbe2-124">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bcbe2-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





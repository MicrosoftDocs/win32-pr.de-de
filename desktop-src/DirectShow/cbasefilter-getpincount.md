---
description: 'CBaseFilter.GetPinCount-Methode: Die GetPinCount-Methode ruft die Anzahl der Stecknadeln ab.'
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: CBaseFilter.GetPinCount-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0081b4cec45ed4cac5b4f0883032631983824cec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099788"
---
# <a name="cbasefiltergetpincount-method"></a><span data-ttu-id="c875f-103">CBaseFilter.GetPinCount-Methode</span><span class="sxs-lookup"><span data-stu-id="c875f-103">CBaseFilter.GetPinCount method</span></span>

<span data-ttu-id="c875f-104">Die `GetPinCount` -Methode ruft die Anzahl der Stecknadeln ab.</span><span class="sxs-lookup"><span data-stu-id="c875f-104">The `GetPinCount` method retrieves the number of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="c875f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c875f-105">Syntax</span></span>


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a><span data-ttu-id="c875f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c875f-106">Parameters</span></span>

<span data-ttu-id="c875f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c875f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c875f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c875f-108">Return value</span></span>

<span data-ttu-id="c875f-109">Gibt die Anzahl der Stecknadeln zurück.</span><span class="sxs-lookup"><span data-stu-id="c875f-109">Returns the number of pins.</span></span>

## <a name="remarks"></a><span data-ttu-id="c875f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c875f-110">Remarks</span></span>

<span data-ttu-id="c875f-111">Die abgeleitete Klasse muss diese rein virtuelle Methode implementieren.</span><span class="sxs-lookup"><span data-stu-id="c875f-111">The derived class must implement this pure virtual method.</span></span> <span data-ttu-id="c875f-112">Gibt die Anzahl der Pins zurück, die derzeit für diesen Filter verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c875f-112">Return the number of pins that are currently available on this filter.</span></span> <span data-ttu-id="c875f-113">Filter können Pins dynamisch erstellen oder zerstören.</span><span class="sxs-lookup"><span data-stu-id="c875f-113">Filters can dynamically create or destroy pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="c875f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c875f-114">Requirements</span></span>



| <span data-ttu-id="c875f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c875f-115">Requirement</span></span> | <span data-ttu-id="c875f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c875f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c875f-117">Header</span><span class="sxs-lookup"><span data-stu-id="c875f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c875f-118"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="c875f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c875f-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c875f-119">Library</span></span><br/> | <dl> <span data-ttu-id="c875f-120"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c875f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c875f-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c875f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c875f-122">**CBaseFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c875f-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 





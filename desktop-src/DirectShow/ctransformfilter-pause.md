---
description: 'CTransformFilter.Pause-Methode: Die Pause-Methode hält den Filter an. Diese Methode implementiert die IMediaFilter::P ause-Methode.'
ms.assetid: 3e3afd14-1c92-4f2b-a367-e10caaeb3b63
title: CTransformFilter.Pause-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 903522b63754ff7972e4cdcf5221946442497896
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095098"
---
# <a name="ctransformfilterpause-method"></a><span data-ttu-id="121a6-104">CTransformFilter.Pause-Methode</span><span class="sxs-lookup"><span data-stu-id="121a6-104">CTransformFilter.Pause method</span></span>

<span data-ttu-id="121a6-105">Die `Pause` -Methode hält den Filter an.</span><span class="sxs-lookup"><span data-stu-id="121a6-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="121a6-106">Diese Methode implementiert die [**IMediaFilter::P ause-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause)</span><span class="sxs-lookup"><span data-stu-id="121a6-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="121a6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="121a6-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="121a6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="121a6-108">Parameters</span></span>

<span data-ttu-id="121a6-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="121a6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="121a6-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="121a6-110">Return value</span></span>

<span data-ttu-id="121a6-111">Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="121a6-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="121a6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="121a6-112">Remarks</span></span>

<span data-ttu-id="121a6-113">Diese Methode ruft die [**StartStreaming-Methode**](ctransformfilter-startstreaming.md) auf.</span><span class="sxs-lookup"><span data-stu-id="121a6-113">This method calls the [**StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span> <span data-ttu-id="121a6-114">Die **StartStreaming-Methode** führt in der Basisklasse nichts aus, aber die abgeleitete Klasse kann sie überschreiben.</span><span class="sxs-lookup"><span data-stu-id="121a6-114">The **StartStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="121a6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="121a6-115">Requirements</span></span>



| <span data-ttu-id="121a6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="121a6-116">Requirement</span></span> | <span data-ttu-id="121a6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="121a6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="121a6-118">Header</span><span class="sxs-lookup"><span data-stu-id="121a6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="121a6-119"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="121a6-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="121a6-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="121a6-120">Library</span></span><br/> | <dl> <span data-ttu-id="121a6-121"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="121a6-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="121a6-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="121a6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="121a6-123">**CTransformFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="121a6-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





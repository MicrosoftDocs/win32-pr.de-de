---
description: 'CBaseFilter.Pause-Methode: Die Pause-Methode hält den Filter an. Diese Methode implementiert die IMediaFilter::P ause-Methode.'
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: CBaseFilter.Pause-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee91393a574d0135e66e5a9c1e1e6b0325a0b4de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120088"
---
# <a name="cbasefilterpause-method"></a><span data-ttu-id="cf683-104">CBaseFilter.Pause-Methode</span><span class="sxs-lookup"><span data-stu-id="cf683-104">CBaseFilter.Pause method</span></span>

<span data-ttu-id="cf683-105">Die `Pause` -Methode hält den Filter an.</span><span class="sxs-lookup"><span data-stu-id="cf683-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="cf683-106">Diese Methode implementiert die [**IMediaFilter::P ause-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause)</span><span class="sxs-lookup"><span data-stu-id="cf683-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf683-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf683-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="cf683-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf683-108">Parameters</span></span>

<span data-ttu-id="cf683-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cf683-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf683-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf683-110">Return value</span></span>

<span data-ttu-id="cf683-111">Gibt S \_ OK zurück, wenn erfolgreich, oder ein **HRESULT-Wert,** der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="cf683-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf683-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf683-112">Remarks</span></span>

<span data-ttu-id="cf683-113">Diese Methode ruft die [**CBasePin::Active-Methode**](cbasepin-active.md) für jeden verbundenen Pin des Filters auf.</span><span class="sxs-lookup"><span data-stu-id="cf683-113">This method calls the [**CBasePin::Active**](cbasepin-active.md) method on each of the filter's connected pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf683-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf683-114">Requirements</span></span>



| <span data-ttu-id="cf683-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf683-115">Requirement</span></span> | <span data-ttu-id="cf683-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cf683-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf683-117">Header</span><span class="sxs-lookup"><span data-stu-id="cf683-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cf683-118"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="cf683-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cf683-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf683-119">Library</span></span><br/> | <dl> <span data-ttu-id="cf683-120"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="cf683-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf683-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cf683-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf683-122">**CBaseFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cf683-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 





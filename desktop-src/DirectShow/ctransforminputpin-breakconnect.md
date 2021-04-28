---
description: 'CTransformInputPin.BreakConnect-Methode: Die BreakConnect-Methode gibt den Pin von einer Verbindung frei.'
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: CTransformInputPin.BreakConnect-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe425ba617909dcfb1d66dbb4777b579139d436b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085018"
---
# <a name="ctransforminputpinbreakconnect-method"></a><span data-ttu-id="eaaa8-103">CTransformInputPin.BreakConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="eaaa8-103">CTransformInputPin.BreakConnect method</span></span>

<span data-ttu-id="eaaa8-104">Die `BreakConnect` -Methode gibt den Pin von einer Verbindung frei.</span><span class="sxs-lookup"><span data-stu-id="eaaa8-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaaa8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eaaa8-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="eaaa8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eaaa8-106">Parameters</span></span>

<span data-ttu-id="eaaa8-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="eaaa8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eaaa8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eaaa8-108">Return value</span></span>

<span data-ttu-id="eaaa8-109">Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="eaaa8-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaaa8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaaa8-110">Remarks</span></span>

<span data-ttu-id="eaaa8-111">Diese Methode überschreibt die [**CBaseInputPin::BreakConnect-Methode.**](cbaseinputpin-breakconnect.md)</span><span class="sxs-lookup"><span data-stu-id="eaaa8-111">This method overrides the [**CBaseInputPin::BreakConnect**](cbaseinputpin-breakconnect.md) method.</span></span> <span data-ttu-id="eaaa8-112">Sie ruft die [**CTransformFilter::BreakConnect-Methode**](ctransformfilter-breakconnect.md) des Filters auf, die S \_ OK in der Basisklasse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="eaaa8-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="eaaa8-113">Die abgeleitete Klasse kann die **CTransformFilter::BreakConnect-Methode** überschreiben.</span><span class="sxs-lookup"><span data-stu-id="eaaa8-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaaa8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eaaa8-114">Requirements</span></span>



| <span data-ttu-id="eaaa8-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eaaa8-115">Requirement</span></span> | <span data-ttu-id="eaaa8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="eaaa8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaaa8-117">Header</span><span class="sxs-lookup"><span data-stu-id="eaaa8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="eaaa8-118"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="eaaa8-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eaaa8-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eaaa8-119">Library</span></span><br/> | <dl> <span data-ttu-id="eaaa8-120"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="eaaa8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





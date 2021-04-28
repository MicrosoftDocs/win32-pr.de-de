---
description: 'CTransformOutputPin.BreakConnect-Methode: Die BreakConnect-Methode gibt den Pin von einer Verbindung frei.'
ms.assetid: bf68aca3-93e5-4f9d-9980-1a5eed1513f5
title: CTransformOutputPin.BreakConnect-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92854041e1d553945d0a1ab1755ef3557bd4a8b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084958"
---
# <a name="ctransformoutputpinbreakconnect-method"></a><span data-ttu-id="6e829-103">CTransformOutputPin.BreakConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="6e829-103">CTransformOutputPin.BreakConnect method</span></span>

<span data-ttu-id="6e829-104">Die `BreakConnect` -Methode gibt den Pin von einer Verbindung frei.</span><span class="sxs-lookup"><span data-stu-id="6e829-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e829-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e829-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="6e829-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e829-106">Parameters</span></span>

<span data-ttu-id="6e829-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6e829-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e829-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e829-108">Return value</span></span>

<span data-ttu-id="6e829-109">Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="6e829-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e829-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e829-110">Remarks</span></span>

<span data-ttu-id="6e829-111">Diese Methode überschreibt die [**CBaseOutputPin::BreakConnect-Methode.**](cbaseoutputpin-breakconnect.md)</span><span class="sxs-lookup"><span data-stu-id="6e829-111">This method overrides the [**CBaseOutputPin::BreakConnect**](cbaseoutputpin-breakconnect.md) method.</span></span> <span data-ttu-id="6e829-112">Sie ruft die [**CTransformFilter::BreakConnect-Methode**](ctransformfilter-breakconnect.md) des Filters auf, die \_ S OK in der Basisklasse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6e829-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="6e829-113">Die abgeleitete Klasse kann die **CTransformFilter::BreakConnect-Methode** überschreiben.</span><span class="sxs-lookup"><span data-stu-id="6e829-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e829-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e829-114">Requirements</span></span>



| <span data-ttu-id="6e829-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e829-115">Requirement</span></span> | <span data-ttu-id="6e829-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6e829-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e829-117">Header</span><span class="sxs-lookup"><span data-stu-id="6e829-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6e829-118"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e829-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6e829-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6e829-119">Library</span></span><br/> | <dl> <span data-ttu-id="6e829-120"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6e829-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





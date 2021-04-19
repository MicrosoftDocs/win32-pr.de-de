---
description: Die breakconnect-Methode gibt die PIN von einer Verbindung frei.
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: Ctransforminputpin. breakconnect-Methode (Transfrm. h)
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
ms.openlocfilehash: 2274b71b67a54ecacb291d77d2eef4ad8a110fa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359793"
---
# <a name="ctransforminputpinbreakconnect-method"></a><span data-ttu-id="0829c-103">Ctransforminputpin. breakconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="0829c-103">CTransformInputPin.BreakConnect method</span></span>

<span data-ttu-id="0829c-104">Die- `BreakConnect` Methode gibt die PIN von einer Verbindung frei.</span><span class="sxs-lookup"><span data-stu-id="0829c-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0829c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0829c-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="0829c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0829c-106">Parameters</span></span>

<span data-ttu-id="0829c-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0829c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0829c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0829c-108">Return value</span></span>

<span data-ttu-id="0829c-109">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0829c-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0829c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0829c-110">Remarks</span></span>

<span data-ttu-id="0829c-111">Diese Methode überschreibt die [**cbasinput PIN:: breakconnect**](cbaseinputpin-breakconnect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0829c-111">This method overrides the [**CBaseInputPin::BreakConnect**](cbaseinputpin-breakconnect.md) method.</span></span> <span data-ttu-id="0829c-112">Er ruft die [**ctransformfilter:: breakconnect**](ctransformfilter-breakconnect.md) -Methode des Filters auf, die \_ in der Basisklasse den Wert s OK zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0829c-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="0829c-113">Die abgeleitete Klasse kann die **ctransformfilter:: breakconnect** -Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="0829c-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0829c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0829c-114">Requirements</span></span>



| <span data-ttu-id="0829c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0829c-115">Requirement</span></span> | <span data-ttu-id="0829c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0829c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0829c-117">Header</span><span class="sxs-lookup"><span data-stu-id="0829c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0829c-118"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0829c-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0829c-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0829c-119">Library</span></span><br/> | <dl> <span data-ttu-id="0829c-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0829c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





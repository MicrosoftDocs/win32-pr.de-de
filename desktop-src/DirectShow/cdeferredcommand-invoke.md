---
description: Die Aufruf Methode ermöglicht den Zugriff auf Methoden und Eigenschaften, die von einem-Objekt verfügbar gemacht werden.
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: Cdeferredcommand. aufrufen-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 268cfc3d4665eeacafbd695b974f55445747e151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371180"
---
# <a name="cdeferredcommandinvoke-method"></a><span data-ttu-id="d32c1-103">Cdeferredcommand. aufrufen-Methode</span><span class="sxs-lookup"><span data-stu-id="d32c1-103">CDeferredCommand.Invoke method</span></span>

<span data-ttu-id="d32c1-104">Die- `Invoke` Methode bietet Zugriff auf Methoden und Eigenschaften, die von einem-Objekt verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="d32c1-104">The `Invoke` method provides access to methods and properties exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d32c1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d32c1-105">Syntax</span></span>


```C++
HRESULT Invoke();
```



## <a name="parameters"></a><span data-ttu-id="d32c1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d32c1-106">Parameters</span></span>

<span data-ttu-id="d32c1-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d32c1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d32c1-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d32c1-108">Return value</span></span>

<span data-ttu-id="d32c1-109">Gibt VFW E zurück, die \_ \_ bereits \_ abgebrochen wurde, wenn **m \_ pqueue** **null** ist.</span><span class="sxs-lookup"><span data-stu-id="d32c1-109">Returns VFW\_E\_ALREADY\_CANCELLED if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="d32c1-110">Andernfalls wird das **HRESULT** zurückgegeben, das sich aus einem **IDispatch:: GetTypeInfo** -oder **IUnknown:: QueryInterface**-Ausdruck ergibt.</span><span class="sxs-lookup"><span data-stu-id="d32c1-110">Otherwise, returns the **HRESULT** resulting from a call to **IDispatch::GetTypeInfo** or **IUnknown::QueryInterface**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d32c1-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d32c1-111">Requirements</span></span>



| <span data-ttu-id="d32c1-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d32c1-112">Requirement</span></span> | <span data-ttu-id="d32c1-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d32c1-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d32c1-114">Header</span><span class="sxs-lookup"><span data-stu-id="d32c1-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d32c1-115"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d32c1-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d32c1-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d32c1-116">Library</span></span><br/> | <dl> <span data-ttu-id="d32c1-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d32c1-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d32c1-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d32c1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d32c1-119">**Cdeferredcommand-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d32c1-119">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 





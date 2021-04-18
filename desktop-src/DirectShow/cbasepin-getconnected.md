---
description: Die getconnected-Methode ruft die mit dieser Pin verbundene Pin ab.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: Cbasepin. getconnected-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c583b06a9c25126a611736002c455a2c93ed90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351350"
---
# <a name="cbasepingetconnected-method"></a><span data-ttu-id="ab0be-103">Cbasepin. getconnected-Methode</span><span class="sxs-lookup"><span data-stu-id="ab0be-103">CBasePin.GetConnected method</span></span>

<span data-ttu-id="ab0be-104">Die- `GetConnected` Methode ruft die mit dieser Pin verbundene Pin ab.</span><span class="sxs-lookup"><span data-stu-id="ab0be-104">The `GetConnected` method retrieves the pin connected to this pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab0be-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab0be-105">Syntax</span></span>


```C++
IPin* GetConnected();
```



## <a name="parameters"></a><span data-ttu-id="ab0be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab0be-106">Parameters</span></span>

<span data-ttu-id="ab0be-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ab0be-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab0be-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab0be-108">Return value</span></span>

<span data-ttu-id="ab0be-109">Gibt einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen Pin zurück.</span><span class="sxs-lookup"><span data-stu-id="ab0be-109">Returns a pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab0be-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab0be-110">Remarks</span></span>

<span data-ttu-id="ab0be-111">Wenn die PIN nicht verbunden ist, gibt diese Methode **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="ab0be-111">If the pin is not connected, this method returns **NULL**.</span></span> <span data-ttu-id="ab0be-112">Wenden Sie die [**cbasepin:: IsConnected**](cbasepin-isconnected.md) -Methode an, um zu bestimmen, ob die PIN verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ab0be-112">Call the [**CBasePin::IsConnected**](cbasepin-isconnected.md) method to determine whether the pin is connected.</span></span>

<span data-ttu-id="ab0be-113">Die-Methode ruft keine **adressf** für die **IPin** -Schnittstelle auf, sodass der Aufrufer die-Schnittstelle nicht freigeben darf.</span><span class="sxs-lookup"><span data-stu-id="ab0be-113">The method does not call **AddRef** on the **IPin** interface, so the caller should not release the interface.</span></span>

## <a name="examples"></a><span data-ttu-id="ab0be-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab0be-114">Examples</span></span>

<span data-ttu-id="ab0be-115">Da der Verweis Zähler auf dem zurückgegebenen Zeiger nicht inkrementiert wird, können Sie Methodenaufrufe verketten:</span><span class="sxs-lookup"><span data-stu-id="ab0be-115">Because the reference count is not incremented on the returned pointer, you can chain method calls together:</span></span>


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



<span data-ttu-id="ab0be-116">Dieses Codierungs Muster ist sehr praktisch. wie im Beispiel gezeigt, müssen Sie jedoch darauf achten, einen **null** -Zeiger nicht zu dereferenzieren, wenn die PIN nicht verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ab0be-116">This coding pattern is very convenient; but as the example shows, you must be careful not to dereference a **NULL** pointer when the pin is unconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab0be-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab0be-117">Requirements</span></span>



| <span data-ttu-id="ab0be-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab0be-118">Requirement</span></span> | <span data-ttu-id="ab0be-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ab0be-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab0be-120">Header</span><span class="sxs-lookup"><span data-stu-id="ab0be-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ab0be-121"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab0be-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ab0be-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ab0be-122">Library</span></span><br/> | <dl> <span data-ttu-id="ab0be-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ab0be-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab0be-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab0be-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab0be-125">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ab0be-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





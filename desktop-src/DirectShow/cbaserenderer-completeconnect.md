---
description: Die completeconnect-Methode schließt die Verbindung der Eingabe-PIN mit einer anderen Pin ab.
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: Cbaserderderer. completeconnect-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9d2d35f99a3b3b8dc5b668b8ee9a9f94f0a53dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367658"
---
# <a name="cbaserenderercompleteconnect-method"></a><span data-ttu-id="7b39c-103">Cbaserderderer. completeconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="7b39c-103">CBaseRenderer.CompleteConnect method</span></span>

<span data-ttu-id="7b39c-104">Die `CompleteConnect` -Methode schließt die Verbindung der Eingabe-PIN mit einer anderen Pin ab.</span><span class="sxs-lookup"><span data-stu-id="7b39c-104">The `CompleteConnect` method completes the input pin's connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b39c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b39c-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="7b39c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b39c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b39c-107">*preceivepin*</span><span class="sxs-lookup"><span data-stu-id="7b39c-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="7b39c-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="7b39c-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b39c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b39c-109">Return value</span></span>

<span data-ttu-id="7b39c-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="7b39c-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b39c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b39c-111">Remarks</span></span>

<span data-ttu-id="7b39c-112">Die Eingabe-PIN des Filters ruft diese Methode in der eigenen `CompleteConnect` Methode auf, die aufgerufen wird, um eine PIN-Verbindung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7b39c-112">The filter's input pin calls this method from inside its own `CompleteConnect` method, which is called in order to complete a pin connection.</span></span> <span data-ttu-id="7b39c-113">(Weitere Informationen finden Sie unter [**cbasepin:: completeconnect**](cbasepin-completeconnect.md).) Der Filter Ruft die [**cbaserdenderer:: settrepaintstatus**](cbaserenderer-setrepaintstatus.md) -Methode auf, um [**EC- \_ Repaint**](ec-repaint.md) -Ereignisse zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7b39c-113">(For more information, see [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md).) The filter calls the [**CBaseRenderer::SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) method to enable [**EC\_REPAINT**](ec-repaint.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b39c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b39c-114">Requirements</span></span>



| <span data-ttu-id="7b39c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b39c-115">Requirement</span></span> | <span data-ttu-id="7b39c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7b39c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b39c-117">Header</span><span class="sxs-lookup"><span data-stu-id="7b39c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7b39c-118"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b39c-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7b39c-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7b39c-119">Library</span></span><br/> | <dl> <span data-ttu-id="7b39c-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7b39c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b39c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b39c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b39c-122">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7b39c-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





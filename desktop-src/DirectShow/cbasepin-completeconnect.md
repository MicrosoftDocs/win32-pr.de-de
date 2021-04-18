---
description: Die completeconnect-Methode schließt eine Verbindung mit einer anderen Pin ab.
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Cbasepin. completeconnect-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9068bf63d3168a8c6d9e1bca2ef709f63e80a3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354784"
---
# <a name="cbasepincompleteconnect-method"></a><span data-ttu-id="468ed-103">Cbasepin. completeconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="468ed-103">CBasePin.CompleteConnect method</span></span>

<span data-ttu-id="468ed-104">Die- `CompleteConnect` Methode schließt eine Verbindung mit einer anderen Pin ab.</span><span class="sxs-lookup"><span data-stu-id="468ed-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="468ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="468ed-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="468ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="468ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="468ed-107">*preceivepin*</span><span class="sxs-lookup"><span data-stu-id="468ed-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="468ed-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen Pin.</span><span class="sxs-lookup"><span data-stu-id="468ed-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="468ed-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="468ed-109">Return value</span></span>

<span data-ttu-id="468ed-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="468ed-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="468ed-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="468ed-111">Remarks</span></span>

<span data-ttu-id="468ed-112">Diese Methode wird auf beiden Pins am Ende des Verbindungsprozesses aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="468ed-112">This method is called on both pins at the end of the connection process.</span></span> <span data-ttu-id="468ed-113">Die Verbindungs-Pin ruft Sie aus der [**cbasepin:: Connect**](cbasepin-connect.md) -Methode ab, und die empfangende Pin ruft Sie innerhalb der [**cbasepin:: receiveconnection**](cbasepin-receiveconnection.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="468ed-113">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="468ed-114">In der Basisklasse gibt diese Methode einfach S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="468ed-114">In the base class, this method simply returns S\_OK.</span></span> <span data-ttu-id="468ed-115">Wenn eine abgeleitete Klasse über Anforderungen zum Abschließen einer Verbindung verfügt, sollte diese Methode überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="468ed-115">If a derived class has any requirements for completing a connection, it should override this method.</span></span> <span data-ttu-id="468ed-116">Beispielsweise verwendet die [**cbaseoutputpin**](cbaseoutputpin.md) -Klasse diese Methode, um die Speicherzuweisung zu entscheiden.</span><span class="sxs-lookup"><span data-stu-id="468ed-116">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class uses this method to decide the memory allocator.</span></span>

<span data-ttu-id="468ed-117">Wenn diese Methode fehlschlägt, schlägt der allgemeine Verbindungsversuch ebenfalls fehl, und die PIN trennt die Verbindung mit der empfangenden PIN.</span><span class="sxs-lookup"><span data-stu-id="468ed-117">If this method fails, the overall connection attempt also fails, and the pin disconnects from the receiving pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="468ed-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="468ed-118">Requirements</span></span>



| <span data-ttu-id="468ed-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="468ed-119">Requirement</span></span> | <span data-ttu-id="468ed-120">Wert</span><span class="sxs-lookup"><span data-stu-id="468ed-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="468ed-121">Header</span><span class="sxs-lookup"><span data-stu-id="468ed-121">Header</span></span><br/>  | <dl> <span data-ttu-id="468ed-122"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="468ed-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="468ed-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="468ed-123">Library</span></span><br/> | <dl> <span data-ttu-id="468ed-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="468ed-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="468ed-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="468ed-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="468ed-126">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="468ed-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





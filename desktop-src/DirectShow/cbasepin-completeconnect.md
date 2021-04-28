---
description: 'CBasePin.CompleteConnect-Methode: Die CompleteConnect-Methode schließt eine Verbindung mit einem anderen Pin ab.'
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: CBasePin.CompleteConnect-Methode (Amfilter.h)
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
ms.openlocfilehash: fee207d7a17f12cc81036fbd4f82ec49a99f4a31
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096038"
---
# <a name="cbasepincompleteconnect-method"></a><span data-ttu-id="3f6db-103">CBasePin.CompleteConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="3f6db-103">CBasePin.CompleteConnect method</span></span>

<span data-ttu-id="3f6db-104">Die `CompleteConnect` -Methode schließt eine Verbindung mit einem anderen Pin ab.</span><span class="sxs-lookup"><span data-stu-id="3f6db-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f6db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f6db-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="3f6db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f6db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f6db-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="3f6db-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="3f6db-108">Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des anderen Pins.</span><span class="sxs-lookup"><span data-stu-id="3f6db-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f6db-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f6db-109">Return value</span></span>

<span data-ttu-id="3f6db-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="3f6db-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f6db-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f6db-111">Remarks</span></span>

<span data-ttu-id="3f6db-112">Diese Methode wird an beiden Pins am Ende des Verbindungsprozesses aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3f6db-112">This method is called on both pins at the end of the connection process.</span></span> <span data-ttu-id="3f6db-113">Der Verbindungspin ruft ihn innerhalb der [**CBasePin::Connect-Methode**](cbasepin-connect.md) auf, und der empfangende Pin ruft ihn innerhalb der [**CBasePin::ReceiveConnection-Methode**](cbasepin-receiveconnection.md) auf.</span><span class="sxs-lookup"><span data-stu-id="3f6db-113">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="3f6db-114">In der Basisklasse gibt diese Methode einfach S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="3f6db-114">In the base class, this method simply returns S\_OK.</span></span> <span data-ttu-id="3f6db-115">Wenn eine abgeleitete Klasse Anforderungen zum Abschließen einer Verbindung hat, sollte sie diese Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="3f6db-115">If a derived class has any requirements for completing a connection, it should override this method.</span></span> <span data-ttu-id="3f6db-116">Beispielsweise verwendet die [**CBaseOutputPin-Klasse**](cbaseoutputpin.md) diese Methode, um die Speicherzuweisung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3f6db-116">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class uses this method to decide the memory allocator.</span></span>

<span data-ttu-id="3f6db-117">Wenn bei dieser Methode ein Fehler auftritt, schlägt auch der gesamte Verbindungsversuch fehl, und der Pin wird vom empfangenden Pin getrennt.</span><span class="sxs-lookup"><span data-stu-id="3f6db-117">If this method fails, the overall connection attempt also fails, and the pin disconnects from the receiving pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f6db-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f6db-118">Requirements</span></span>



| <span data-ttu-id="3f6db-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f6db-119">Requirement</span></span> | <span data-ttu-id="3f6db-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3f6db-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f6db-121">Header</span><span class="sxs-lookup"><span data-stu-id="3f6db-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3f6db-122"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="3f6db-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3f6db-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3f6db-123">Library</span></span><br/> | <dl> <span data-ttu-id="3f6db-124"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3f6db-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f6db-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3f6db-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f6db-126">**CBasePin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3f6db-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





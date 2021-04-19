---
description: Die checkConnect-Methode bestimmt, ob eine PIN-Verbindung geeignet ist.
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Cbasepin. checkConnect-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24d5c221da417fd1fc2b3f9f140536f825b2f9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373985"
---
# <a name="cbasepincheckconnect-method"></a><span data-ttu-id="339cc-103">Cbasepin. checkConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="339cc-103">CBasePin.CheckConnect method</span></span>

<span data-ttu-id="339cc-104">Die- `CheckConnect` Methode bestimmt, ob eine PIN-Verbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="339cc-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="339cc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="339cc-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="339cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="339cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="339cc-107">*ppin*</span><span class="sxs-lookup"><span data-stu-id="339cc-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="339cc-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen Pin.</span><span class="sxs-lookup"><span data-stu-id="339cc-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="339cc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="339cc-109">Return value</span></span>

<span data-ttu-id="339cc-110">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="339cc-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="339cc-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="339cc-111">Return code</span></span>                                                                                               | <span data-ttu-id="339cc-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="339cc-112">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="339cc-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="339cc-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="339cc-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="339cc-114">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="339cc-115"><dt>**VFW \_ E \_ ungültige \_ Richtung**</dt></span><span class="sxs-lookup"><span data-stu-id="339cc-115"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="339cc-116">PIN-Anweisungen sind nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="339cc-116">Pin directions are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="339cc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="339cc-117">Remarks</span></span>

<span data-ttu-id="339cc-118">Diese Methode wird am Anfang des Verbindungsprozesses für beide Pins aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="339cc-118">This method is called on both pins at the start of the connection process.</span></span> <span data-ttu-id="339cc-119">Die Verbindungs-Pin ruft Sie aus der [**cbasepin:: Connect**](cbasepin-connect.md) -Methode ab, und die empfangende Pin ruft Sie innerhalb der [**cbasepin:: receiveconnection**](cbasepin-receiveconnection.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="339cc-119">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="339cc-120">Verwenden Sie diese Methode, um zu bestimmen, ob die vom *ppin* -Parameter angegebene PIN für eine Verbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="339cc-120">Use this method to determine whether the pin specified by the *pPin* parameter is suitable for a connection.</span></span> <span data-ttu-id="339cc-121">Die-Basisklasse gibt einen Fehler zurück, wenn beide Pins die gleiche Richtung (sowohl Eingabe als auch beide Ausgaben) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="339cc-121">The base class returns an error if both pins have the same direction (both input, or both output).</span></span> <span data-ttu-id="339cc-122">Abgeleitete Klassen können diese Methode überschreiben, um andere Funktionen in der PIN zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="339cc-122">Derived classes can override this method to verify other features in the pin.</span></span> <span data-ttu-id="339cc-123">Beispielsweise fragt die [**cbaseoutputpin**](cbaseoutputpin.md) -Klasse die Eingabe-PIN für Ihre [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="339cc-123">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

<span data-ttu-id="339cc-124">Wenn diese Methode fehlschlägt, schlägt die Verbindung fehl, und die PIN Ruft die [**cbasepin:: breakconnect**](cbasepin-breakconnect.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="339cc-124">If this method fails, the connection fails and the pin calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="339cc-125">Verwenden Sie **breakconnect** , um Ressourcen freizugeben, die in abgerufen wurden `CheckConnect` .</span><span class="sxs-lookup"><span data-stu-id="339cc-125">Use **BreakConnect** to free any resources obtained in `CheckConnect`.</span></span> <span data-ttu-id="339cc-126">Wenn z. b. `CheckConnect` die **QueryInterface** -Methode aufruft, muss **breakconnect** die-Schnittstelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="339cc-126">For example, if `CheckConnect` calls the **QueryInterface** method, **BreakConnect** must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="339cc-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="339cc-127">Requirements</span></span>



| <span data-ttu-id="339cc-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="339cc-128">Requirement</span></span> | <span data-ttu-id="339cc-129">Wert</span><span class="sxs-lookup"><span data-stu-id="339cc-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="339cc-130">Header</span><span class="sxs-lookup"><span data-stu-id="339cc-130">Header</span></span><br/>  | <dl> <span data-ttu-id="339cc-131"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="339cc-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="339cc-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="339cc-132">Library</span></span><br/> | <dl> <span data-ttu-id="339cc-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="339cc-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="339cc-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="339cc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="339cc-135">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="339cc-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





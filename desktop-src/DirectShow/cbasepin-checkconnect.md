---
description: 'CBasePin.CheckConnect-Methode: Die CheckConnect-Methode bestimmt, ob eine Pinverbindung geeignet ist.'
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: CBasePin.CheckConnect-Methode (Amfilter.h)
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
ms.openlocfilehash: 314d3e1ce0e73e60ea07bb4f7270fa04f69750c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096048"
---
# <a name="cbasepincheckconnect-method"></a><span data-ttu-id="f4c6b-103">CBasePin.CheckConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="f4c6b-103">CBasePin.CheckConnect method</span></span>

<span data-ttu-id="f4c6b-104">Die `CheckConnect` -Methode bestimmt, ob eine Stecknadelverbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="f4c6b-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c6b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4c6b-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="f4c6b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4c6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4c6b-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="f4c6b-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="f4c6b-108">Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des anderen Pins.</span><span class="sxs-lookup"><span data-stu-id="f4c6b-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4c6b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4c6b-109">Return value</span></span>

<span data-ttu-id="f4c6b-110">Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.</span><span class="sxs-lookup"><span data-stu-id="f4c6b-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="f4c6b-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f4c6b-111">Return code</span></span>                                                                                               | <span data-ttu-id="f4c6b-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4c6b-112">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="f4c6b-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f4c6b-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="f4c6b-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="f4c6b-114">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="f4c6b-115"><dt>**VFW \_ E \_ INVALID \_ DIRECTION**</dt></span><span class="sxs-lookup"><span data-stu-id="f4c6b-115"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="f4c6b-116">Stecknadelrichtungen sind nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f4c6b-116">Pin directions are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f4c6b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4c6b-117">Remarks</span></span>

<span data-ttu-id="f4c6b-118">Diese Methode wird zu Beginn des Verbindungsprozesses für beide Pins aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f4c6b-118">This method is called on both pins at the start of the connection process.</span></span> <span data-ttu-id="f4c6b-119">Der Verbindende Pin ruft ihn aus der [**CBasePin::Connect-Methode**](cbasepin-connect.md) auf, und der empfangende Pin ruft ihn aus der [**CBasePin::ReceiveConnection-Methode**](cbasepin-receiveconnection.md) auf.</span><span class="sxs-lookup"><span data-stu-id="f4c6b-119">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="f4c6b-120">Verwenden Sie diese Methode, um zu bestimmen, ob der durch den *pPin-Parameter* angegebene Pin für eine Verbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="f4c6b-120">Use this method to determine whether the pin specified by the *pPin* parameter is suitable for a connection.</span></span> <span data-ttu-id="f4c6b-121">Die Basisklasse gibt einen Fehler zurück, wenn beide Pins die gleiche Richtung aufweisen (eingabe oder beide Ausgabe).</span><span class="sxs-lookup"><span data-stu-id="f4c6b-121">The base class returns an error if both pins have the same direction (both input, or both output).</span></span> <span data-ttu-id="f4c6b-122">Abgeleitete Klassen können diese Methode überschreiben, um andere Features im Pin zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f4c6b-122">Derived classes can override this method to verify other features in the pin.</span></span> <span data-ttu-id="f4c6b-123">Beispielsweise fragt die [**CBaseOutputPin-Klasse**](cbaseoutputpin.md) den Eingabepin für die [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ab.</span><span class="sxs-lookup"><span data-stu-id="f4c6b-123">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

<span data-ttu-id="f4c6b-124">Wenn bei dieser Methode ein Fehler auftritt, schlägt die Verbindung fehl, und der Pin ruft die [**CBasePin::BreakConnect-Methode**](cbasepin-breakconnect.md) auf.</span><span class="sxs-lookup"><span data-stu-id="f4c6b-124">If this method fails, the connection fails and the pin calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="f4c6b-125">Verwenden Sie **BreakConnect,** um alle in abgerufenen Ressourcen frei zu `CheckConnect` machen.</span><span class="sxs-lookup"><span data-stu-id="f4c6b-125">Use **BreakConnect** to free any resources obtained in `CheckConnect`.</span></span> <span data-ttu-id="f4c6b-126">Wenn beispielsweise `CheckConnect` die **QueryInterface-Methode** aufruft, muss **BreakConnect** die -Schnittstelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="f4c6b-126">For example, if `CheckConnect` calls the **QueryInterface** method, **BreakConnect** must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4c6b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4c6b-127">Requirements</span></span>



| <span data-ttu-id="f4c6b-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4c6b-128">Requirement</span></span> | <span data-ttu-id="f4c6b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f4c6b-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c6b-130">Header</span><span class="sxs-lookup"><span data-stu-id="f4c6b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f4c6b-131"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f4c6b-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f4c6b-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f4c6b-132">Library</span></span><br/> | <dl> <span data-ttu-id="f4c6b-133"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f4c6b-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4c6b-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f4c6b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4c6b-135">**CBasePin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f4c6b-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





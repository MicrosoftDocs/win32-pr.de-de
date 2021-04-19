---
description: 'Die receiveconnection-Methode akzeptiert eine Verbindung von einer anderen Pin. Diese Methode implementiert die IPin:: receiveconnection-Methode.'
ms.assetid: f17e7d93-ac45-4b8a-98c6-0c76ec7117c9
title: Cbasepin. receiveconnection-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ReceiveConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d0a8134201af1d3c931121f59a20360020a53a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355973"
---
# <a name="cbasepinreceiveconnection-method"></a><span data-ttu-id="96add-104">Cbasepin. receiveconnection-Methode</span><span class="sxs-lookup"><span data-stu-id="96add-104">CBasePin.ReceiveConnection method</span></span>

<span data-ttu-id="96add-105">Die- `ReceiveConnection` Methode akzeptiert eine Verbindung von einer anderen Pin.</span><span class="sxs-lookup"><span data-stu-id="96add-105">The `ReceiveConnection` method accepts a connection from another pin.</span></span> <span data-ttu-id="96add-106">Diese Methode implementiert die [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) -Methode.</span><span class="sxs-lookup"><span data-stu-id="96add-106">This method implements the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="96add-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="96add-107">Syntax</span></span>


```C++
HRESULT ReceiveConnection(
   IPin          *pConnector,
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="96add-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="96add-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96add-109">*pconnector*</span><span class="sxs-lookup"><span data-stu-id="96add-109">*pConnector*</span></span> 
</dt> <dd>

<span data-ttu-id="96add-110">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Verbindungs-PIN.</span><span class="sxs-lookup"><span data-stu-id="96add-110">Pointer to the connecting pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="96add-111">*PMT*</span><span class="sxs-lookup"><span data-stu-id="96add-111">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="96add-112">Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="96add-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96add-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96add-113">Return value</span></span>

<span data-ttu-id="96add-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="96add-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="96add-115">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="96add-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="96add-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="96add-116">Return code</span></span>                                                                                                | <span data-ttu-id="96add-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96add-117">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96add-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="96add-118"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="96add-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="96add-119">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="96add-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="96add-120"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="96add-121">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="96add-121">**NULL** pointer argument.</span></span><br/>                                              |
| <dl> <span data-ttu-id="96add-122"><dt>**VFW \_ E \_ bereits \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="96add-122"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="96add-123">Die PIN ist bereits verbunden.</span><span class="sxs-lookup"><span data-stu-id="96add-123">The pin is already connected.</span></span><br/>                                           |
| <dl> <span data-ttu-id="96add-124"><dt>**VFW \_ E \_ nicht \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="96add-124"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl>        | <span data-ttu-id="96add-125">Der Filter ist aktiv, und die PIN unterstützt keine dynamische erneute Verbindung.</span><span class="sxs-lookup"><span data-stu-id="96add-125">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |
| <dl> <span data-ttu-id="96add-126"><dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt></span><span class="sxs-lookup"><span data-stu-id="96add-126"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="96add-127">Der angegebene Medientyp ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="96add-127">The specified media type is not acceptable.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="96add-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96add-128">Remarks</span></span>

<span data-ttu-id="96add-129">Die Ausgabe-PIN ruft diese Methode für die Eingabe-PIN auf.</span><span class="sxs-lookup"><span data-stu-id="96add-129">The output pin calls this method on the input pin.</span></span> <span data-ttu-id="96add-130">Wenn die Eingabe-PIN einen Fehlercode zurückgibt, schlägt die Verbindung fehl.</span><span class="sxs-lookup"><span data-stu-id="96add-130">If the input pin returns an error code, the connection fails.</span></span>

<span data-ttu-id="96add-131">In der-Basisklasse führt diese Methode die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="96add-131">In the base class, this method performs the following steps:</span></span>

-   <span data-ttu-id="96add-132">Überprüft, ob die PIN bereits verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="96add-132">Checks whether the pin is already connected.</span></span>
-   <span data-ttu-id="96add-133">Überprüft, ob der Filter beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="96add-133">Checks whether the filter is stopped.</span></span>
-   <span data-ttu-id="96add-134">Ruft die [**cbasepin:: checkConnect**](cbasepin-checkconnect.md) -Methode auf, um zu überprüfen, ob die Verbindungs-Pin geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="96add-134">Calls the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method to test whether the connecting pin is suitable.</span></span>
-   <span data-ttu-id="96add-135">Ruft die [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode auf, um zu testen, ob der Medientyp zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="96add-135">Calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to test whether the media type is acceptable.</span></span>

<span data-ttu-id="96add-136">Wenn alle diese Schritte erfolgreich ausgeführt wurden, ruft die-Methode die [**cbasepin:: completeconnect**](cbasepin-completeconnect.md) -Methode und die [**setmediatype**](cbasepin-setmediatype.md) -Methode auf, um die Verbindung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="96add-136">If all of these steps succeed, the method calls the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) and [**SetMediaType**](cbasepin-setmediatype.md) methods to complete the connection.</span></span> <span data-ttu-id="96add-137">Diese Methoden speichern den Medientyp und einen Zeiger auf die Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="96add-137">These methods store the media type and a pointer to the output pin.</span></span>

<span data-ttu-id="96add-138">Wenn **checkConnect** oder **checkmediatype** fehlschlägt, ruft die Basisklasse die [**cbasepin:: breakconnect**](cbasepin-breakconnect.md) -Methode auf, um die Verbindung zu unterbrechen, und gibt dann einen Fehlercode aus zurück `ReceiveConnection` .</span><span class="sxs-lookup"><span data-stu-id="96add-138">If **CheckConnect** or **CheckMediaType** fail, the base class calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method to break the connection and then returns an error code from `ReceiveConnection`.</span></span>

## <a name="requirements"></a><span data-ttu-id="96add-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96add-139">Requirements</span></span>



| <span data-ttu-id="96add-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96add-140">Requirement</span></span> | <span data-ttu-id="96add-141">Wert</span><span class="sxs-lookup"><span data-stu-id="96add-141">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96add-142">Header</span><span class="sxs-lookup"><span data-stu-id="96add-142">Header</span></span><br/>  | <dl> <span data-ttu-id="96add-143"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96add-143"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="96add-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="96add-144">Library</span></span><br/> | <dl> <span data-ttu-id="96add-145">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="96add-145"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96add-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96add-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96add-147">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="96add-147">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





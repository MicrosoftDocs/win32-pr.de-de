---
description: Die Methode "Methode" stellt mithilfe eines angegebenen Medientyps eine Verbindung mit einer anderen Pin her.
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: Cbasepin. ditconnection-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AttemptConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f80d81b5f105f528292a23f8b58257066b425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367808"
---
# <a name="cbasepinattemptconnection-method"></a><span data-ttu-id="78fac-103">Cbasepin.. der Connection-Methode</span><span class="sxs-lookup"><span data-stu-id="78fac-103">CBasePin.AttemptConnection method</span></span>

<span data-ttu-id="78fac-104">Die- `AttemptConnection` Methode stellt mithilfe eines angegebenen Medientyps eine Verbindung mit einer anderen Pin her.</span><span class="sxs-lookup"><span data-stu-id="78fac-104">The `AttemptConnection` method connects to another pin using a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="78fac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78fac-105">Syntax</span></span>


```C++
virtual HRESULT AttemptConnection(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="78fac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78fac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78fac-107">*preceivepin*</span><span class="sxs-lookup"><span data-stu-id="78fac-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="78fac-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der empfangenden PIN.</span><span class="sxs-lookup"><span data-stu-id="78fac-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="78fac-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="78fac-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="78fac-110">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="78fac-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78fac-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78fac-111">Return value</span></span>

<span data-ttu-id="78fac-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="78fac-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="78fac-113">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="78fac-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="78fac-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="78fac-114">Return code</span></span>                                                                                                | <span data-ttu-id="78fac-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78fac-115">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="78fac-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="78fac-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="78fac-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="78fac-117">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="78fac-118"><dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt></span><span class="sxs-lookup"><span data-stu-id="78fac-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="78fac-119">Der Medientyp ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="78fac-119">The media type is not acceptable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="78fac-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78fac-120">Remarks</span></span>

<span data-ttu-id="78fac-121">Diese Methode versucht, die beiden Pins mit einem bestimmten Medientyp zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="78fac-121">This method attempts to connect the two pins with a specific media type.</span></span> <span data-ttu-id="78fac-122">Wenn der Typ nicht zulässig ist, schlägt die Methode fehl, ohne andere Medientypen auszuprobieren.</span><span class="sxs-lookup"><span data-stu-id="78fac-122">If the type is not acceptable, the method fails without trying other media types.</span></span>

<span data-ttu-id="78fac-123">Wenn der Medientyp zulässig ist, ruft diese Methode die [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) -Methode der empfangenden PIN auf.</span><span class="sxs-lookup"><span data-stu-id="78fac-123">If the media type is acceptable, this method calls the receiving pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="78fac-124">Anschließend wird die [**cbasepin:: completeconnect**](cbasepin-completeconnect.md) -Methode aufgerufen, um die Verbindung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="78fac-124">Then it calls the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method to complete the connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="78fac-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78fac-125">Requirements</span></span>



| <span data-ttu-id="78fac-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78fac-126">Requirement</span></span> | <span data-ttu-id="78fac-127">Wert</span><span class="sxs-lookup"><span data-stu-id="78fac-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78fac-128">Header</span><span class="sxs-lookup"><span data-stu-id="78fac-128">Header</span></span><br/>  | <dl> <span data-ttu-id="78fac-129"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78fac-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="78fac-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78fac-130">Library</span></span><br/> | <dl> <span data-ttu-id="78fac-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="78fac-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78fac-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78fac-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78fac-133">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="78fac-133">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





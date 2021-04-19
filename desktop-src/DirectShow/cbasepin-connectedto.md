---
description: 'Die connectedto-Methode ruft ggf. einen Zeiger auf die verbundene Pin ab. Diese Methode implementiert die IPin:: connectedto-Methode.'
ms.assetid: d8978c9a-e498-4411-a052-f3c2fca570ef
title: Cbasepin. connectedto-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectedTo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5003154011f93b2b70ddd49dab00dcc1659eb2f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354171"
---
# <a name="cbasepinconnectedto-method"></a><span data-ttu-id="64c66-104">Cbasepin. connectedto-Methode</span><span class="sxs-lookup"><span data-stu-id="64c66-104">CBasePin.ConnectedTo method</span></span>

<span data-ttu-id="64c66-105">Die- `ConnectedTo` Methode ruft ggf. einen Zeiger auf die verbundene Pin ab.</span><span class="sxs-lookup"><span data-stu-id="64c66-105">The `ConnectedTo` method retrieves a pointer to the connected pin, if any.</span></span> <span data-ttu-id="64c66-106">Diese Methode implementiert die [**IPin:: connectedto**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) -Methode.</span><span class="sxs-lookup"><span data-stu-id="64c66-106">This method implements the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="64c66-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="64c66-107">Syntax</span></span>


```C++
HRESULT ConnectedTo(
   IPin **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="64c66-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="64c66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64c66-109">*pppin*</span><span class="sxs-lookup"><span data-stu-id="64c66-109">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="64c66-110">Adresse einer Variablen, die einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der anderen Pin empfängt.</span><span class="sxs-lookup"><span data-stu-id="64c66-110">Address of a variable that receives a pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64c66-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64c66-111">Return value</span></span>

<span data-ttu-id="64c66-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="64c66-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="64c66-113">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="64c66-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="64c66-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="64c66-114">Return code</span></span>                                                                                           | <span data-ttu-id="64c66-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64c66-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="64c66-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="64c66-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="64c66-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="64c66-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="64c66-118"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="64c66-118"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="64c66-119">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="64c66-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="64c66-120"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="64c66-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="64c66-121">Die PIN ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="64c66-121">Pin is not connected.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="64c66-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64c66-122">Remarks</span></span>

<span data-ttu-id="64c66-123">Wenn die Methode erfolgreich ausgeführt wird, weist die zurückgegebene **IPin** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="64c66-123">If the method succeeds, the **IPin** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="64c66-124">Stellen Sie sicher, dass Sie Sie freigeben, wenn Sie dies erledigt haben.</span><span class="sxs-lookup"><span data-stu-id="64c66-124">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="64c66-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64c66-125">Requirements</span></span>



| <span data-ttu-id="64c66-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64c66-126">Requirement</span></span> | <span data-ttu-id="64c66-127">Wert</span><span class="sxs-lookup"><span data-stu-id="64c66-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c66-128">Header</span><span class="sxs-lookup"><span data-stu-id="64c66-128">Header</span></span><br/>  | <dl> <span data-ttu-id="64c66-129"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64c66-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="64c66-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="64c66-130">Library</span></span><br/> | <dl> <span data-ttu-id="64c66-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="64c66-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64c66-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64c66-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64c66-133">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="64c66-133">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





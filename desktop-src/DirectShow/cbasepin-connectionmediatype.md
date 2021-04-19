---
description: 'Die connectionmediatype-Methode ruft ggf. den Medientyp für die aktuelle PIN-Verbindung ab. Diese Methode implementiert die IPin:: connectionmediatype-Methode.'
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: Cbasepin. connectionmediatype-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectionMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62bd211b6c93e44c571d822ccc86104a5a6fdcab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367540"
---
# <a name="cbasepinconnectionmediatype-method"></a><span data-ttu-id="7de4a-104">Cbasepin. connectionmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="7de4a-104">CBasePin.ConnectionMediaType method</span></span>

<span data-ttu-id="7de4a-105">Die **connectionmediatype** -Methode ruft ggf. den Medientyp für die aktuelle PIN-Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="7de4a-105">The **ConnectionMediaType** method retrieves the media type for the current pin connection, if any.</span></span> <span data-ttu-id="7de4a-106">Diese Methode implementiert die [**IPin:: connectionmediatype**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7de4a-106">This method implements the [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7de4a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7de4a-107">Syntax</span></span>


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="7de4a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7de4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7de4a-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="7de4a-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="7de4a-110">Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp empfängt.</span><span class="sxs-lookup"><span data-stu-id="7de4a-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7de4a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7de4a-111">Return value</span></span>

<span data-ttu-id="7de4a-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7de4a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7de4a-113">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="7de4a-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="7de4a-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7de4a-114">Return code</span></span>                                                                                           | <span data-ttu-id="7de4a-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7de4a-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="7de4a-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7de4a-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="7de4a-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="7de4a-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="7de4a-118"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="7de4a-118"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="7de4a-119">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="7de4a-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="7de4a-120"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="7de4a-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="7de4a-121">Die PIN ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="7de4a-121">Pin is not connected.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="7de4a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7de4a-122">Remarks</span></span>

<span data-ttu-id="7de4a-123">Wenn die PIN verbunden ist, kopiert diese Methode den Medientyp in die von *PMT* angegebene [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur. Der Aufrufer muss den Format Block des Medientyps freigeben.</span><span class="sxs-lookup"><span data-stu-id="7de4a-123">If the pin is connected, this method copies the media type into the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure specified by *pmt*. The caller must free the media type's format block.</span></span> <span data-ttu-id="7de4a-124">Sie können die [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) -Funktion oder die [**freemediatype**](freemediatype.md) -Hilfsfunktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="7de4a-124">You can use the [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function, or the [**FreeMediaType**](freemediatype.md) helper function.</span></span>

<span data-ttu-id="7de4a-125">Wenn die PIN nicht verbunden ist, wird von dieser Methode der durch *PMT* angegebene Speicherblock Nullen und ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7de4a-125">If the pin is not connected, this method zeroes the memory block specified by *pmt* and returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7de4a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7de4a-126">Requirements</span></span>



| <span data-ttu-id="7de4a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7de4a-127">Requirement</span></span> | <span data-ttu-id="7de4a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7de4a-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7de4a-129">Header</span><span class="sxs-lookup"><span data-stu-id="7de4a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7de4a-130"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7de4a-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7de4a-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7de4a-131">Library</span></span><br/> | <dl> <span data-ttu-id="7de4a-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7de4a-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7de4a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7de4a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7de4a-134">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7de4a-134">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 


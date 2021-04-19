---
description: Die checkmediatype-Methode bestimmt, ob ein vorgeschlagene Medientyp mit dem Anzeige Format kompatibel ist.
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: Cimagedisplay. checkmediatype-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8ebcdbe6bbfe6538a2ea166be0816f31954c7d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366906"
---
# <a name="cimagedisplaycheckmediatype-method"></a><span data-ttu-id="733c7-103">Cimagedisplay. checkmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="733c7-103">CImageDisplay.CheckMediaType method</span></span>

<span data-ttu-id="733c7-104">Die- `CheckMediaType` Methode bestimmt, ob ein vorgeschlagene Medientyp mit dem Anzeige Format kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="733c7-104">The `CheckMediaType` method determines whether a proposed media type is compatible with the display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="733c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="733c7-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmtIn
);
```



## <a name="parameters"></a><span data-ttu-id="733c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="733c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733c7-107">*pmtin*</span><span class="sxs-lookup"><span data-stu-id="733c7-107">*pmtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="733c7-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="733c7-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733c7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="733c7-109">Return value</span></span>

<span data-ttu-id="733c7-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="733c7-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="733c7-111">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="733c7-111">Possible values include the following.</span></span>



| <span data-ttu-id="733c7-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="733c7-112">Return code</span></span>                                                                                  | <span data-ttu-id="733c7-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="733c7-113">Description</span></span>                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="733c7-114"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="733c7-114"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="733c7-115">Ungültiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="733c7-115">Invalid media type.</span></span><br/>           |
| <dl> <span data-ttu-id="733c7-116"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="733c7-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="733c7-117">Ungültiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="733c7-117">Invalid media type.</span></span><br/>           |
| <dl> <span data-ttu-id="733c7-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="733c7-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="733c7-119">Der Medientyp ist kompatibel.</span><span class="sxs-lookup"><span data-stu-id="733c7-119">The media type is compatible.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="733c7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="733c7-120">Requirements</span></span>



| <span data-ttu-id="733c7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="733c7-121">Requirement</span></span> | <span data-ttu-id="733c7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="733c7-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="733c7-123">Header</span><span class="sxs-lookup"><span data-stu-id="733c7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="733c7-124"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="733c7-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="733c7-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="733c7-125">Library</span></span><br/> | <dl> <span data-ttu-id="733c7-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="733c7-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="733c7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="733c7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733c7-128">**Cimagedisplay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="733c7-128">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 





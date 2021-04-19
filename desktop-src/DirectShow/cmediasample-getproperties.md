---
description: 'Die GetProperties-Methode ruft die Eigenschaften des Beispiels ab. Diese Methode implementiert die IMediaSample2:: GetProperties-Methode.'
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: Cmediasample. GetProperties-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06ee1022f298e2f5167d348777b33fc2f1703eef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369395"
---
# <a name="cmediasamplegetproperties-method"></a><span data-ttu-id="7a72f-104">Cmediasample. GetProperties-Methode</span><span class="sxs-lookup"><span data-stu-id="7a72f-104">CMediaSample.GetProperties method</span></span>

<span data-ttu-id="7a72f-105">Die- `GetProperties` Methode ruft die Eigenschaften des Beispiels ab.</span><span class="sxs-lookup"><span data-stu-id="7a72f-105">The `GetProperties` method retrieves the properties of the sample.</span></span> <span data-ttu-id="7a72f-106">Diese Methode implementiert die [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7a72f-106">This method implements the [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a72f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a72f-107">Syntax</span></span>


```C++
HRESULT GetProperties(
   DWORD cbProperties,
   BYTE  *pbProperties
);
```



## <a name="parameters"></a><span data-ttu-id="7a72f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a72f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a72f-109">*cbproperties*</span><span class="sxs-lookup"><span data-stu-id="7a72f-109">*cbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="7a72f-110">Länge der abzurufenden Eigenschaften Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="7a72f-110">Length of property data to retrieve, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7a72f-111">*pbproperties*</span><span class="sxs-lookup"><span data-stu-id="7a72f-111">*pbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="7a72f-112">Zeiger auf einen Puffer der Größe *cbproperties*.</span><span class="sxs-lookup"><span data-stu-id="7a72f-112">Pointer to a buffer of size *cbProperties*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a72f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a72f-113">Return value</span></span>

<span data-ttu-id="7a72f-114">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7a72f-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="7a72f-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7a72f-115">Return code</span></span>                                                                               | <span data-ttu-id="7a72f-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a72f-116">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="7a72f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a72f-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="7a72f-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="7a72f-118">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="7a72f-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="7a72f-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="7a72f-120">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="7a72f-120">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7a72f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a72f-121">Requirements</span></span>



| <span data-ttu-id="7a72f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a72f-122">Requirement</span></span> | <span data-ttu-id="7a72f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7a72f-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a72f-124">Header</span><span class="sxs-lookup"><span data-stu-id="7a72f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7a72f-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a72f-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7a72f-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7a72f-126">Library</span></span><br/> | <dl> <span data-ttu-id="7a72f-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7a72f-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a72f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a72f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a72f-129">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7a72f-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 





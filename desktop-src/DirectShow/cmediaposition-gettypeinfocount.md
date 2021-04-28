---
description: 'CMediaPosition.GetTypeInfoCount-Methode: Die GetTypeInfoCount-Methode ruft die Anzahl der Typinformationsschnittstellen ab, die das Objekt bereitstellt.'
ms.assetid: c98368f2-ae0c-4301-be30-7332b19f53ee
title: CMediaPosition.GetTypeInfoCount-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8cfc54f414a6722f7f69a0330fad2d1a0cfab425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095478"
---
# <a name="cmediapositiongettypeinfocount-method"></a><span data-ttu-id="332f2-103">CMediaPosition.GetTypeInfoCount-Methode</span><span class="sxs-lookup"><span data-stu-id="332f2-103">CMediaPosition.GetTypeInfoCount method</span></span>

<span data-ttu-id="332f2-104">Die `GetTypeInfoCount` -Methode ruft die Anzahl der Typinformationsschnittstellen ab, die das -Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="332f2-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="332f2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="332f2-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="332f2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="332f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="332f2-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="332f2-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="332f2-108">Zeiger auf eine Variable, die die Anzahl der vom -Objekt bereitgestellten Typinformationsschnittstellen empfängt.</span><span class="sxs-lookup"><span data-stu-id="332f2-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="332f2-109">Wenn die Methode zurückgegeben wird, ist der Wert 1.</span><span class="sxs-lookup"><span data-stu-id="332f2-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="332f2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="332f2-110">Return value</span></span>

<span data-ttu-id="332f2-111">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="332f2-111">Returns one of the following values.</span></span>



| <span data-ttu-id="332f2-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="332f2-112">Return code</span></span>                                                                               | <span data-ttu-id="332f2-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="332f2-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="332f2-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="332f2-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="332f2-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="332f2-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="332f2-116"><dt>**E \_ POINTER**</dt></span><span class="sxs-lookup"><span data-stu-id="332f2-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="332f2-117">**NULL-Zeigerargument.**</span><span class="sxs-lookup"><span data-stu-id="332f2-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="332f2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="332f2-118">Requirements</span></span>



| <span data-ttu-id="332f2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="332f2-119">Requirement</span></span> | <span data-ttu-id="332f2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="332f2-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="332f2-121">Header</span><span class="sxs-lookup"><span data-stu-id="332f2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="332f2-122"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="332f2-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="332f2-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="332f2-123">Library</span></span><br/> | <dl> <span data-ttu-id="332f2-124"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="332f2-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="332f2-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="332f2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="332f2-126">**CMediaPosition-Klasse**</span><span class="sxs-lookup"><span data-stu-id="332f2-126">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 





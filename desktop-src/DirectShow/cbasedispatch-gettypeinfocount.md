---
description: Die GetTypeInfoCount-Methode ruft die Anzahl der Schnittstellen für Typinformationen ab, die das Objekt bereitstellt.
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: Cbasedispatch. gettypanfocount-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39c5b78181f5f26fb5f57831345bb6345a26da85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368422"
---
# <a name="cbasedispatchgettypeinfocount-method"></a><span data-ttu-id="c2cb3-103">Cbasedispatch. gettypanfocount-Methode</span><span class="sxs-lookup"><span data-stu-id="c2cb3-103">CBaseDispatch.GetTypeInfoCount method</span></span>

<span data-ttu-id="c2cb3-104">Die- `GetTypeInfoCount` Methode ruft die Anzahl der Schnittstellen für Typinformationen ab, die das Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c2cb3-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2cb3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2cb3-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="c2cb3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2cb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2cb3-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="c2cb3-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c2cb3-108">Ein Zeiger auf eine Variable, die die Anzahl der vom-Objekt bereitgestellten Type-Information-Schnittstellen empfängt.</span><span class="sxs-lookup"><span data-stu-id="c2cb3-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="c2cb3-109">Wenn die Methode zurückgibt, ist der Wert 1.</span><span class="sxs-lookup"><span data-stu-id="c2cb3-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2cb3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2cb3-110">Return value</span></span>

<span data-ttu-id="c2cb3-111">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c2cb3-111">Returns one of the following values.</span></span>



| <span data-ttu-id="c2cb3-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c2cb3-112">Return code</span></span>                                                                               | <span data-ttu-id="c2cb3-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2cb3-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c2cb3-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c2cb3-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="c2cb3-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="c2cb3-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="c2cb3-116"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="c2cb3-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="c2cb3-117">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="c2cb3-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c2cb3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2cb3-118">Requirements</span></span>



| <span data-ttu-id="c2cb3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2cb3-119">Requirement</span></span> | <span data-ttu-id="c2cb3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c2cb3-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2cb3-121">Header</span><span class="sxs-lookup"><span data-stu-id="c2cb3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c2cb3-122"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2cb3-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c2cb3-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c2cb3-123">Library</span></span><br/> | <dl> <span data-ttu-id="c2cb3-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c2cb3-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2cb3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2cb3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2cb3-126">**Cbasedispatch-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c2cb3-126">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 





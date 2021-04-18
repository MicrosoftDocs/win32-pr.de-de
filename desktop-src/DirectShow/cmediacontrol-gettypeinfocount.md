---
description: Ruft die Anzahl der von einem-Objekt bereitgestellten Typ-Informations Schnittstellen ab.
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: Cmediacontrol. gettypanfocount-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2454e503a045a02db20c0dc457b6367f6d3b427
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365629"
---
# <a name="cmediacontrolgettypeinfocount-method"></a><span data-ttu-id="b55df-103">Cmediacontrol. gettypanfocount-Methode</span><span class="sxs-lookup"><span data-stu-id="b55df-103">CMediaControl.GetTypeInfoCount method</span></span>

<span data-ttu-id="b55df-104">Ruft die Anzahl der von einem-Objekt bereitgestellten Typ-Informations Schnittstellen ab.</span><span class="sxs-lookup"><span data-stu-id="b55df-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b55df-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b55df-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="b55df-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b55df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b55df-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="b55df-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="b55df-108">Ein Zeiger auf die Anzahl der vom Objekt bereitgestellten Schnittstellen vom Typ "Information".</span><span class="sxs-lookup"><span data-stu-id="b55df-108">Pointer to the number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="b55df-109">Wenn das Objekt Typinformationen bereitstellt, ist diese Zahl 1. Andernfalls ist die Zahl 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b55df-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b55df-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b55df-110">Return value</span></span>

<span data-ttu-id="b55df-111">Gibt einen E- \_ Zeiger zurück, wenn *pctinfo* ungültig ist; andernfalls gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b55df-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="b55df-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b55df-112">Requirements</span></span>



| <span data-ttu-id="b55df-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b55df-113">Requirement</span></span> | <span data-ttu-id="b55df-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b55df-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b55df-115">Header</span><span class="sxs-lookup"><span data-stu-id="b55df-115">Header</span></span><br/>  | <dl> <span data-ttu-id="b55df-116"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b55df-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b55df-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b55df-117">Library</span></span><br/> | <dl> <span data-ttu-id="b55df-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b55df-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b55df-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b55df-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b55df-120">**Cmediacontrol-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b55df-120">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 





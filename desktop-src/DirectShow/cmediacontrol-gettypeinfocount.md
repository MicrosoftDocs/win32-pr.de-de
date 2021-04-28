---
description: 'CMediaControl.GetTypeInfoCount-Methode: Ruft die Anzahl der Typinformationsschnittstellen ab, die von einem -Objekt bereitgestellt werden.'
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: CMediaControl.GetTypeInfoCount-Methode (Ctlutil.h)
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
ms.openlocfilehash: 7b46838278414442d6c6fc64687fe21e02732e83
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095588"
---
# <a name="cmediacontrolgettypeinfocount-method"></a><span data-ttu-id="c6039-103">CMediaControl.GetTypeInfoCount-Methode</span><span class="sxs-lookup"><span data-stu-id="c6039-103">CMediaControl.GetTypeInfoCount method</span></span>

<span data-ttu-id="c6039-104">Ruft die Anzahl der Typinformationsschnittstellen ab, die von einem -Objekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c6039-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6039-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6039-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="c6039-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6039-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6039-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="c6039-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c6039-108">Zeiger auf die Anzahl der Typinformationsschnittstellen, die das -Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c6039-108">Pointer to the number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="c6039-109">Wenn das Objekt Typinformationen bereitstellt, ist diese Zahl 1. Andernfalls ist die Zahl 0.</span><span class="sxs-lookup"><span data-stu-id="c6039-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6039-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6039-110">Return value</span></span>

<span data-ttu-id="c6039-111">Gibt E \_ POINTER zurück, wenn *pctinfo* ungültig ist, andernfalls S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c6039-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6039-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6039-112">Requirements</span></span>



| <span data-ttu-id="c6039-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6039-113">Requirement</span></span> | <span data-ttu-id="c6039-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c6039-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6039-115">Header</span><span class="sxs-lookup"><span data-stu-id="c6039-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c6039-116"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6039-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c6039-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c6039-117">Library</span></span><br/> | <dl> <span data-ttu-id="c6039-118"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c6039-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6039-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c6039-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6039-120">**CMediaControl-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c6039-120">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 





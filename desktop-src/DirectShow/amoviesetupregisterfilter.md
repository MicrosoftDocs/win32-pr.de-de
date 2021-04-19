---
description: Veraltet. Verwenden Sie stattdessen AMovieSetupRegisterFilter2.
ms.assetid: 42278829-d09e-46c7-8f1a-fa4572f7cc00
title: Amoviesetupregisterfilter-Funktion (dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieSetupRegisterFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 398d2d727e26feaca23d6bddbdcbc8a578d096eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373808"
---
# <a name="amoviesetupregisterfilter-function"></a><span data-ttu-id="11ded-104">Amoviesetupregisterfilter-Funktion</span><span class="sxs-lookup"><span data-stu-id="11ded-104">AMovieSetupRegisterFilter function</span></span>

<span data-ttu-id="11ded-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="11ded-105">Obsolete.</span></span> <span data-ttu-id="11ded-106">Verwenden Sie stattdessen [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) .</span><span class="sxs-lookup"><span data-stu-id="11ded-106">Use [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="11ded-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="11ded-107">Syntax</span></span>


```C++
HRESULT AMovieSetupRegisterFilter(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper              *pIFM,
         BOOL                       bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="11ded-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="11ded-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11ded-109">*psetupdata*</span><span class="sxs-lookup"><span data-stu-id="11ded-109">*psetupdata*</span></span> 
</dt> <dd>

<span data-ttu-id="11ded-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="11ded-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="11ded-111">*pifm*</span><span class="sxs-lookup"><span data-stu-id="11ded-111">*pIFM*</span></span> 
</dt> <dd>

<span data-ttu-id="11ded-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="11ded-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="11ded-113">*bregister*</span><span class="sxs-lookup"><span data-stu-id="11ded-113">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="11ded-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="11ded-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11ded-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11ded-115">Return value</span></span>

<span data-ttu-id="11ded-116">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="11ded-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="11ded-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="11ded-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="11ded-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11ded-118">Requirements</span></span>



| <span data-ttu-id="11ded-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11ded-119">Requirement</span></span> | <span data-ttu-id="11ded-120">Wert</span><span class="sxs-lookup"><span data-stu-id="11ded-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11ded-121">Header</span><span class="sxs-lookup"><span data-stu-id="11ded-121">Header</span></span><br/>  | <dl> <span data-ttu-id="11ded-122"><dt>Dllsetup. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11ded-122"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="11ded-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11ded-123">Library</span></span><br/> | <dl> <span data-ttu-id="11ded-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="11ded-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11ded-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11ded-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11ded-126">**DLL-Setup Funktionen**</span><span class="sxs-lookup"><span data-stu-id="11ded-126">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 





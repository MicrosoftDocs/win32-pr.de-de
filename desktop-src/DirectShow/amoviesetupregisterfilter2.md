---
description: Die AMovieSetupRegisterFilter2-Funktion registriert die Vorzüge, Pins und Medientypen eines Filters mithilfe der IFilterMapper2-Schnittstelle in der Registrierung.
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: AMovieSetupRegisterFilter2-Funktion (dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 272b781cf70f1dede9d4eea64b45d3d9d793a119
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359736"
---
# <a name="amoviesetupregisterfilter2-function"></a><span data-ttu-id="2d593-103">AMovieSetupRegisterFilter2-Funktion</span><span class="sxs-lookup"><span data-stu-id="2d593-103">AMovieSetupRegisterFilter2 function</span></span>

<span data-ttu-id="2d593-104">Die **AMovieSetupRegisterFilter2** -Funktion registriert die Vorzüge, Pins und Medientypen eines Filters mithilfe der [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) -Schnittstelle in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="2d593-104">The **AMovieSetupRegisterFilter2** function registers a filter's merit, pins, and media types in the registry using the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d593-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d593-105">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper2             *pIFM2,
         BOOL                       bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="2d593-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d593-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d593-107">*psetupdata*</span><span class="sxs-lookup"><span data-stu-id="2d593-107">*psetupdata*</span></span> 
</dt> <dd>

<span data-ttu-id="2d593-108">Zeiger auf die [**amoviesetup- \_ Filter**](amoviesetup-filter.md) Daten.</span><span class="sxs-lookup"><span data-stu-id="2d593-108">Pointer to the [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) data.</span></span>

</dd> <dt>

<span data-ttu-id="2d593-109">*pIFM2*</span><span class="sxs-lookup"><span data-stu-id="2d593-109">*pIFM2*</span></span> 
</dt> <dd>

<span data-ttu-id="2d593-110">Zeiger auf die [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2d593-110">Pointer to [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2d593-111">*bregister*</span><span class="sxs-lookup"><span data-stu-id="2d593-111">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="2d593-112">Wert, der angibt, ob der Filter registriert werden soll. **True** gibt den Filter registrieren an, **false** bedeutet, dass die Registrierung aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="2d593-112">Value indicating whether to register the filter; **TRUE** indicates register the filter, **FALSE** indicates unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d593-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d593-113">Return value</span></span>

<span data-ttu-id="2d593-114">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2d593-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2d593-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2d593-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d593-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d593-116">Remarks</span></span>

<span data-ttu-id="2d593-117">Die [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) -Funktion ruft diese Hilfsfunktion auf, um einen Filter zu registrieren, nachdem der com-Server registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="2d593-117">The [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function calls this helper function to register a filter after the COM server has been registered.</span></span>

<span data-ttu-id="2d593-118">In der Regel verwendet ein Filter [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) und ruft diese Funktion nicht direkt auf.</span><span class="sxs-lookup"><span data-stu-id="2d593-118">Typically, a filter will use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) and will not call this function directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d593-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d593-119">Requirements</span></span>



| <span data-ttu-id="2d593-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d593-120">Requirement</span></span> | <span data-ttu-id="2d593-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2d593-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d593-122">Header</span><span class="sxs-lookup"><span data-stu-id="2d593-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2d593-123"><dt>Dllsetup. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d593-123"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2d593-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2d593-124">Library</span></span><br/> | <dl> <span data-ttu-id="2d593-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2d593-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d593-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d593-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d593-127">**DLL-Setup Funktionen**</span><span class="sxs-lookup"><span data-stu-id="2d593-127">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 





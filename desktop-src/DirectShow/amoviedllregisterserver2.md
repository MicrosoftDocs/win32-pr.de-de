---
description: Die AMovieDllRegisterServer2-Funktion registriert Filter und hebt die Registrierung auf.
ms.assetid: 2122949d-0117-4c68-bfcd-c717b14dc970
title: AMovieDllRegisterServer2-Funktion (dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec36290b7cad66b2b5f27633d30ae76c3331eba9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360984"
---
# <a name="amoviedllregisterserver2-function"></a><span data-ttu-id="78d2b-103">AMovieDllRegisterServer2-Funktion</span><span class="sxs-lookup"><span data-stu-id="78d2b-103">AMovieDllRegisterServer2 function</span></span>

<span data-ttu-id="78d2b-104">Die **AMovieDllRegisterServer2** -Funktion registriert Filter und hebt die Registrierung auf.</span><span class="sxs-lookup"><span data-stu-id="78d2b-104">The **AMovieDllRegisterServer2** function registers and unregisters filters.</span></span>

## <a name="syntax"></a><span data-ttu-id="78d2b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78d2b-105">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer2(
   BOOL bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="78d2b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78d2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78d2b-107">*bregister*</span><span class="sxs-lookup"><span data-stu-id="78d2b-107">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="78d2b-108">**True** gibt den Filter registrieren an, **false** bedeutet, dass die Registrierung aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="78d2b-108">**TRUE** indicates register the filter, **FALSE** indicates unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78d2b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78d2b-109">Return value</span></span>

<span data-ttu-id="78d2b-110">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="78d2b-110">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="78d2b-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78d2b-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="78d2b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78d2b-112">Remarks</span></span>

<span data-ttu-id="78d2b-113">Verwenden Sie diese Funktion, um die Filter einzurichten.</span><span class="sxs-lookup"><span data-stu-id="78d2b-113">Use this function to set up your filters.</span></span> <span data-ttu-id="78d2b-114">Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="78d2b-114">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78d2b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78d2b-115">Requirements</span></span>



| <span data-ttu-id="78d2b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78d2b-116">Requirement</span></span> | <span data-ttu-id="78d2b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="78d2b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78d2b-118">Header</span><span class="sxs-lookup"><span data-stu-id="78d2b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="78d2b-119"><dt>Dllsetup. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78d2b-119"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="78d2b-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78d2b-120">Library</span></span><br/> | <dl> <span data-ttu-id="78d2b-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="78d2b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78d2b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78d2b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d2b-123">**DLL-Setup Funktionen**</span><span class="sxs-lookup"><span data-stu-id="78d2b-123">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 





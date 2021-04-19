---
description: Veraltet. Verwenden Sie stattdessen AMovieDllRegisterServer2.
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: Amoviedllunregisterserver-Funktion (dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllUnregisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cab526a69f14cdd4c4f48767ca34722f61002eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359737"
---
# <a name="amoviedllunregisterserver-function"></a><span data-ttu-id="643ea-104">Amoviedllunregisterserver-Funktion</span><span class="sxs-lookup"><span data-stu-id="643ea-104">AMovieDllUnregisterServer function</span></span>

<span data-ttu-id="643ea-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="643ea-105">Obsolete.</span></span> <span data-ttu-id="643ea-106">Verwenden Sie stattdessen [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="643ea-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="643ea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="643ea-107">Syntax</span></span>


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="643ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="643ea-108">Parameters</span></span>

<span data-ttu-id="643ea-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="643ea-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="643ea-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="643ea-110">Return value</span></span>

<span data-ttu-id="643ea-111">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="643ea-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="643ea-112">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="643ea-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="643ea-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="643ea-113">Requirements</span></span>



| <span data-ttu-id="643ea-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="643ea-114">Requirement</span></span> | <span data-ttu-id="643ea-115">Wert</span><span class="sxs-lookup"><span data-stu-id="643ea-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="643ea-116">Header</span><span class="sxs-lookup"><span data-stu-id="643ea-116">Header</span></span><br/>  | <dl> <span data-ttu-id="643ea-117"><dt>Dllsetup. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="643ea-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="643ea-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="643ea-118">Library</span></span><br/> | <dl> <span data-ttu-id="643ea-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="643ea-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="643ea-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="643ea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="643ea-121">**DLL-Setup Funktionen**</span><span class="sxs-lookup"><span data-stu-id="643ea-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 





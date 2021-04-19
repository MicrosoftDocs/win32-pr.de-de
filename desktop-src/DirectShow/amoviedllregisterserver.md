---
description: Veraltet. Verwenden Sie stattdessen AMovieDllRegisterServer2.
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: Amoviedllregisterserver-Funktion (dllsetup. h)
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
ms.openlocfilehash: d93724c0f1ea6ed8b6cd2fa2b683a5ba9d45f0d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372616"
---
# <a name="amoviedllregisterserver-function"></a><span data-ttu-id="99ddf-104">Amoviedllregisterserver-Funktion</span><span class="sxs-lookup"><span data-stu-id="99ddf-104">AMovieDllRegisterServer function</span></span>

<span data-ttu-id="99ddf-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="99ddf-105">Obsolete.</span></span> <span data-ttu-id="99ddf-106">Verwenden Sie stattdessen [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="99ddf-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="99ddf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="99ddf-107">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="99ddf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="99ddf-108">Parameters</span></span>

<span data-ttu-id="99ddf-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="99ddf-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="99ddf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99ddf-110">Return value</span></span>

<span data-ttu-id="99ddf-111">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="99ddf-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="99ddf-112">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="99ddf-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="99ddf-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99ddf-113">Requirements</span></span>



| <span data-ttu-id="99ddf-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99ddf-114">Requirement</span></span> | <span data-ttu-id="99ddf-115">Wert</span><span class="sxs-lookup"><span data-stu-id="99ddf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99ddf-116">Header</span><span class="sxs-lookup"><span data-stu-id="99ddf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="99ddf-117"><dt>Dllsetup. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99ddf-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="99ddf-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="99ddf-118">Library</span></span><br/> | <dl> <span data-ttu-id="99ddf-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="99ddf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99ddf-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99ddf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99ddf-121">**DLL-Setup Funktionen**</span><span class="sxs-lookup"><span data-stu-id="99ddf-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 





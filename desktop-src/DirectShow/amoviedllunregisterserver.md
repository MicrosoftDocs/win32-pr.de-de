---
description: 'AMovieDllUnregisterServer-Funktion: Veraltet. Verwenden Sie stattdessen AMovieDllRegisterServer2.'
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: AMovieDllUnregisterServer-Funktion (Dllsetup.h)
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
ms.openlocfilehash: df7fb34246249298efc143b7ccc8e6332540867c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099928"
---
# <a name="amoviedllunregisterserver-function"></a><span data-ttu-id="e5b70-104">AMovieDllUnregisterServer-Funktion</span><span class="sxs-lookup"><span data-stu-id="e5b70-104">AMovieDllUnregisterServer function</span></span>

<span data-ttu-id="e5b70-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e5b70-105">Obsolete.</span></span> <span data-ttu-id="e5b70-106">Verwenden [**Sie stattdessen AMovieDllRegisterServer2.**](amoviedllregisterserver2.md)</span><span class="sxs-lookup"><span data-stu-id="e5b70-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5b70-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5b70-107">Syntax</span></span>


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="e5b70-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5b70-108">Parameters</span></span>

<span data-ttu-id="e5b70-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e5b70-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e5b70-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5b70-110">Return value</span></span>

<span data-ttu-id="e5b70-111">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="e5b70-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e5b70-112">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e5b70-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5b70-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5b70-113">Requirements</span></span>



| <span data-ttu-id="e5b70-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5b70-114">Requirement</span></span> | <span data-ttu-id="e5b70-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e5b70-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b70-116">Header</span><span class="sxs-lookup"><span data-stu-id="e5b70-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e5b70-117"><dt>Dllsetup.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="e5b70-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e5b70-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e5b70-118">Library</span></span><br/> | <dl> <span data-ttu-id="e5b70-119"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e5b70-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b70-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e5b70-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b70-121">**DLL-Setupfunktionen**</span><span class="sxs-lookup"><span data-stu-id="e5b70-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 





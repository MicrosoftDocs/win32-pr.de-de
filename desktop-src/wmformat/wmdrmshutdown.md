---
title: Wmdrmshutdown-Funktion (wmdrmsdk. h)
description: Die wmdrmshutdown-Funktion gibt Ressourcen frei, die von den erweiterten APIs des Windows Media DRM-Clients verwendet werden.
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- Wmdrmshutdown-Funktion Windows Media-Format
topic_type:
- apiref
api_name:
- WMDRMShutdown
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb49049a593699a4071eefea9c5cf7c61571fc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359227"
---
# <a name="wmdrmshutdown-function"></a><span data-ttu-id="72685-104">Wmdrmshutdown-Funktion</span><span class="sxs-lookup"><span data-stu-id="72685-104">WMDRMShutdown function</span></span>

<span data-ttu-id="72685-105">Die **wmdrmshutdown** -Funktion gibt Ressourcen frei, die von den erweiterten APIs des Windows Media DRM-Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72685-105">The **WMDRMShutdown** function releases resources used by the Windows Media DRM Client Extended APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="72685-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="72685-106">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a><span data-ttu-id="72685-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="72685-107">Parameters</span></span>

<span data-ttu-id="72685-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="72685-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72685-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72685-109">Return value</span></span>

<span data-ttu-id="72685-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="72685-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="72685-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="72685-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="72685-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="72685-112">Return code</span></span>                                                                          | <span data-ttu-id="72685-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72685-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="72685-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="72685-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="72685-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72685-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="72685-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72685-116">Remarks</span></span>

<span data-ttu-id="72685-117">Um Speicher Verluste zu vermeiden, müssen Sie diese Funktion für jeden Aufrufe der [**wmdrmstartup**](wmdrmstartup.md) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="72685-117">To avoid memory leaks, you must call this function for every call of the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="72685-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72685-118">Requirements</span></span>



| <span data-ttu-id="72685-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72685-119">Requirement</span></span> | <span data-ttu-id="72685-120">Wert</span><span class="sxs-lookup"><span data-stu-id="72685-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72685-121">Header</span><span class="sxs-lookup"><span data-stu-id="72685-121">Header</span></span><br/>  | <dl> <span data-ttu-id="72685-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="72685-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="72685-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="72685-123">Library</span></span><br/> | <dl> <span data-ttu-id="72685-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72685-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="72685-125">DLL</span><span class="sxs-lookup"><span data-stu-id="72685-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="72685-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72685-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72685-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72685-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72685-128">**Funktionen**</span><span class="sxs-lookup"><span data-stu-id="72685-128">**Functions**</span></span>](drm-functions.md)
</dt> </dl>

 

 






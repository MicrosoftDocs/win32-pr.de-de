---
title: Wmdrmstartup-Funktion (wmdrmsdk. h)
description: Die wmdrmstartup-Funktion initialisiert Ressourcen, die von den erweiterten APIs des Windows Media DRM-Clients verwendet werden.
ms.assetid: 2fd26bcc-8106-4356-933a-d4cf3536f4fb
keywords:
- Wmdrmstartup-Funktion Windows Media-Format
topic_type:
- apiref
api_name:
- WMDRMStartup
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c152a5160750f3c1943b455a8877b4615781b6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359691"
---
# <a name="wmdrmstartup-function"></a><span data-ttu-id="2e1f0-104">Wmdrmstartup-Funktion</span><span class="sxs-lookup"><span data-stu-id="2e1f0-104">WMDRMStartup function</span></span>

<span data-ttu-id="2e1f0-105">Die **wmdrmstartup** -Funktion initialisiert Ressourcen, die von den erweiterten APIs des Windows Media DRM-Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e1f0-105">The **WMDRMStartup** function initializes resources used by the Windows Media DRM Client Extended APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e1f0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e1f0-106">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMStartup(void);
```



## <a name="parameters"></a><span data-ttu-id="2e1f0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e1f0-107">Parameters</span></span>

<span data-ttu-id="2e1f0-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2e1f0-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e1f0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e1f0-109">Return value</span></span>

<span data-ttu-id="2e1f0-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="2e1f0-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2e1f0-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2e1f0-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2e1f0-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2e1f0-112">Return code</span></span>                                                                          | <span data-ttu-id="2e1f0-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e1f0-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2e1f0-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2e1f0-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2e1f0-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e1f0-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2e1f0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e1f0-116">Remarks</span></span>

<span data-ttu-id="2e1f0-117">Für jeden Aufrufe dieser Funktion müssen Sie [**wmdrmshutdown**](wmdrmshutdown.md) anrufen, um die verwendeten Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2e1f0-117">For every call of this function, you must call [**WMDRMShutdown**](wmdrmshutdown.md) to release the resources used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e1f0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e1f0-118">Requirements</span></span>



| <span data-ttu-id="2e1f0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e1f0-119">Requirement</span></span> | <span data-ttu-id="2e1f0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2e1f0-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e1f0-121">Header</span><span class="sxs-lookup"><span data-stu-id="2e1f0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2e1f0-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e1f0-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e1f0-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2e1f0-123">Library</span></span><br/> | <dl> <span data-ttu-id="2e1f0-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e1f0-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="2e1f0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2e1f0-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="2e1f0-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e1f0-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e1f0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e1f0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e1f0-128">**Funktionen**</span><span class="sxs-lookup"><span data-stu-id="2e1f0-128">**Functions**</span></span>](drm-functions.md)
</dt> </dl>

 

 






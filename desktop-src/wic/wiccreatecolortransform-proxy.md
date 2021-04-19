---
description: Erstellt ein Farb Transformations Objekt, das iwiccolortransform implementiert. Dieses com-Objekt unterstützt das frei Hand Thread-Objektmodell.
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: WICCreateColorTransform_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorTransform_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 451b549aa44e785e406f50ccf4eb7a8317edf6b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366921"
---
# <a name="wiccreatecolortransform_proxy-function"></a><span data-ttu-id="d72dd-104">Wickreatecolortransform- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="d72dd-104">WICCreateColorTransform\_Proxy function</span></span>

<span data-ttu-id="d72dd-105">Erstellt ein Farb Transformations Objekt, das [**iwiccolortransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform)implementiert.</span><span class="sxs-lookup"><span data-stu-id="d72dd-105">Creates an color transform object that implements [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform).</span></span> <span data-ttu-id="d72dd-106">Dieses com-Objekt unterstützt das frei Hand Thread-Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="d72dd-106">This COM object supports the free-threaded object model.</span></span>

## <a name="syntax"></a><span data-ttu-id="d72dd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d72dd-107">Syntax</span></span>


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a><span data-ttu-id="d72dd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d72dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d72dd-109">*ppicolortransform* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d72dd-109">*ppIColorTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d72dd-110">Die erstellte Farb Transformation.</span><span class="sxs-lookup"><span data-stu-id="d72dd-110">The color transform created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d72dd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d72dd-111">Return value</span></span>

<span data-ttu-id="d72dd-112">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d72dd-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d72dd-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d72dd-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d72dd-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d72dd-114">Requirements</span></span>



| <span data-ttu-id="d72dd-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d72dd-115">Requirement</span></span> | <span data-ttu-id="d72dd-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d72dd-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d72dd-117">DLL</span><span class="sxs-lookup"><span data-stu-id="d72dd-117">DLL</span></span><br/> | <dl> <span data-ttu-id="d72dd-118"><dt>WindowsCodecsExt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d72dd-118"><dt>WindowsCodecsExt.dll</dt></span></span> </dl> |



 

 

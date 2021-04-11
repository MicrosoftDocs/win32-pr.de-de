---
description: Proxy Funktion für die GetResolution-Methode.
ms.assetid: 5e261c2b-534a-4875-a84f-7251d54f15c6
title: IWICBitmapSource_GetResolution_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0bcd63c01bf99e426cdbf5044223a40308fb5e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216394"
---
# <a name="iwicbitmapsource_getresolution_proxy-function"></a><span data-ttu-id="4fe08-103">IWICBitmapSource \_ GetResolution- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="4fe08-103">IWICBitmapSource\_GetResolution\_Proxy function</span></span>

<span data-ttu-id="4fe08-104">Proxy Funktion für die [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4fe08-104">Proxy function for the [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fe08-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fe08-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetResolution_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ double           *pDpiX,
  _Out_ double           *pDpiY
);
```



## <a name="parameters"></a><span data-ttu-id="4fe08-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fe08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fe08-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fe08-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe08-108">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="4fe08-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="4fe08-109">Zeiger auf dieses [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4fe08-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="4fe08-110">*pdpix* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4fe08-110">*pDpiX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe08-111">Typ: \**Double \** _</span><span class="sxs-lookup"><span data-stu-id="4fe08-111">Type: \**double\** _</span></span>

<span data-ttu-id="4fe08-112">Ein Zeiger, der die x-Achse-dpi-Auflösung empfängt.</span><span class="sxs-lookup"><span data-stu-id="4fe08-112">A pointer that receives the x-axis dpi resolution.</span></span>

</dd> <dt>

<span data-ttu-id="4fe08-113">_pDpiY \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4fe08-113">_pDpiY\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe08-114">Typ: \**Double \** _</span><span class="sxs-lookup"><span data-stu-id="4fe08-114">Type: \**double\** _</span></span>

<span data-ttu-id="4fe08-115">Ein Zeiger, der die dpi-Auflösung der y-Achse empfängt.</span><span class="sxs-lookup"><span data-stu-id="4fe08-115">A pointer that receives the y-axis dpi resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fe08-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fe08-116">Return value</span></span>

<span data-ttu-id="4fe08-117">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4fe08-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4fe08-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="4fe08-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4fe08-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4fe08-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fe08-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fe08-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4fe08-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4fe08-121">Requirements</span></span>



| <span data-ttu-id="4fe08-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fe08-122">Requirement</span></span> | <span data-ttu-id="4fe08-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4fe08-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe08-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fe08-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4fe08-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fe08-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4fe08-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fe08-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4fe08-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fe08-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4fe08-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4fe08-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fe08-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fe08-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





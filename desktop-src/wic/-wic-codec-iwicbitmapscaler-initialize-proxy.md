---
description: 'IWICBitmapScaler_Initialize_Proxy-Funktion: Proxyfunktion für die Initialize-Methode.'
ms.assetid: 47a717d2-9aac-4230-bdb3-093212eb5448
title: IWICBitmapScaler_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapScaler_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 76b7c754273f4d55fbf3de9d8ba592806e590aac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100538"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a><span data-ttu-id="fd356-103">IWICBitmapScaler Initialize \_ \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd356-103">IWICBitmapScaler\_Initialize\_Proxy function</span></span>

<span data-ttu-id="fd356-104">Proxyfunktion für die [**Initialize-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize)</span><span class="sxs-lookup"><span data-stu-id="fd356-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd356-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd356-105">Syntax</span></span>


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a><span data-ttu-id="fd356-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd356-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd356-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd356-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd356-108">Typ: **[ **IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\***</span><span class="sxs-lookup"><span data-stu-id="fd356-108">Type: **[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\***</span></span>

<span data-ttu-id="fd356-109">Zeiger auf dieses [**IWICBitmapScaler-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)</span><span class="sxs-lookup"><span data-stu-id="fd356-109">Pointer to this [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) object.</span></span>

</dd> <dt>

<span data-ttu-id="fd356-110">*pISource* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fd356-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd356-111">Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="fd356-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="fd356-112">Die Eingabebitmapquelle.</span><span class="sxs-lookup"><span data-stu-id="fd356-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="fd356-113">*uiWidth* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fd356-113">*uiWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd356-114">Typ: **UINT**</span><span class="sxs-lookup"><span data-stu-id="fd356-114">Type: **UINT**</span></span>

<span data-ttu-id="fd356-115">Die Zielbreite.</span><span class="sxs-lookup"><span data-stu-id="fd356-115">The destination width.</span></span>

</dd> <dt>

<span data-ttu-id="fd356-116">*uiHeight* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fd356-116">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd356-117">Typ: **UINT**</span><span class="sxs-lookup"><span data-stu-id="fd356-117">Type: **UINT**</span></span>

<span data-ttu-id="fd356-118">Die Desinationshöhe.</span><span class="sxs-lookup"><span data-stu-id="fd356-118">The desination height.</span></span>

</dd> <dt>

<span data-ttu-id="fd356-119">*-Modus* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fd356-119">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd356-120">Typ: **[ **WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span><span class="sxs-lookup"><span data-stu-id="fd356-120">Type: **[**WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span></span>

<span data-ttu-id="fd356-121">Der Interpolationsmodus, der beim Skalieren verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd356-121">The interpolation mode to use when scaling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd356-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd356-122">Return value</span></span>

<span data-ttu-id="fd356-123">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fd356-123">Type: **HRESULT**</span></span>

<span data-ttu-id="fd356-124">Wenn diese Funktion erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fd356-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fd356-125">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fd356-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd356-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd356-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="fd356-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fd356-127">Requirements</span></span>



| <span data-ttu-id="fd356-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd356-128">Requirement</span></span> | <span data-ttu-id="fd356-129">Wert</span><span class="sxs-lookup"><span data-stu-id="fd356-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd356-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd356-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fd356-131">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd356-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="fd356-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd356-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fd356-133">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd356-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="fd356-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fd356-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd356-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd356-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





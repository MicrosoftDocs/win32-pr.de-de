---
description: Initialisiert eine iwiccolortransform mit einer IWICBitmapSource und wandelt sie von einem IWICColorContext in einen anderen um.
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: IWICColorTransform_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorTransform_Initialize_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 29d29bfd925d979897b22711c748083b94673142
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364673"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a><span data-ttu-id="f3a84-103">Iwiccolortransform- \_ \_ Proxy Funktion initialisieren</span><span class="sxs-lookup"><span data-stu-id="f3a84-103">IWICColorTransform\_Initialize\_Proxy function</span></span>

<span data-ttu-id="f3a84-104">Initialisiert eine [**iwiccolortransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) mit einer [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) und wandelt sie von einem [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) in einen anderen um.</span><span class="sxs-lookup"><span data-stu-id="f3a84-104">Initializes an [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) with a [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) and transforms it from one [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a84-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3a84-105">Syntax</span></span>


```C++
HRESULT IWICColorTransform_Initialize_Proxy(
  _In_ IWICColorTransform    *pIColorTransform,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ IWICColorContext      *pIContextSource,
  _In_ IWICColorContext      *pIContextDest,
  _In_ REFWICPixelFormatGUID pixelFmtDest
);
```



## <a name="parameters"></a><span data-ttu-id="f3a84-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3a84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3a84-107">*picolortransform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3a84-107">*pIColorTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3a84-108">Typ: **[ **iwiccolortransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***</span><span class="sxs-lookup"><span data-stu-id="f3a84-108">Type: **[**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***</span></span>

<span data-ttu-id="f3a84-109">Die Farb Transformation, die initialisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3a84-109">The color transform to initialize.</span></span>

</dd> <dt>

<span data-ttu-id="f3a84-110">*pibitmapsource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3a84-110">*pIBitmapSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3a84-111">Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="f3a84-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="f3a84-112">Die Bitmapquelle, die zum Initialisieren der Farb Transformation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f3a84-112">The bitmap source used to initialize the color transform.</span></span>

</dd> <dt>

<span data-ttu-id="f3a84-113">*picontextsource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3a84-113">*pIContextSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3a84-114">Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="f3a84-114">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

<span data-ttu-id="f3a84-115">Die Farb Kontext Quelle.</span><span class="sxs-lookup"><span data-stu-id="f3a84-115">The color context source.</span></span>

</dd> <dt>

<span data-ttu-id="f3a84-116">*picontextdest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3a84-116">*pIContextDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3a84-117">Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="f3a84-117">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

<span data-ttu-id="f3a84-118">Das Farb Kontext Ziel.</span><span class="sxs-lookup"><span data-stu-id="f3a84-118">The color context destination.</span></span>

</dd> <dt>

<span data-ttu-id="f3a84-119">*pixelfmtdest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3a84-119">*pixelFmtDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3a84-120">Typ: **reberwicpixelformatguid**</span><span class="sxs-lookup"><span data-stu-id="f3a84-120">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="f3a84-121">Die GUID des gewünschten Pixel Formats.</span><span class="sxs-lookup"><span data-stu-id="f3a84-121">The GUID of the desired pixel format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3a84-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3a84-122">Return value</span></span>

<span data-ttu-id="f3a84-123">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f3a84-123">Type: **HRESULT**</span></span>

<span data-ttu-id="f3a84-124">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f3a84-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f3a84-125">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f3a84-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a84-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3a84-126">Requirements</span></span>



| <span data-ttu-id="f3a84-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3a84-127">Requirement</span></span> | <span data-ttu-id="f3a84-128">Wert</span><span class="sxs-lookup"><span data-stu-id="f3a84-128">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a84-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f3a84-129">DLL</span></span><br/> | <dl> <span data-ttu-id="f3a84-130"><dt>WindowsCodecsExt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3a84-130"><dt>WindowsCodecsExt.dll</dt></span></span> </dl> |



 

 





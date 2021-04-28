---
description: 'IWICBitmapFrameEncode_SetResolution_Proxy-Funktion: Proxyfunktion für die SetResolution-Methode.'
ms.assetid: dc8df5bb-c38b-4be3-a4c6-60e7d5e1cd1b
title: IWICBitmapFrameEncode_SetResolution_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 632d6e797d499c4c5468505a4cee49e088ab025a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116608"
---
# <a name="iwicbitmapframeencode_setresolution_proxy-function"></a><span data-ttu-id="58747-103">IWICBitmapFrameEncode \_ \_ SetResolution-Proxyfunktion</span><span class="sxs-lookup"><span data-stu-id="58747-103">IWICBitmapFrameEncode\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="58747-104">Proxyfunktion für die [**SetResolution-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)</span><span class="sxs-lookup"><span data-stu-id="58747-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="58747-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58747-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetResolution_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ double                dpiX,
  _In_ double                dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="58747-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58747-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58747-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58747-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58747-108">Typ: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="58747-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="58747-109">Zeiger auf dieses [**IWICBitmapFrameEncode-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="58747-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="58747-110">*dpiX* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="58747-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58747-111">Typ: **double**</span><span class="sxs-lookup"><span data-stu-id="58747-111">Type: **double**</span></span>

<span data-ttu-id="58747-112">Der horizontale Auflösungswert.</span><span class="sxs-lookup"><span data-stu-id="58747-112">The horizontal resolution value.</span></span>

</dd> <dt>

<span data-ttu-id="58747-113">*dpiY* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="58747-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58747-114">Typ: **double**</span><span class="sxs-lookup"><span data-stu-id="58747-114">Type: **double**</span></span>

<span data-ttu-id="58747-115">Der vertikale Auflösungswert.</span><span class="sxs-lookup"><span data-stu-id="58747-115">The vertical resolution value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58747-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58747-116">Return value</span></span>

<span data-ttu-id="58747-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="58747-117">Type: **HRESULT**</span></span>

<span data-ttu-id="58747-118">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="58747-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="58747-119">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58747-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="58747-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58747-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="58747-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="58747-121">Requirements</span></span>



| <span data-ttu-id="58747-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58747-122">Requirement</span></span> | <span data-ttu-id="58747-123">Wert</span><span class="sxs-lookup"><span data-stu-id="58747-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58747-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58747-124">Minimum supported client</span></span><br/> | <span data-ttu-id="58747-125">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58747-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="58747-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58747-126">Minimum supported server</span></span><br/> | <span data-ttu-id="58747-127">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58747-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="58747-128">DLL</span><span class="sxs-lookup"><span data-stu-id="58747-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58747-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="58747-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





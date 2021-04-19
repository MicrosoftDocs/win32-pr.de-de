---
description: Proxy Funktion für die Methode "kreatebitmap".
ms.assetid: 5647521b-231d-4819-97ab-4dfb5f796211
title: IWICImagingFactory_CreateBitmap_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 56684de0280ae27bf2ec1e900bd718faec4733fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373250"
---
# <a name="iwicimagingfactory_createbitmap_proxy-function"></a><span data-ttu-id="51cac-103">IWICImagingFactory-Funktion zum Generieren von \_ \_ Funktionen</span><span class="sxs-lookup"><span data-stu-id="51cac-103">IWICImagingFactory\_CreateBitmap\_Proxy function</span></span>

<span data-ttu-id="51cac-104">Proxy Funktion für die Methode " [**kreatebitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap) ".</span><span class="sxs-lookup"><span data-stu-id="51cac-104">Proxy function for the [**CreateBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51cac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="51cac-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmap_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  UINT                       uiWidth,
  _In_  UINT                       uiHeight,
  _In_  REFWICPixelFormatGUID      pixelFormat,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="51cac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="51cac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51cac-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51cac-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51cac-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="51cac-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="51cac-109">_uiWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51cac-109">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51cac-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="51cac-110">Type: **UINT**</span></span>

<span data-ttu-id="51cac-111">Die Breite der neuen Bitmap.</span><span class="sxs-lookup"><span data-stu-id="51cac-111">The width of the new bitmap .</span></span>

</dd> <dt>

<span data-ttu-id="51cac-112">*uiheight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51cac-112">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51cac-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="51cac-113">Type: **UINT**</span></span>

<span data-ttu-id="51cac-114">Die Höhe der neuen Bitmap.</span><span class="sxs-lookup"><span data-stu-id="51cac-114">The height of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="51cac-115">*Pixel Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51cac-115">*pixelFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51cac-116">Typ: **reberwicpixelformatguid**</span><span class="sxs-lookup"><span data-stu-id="51cac-116">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="51cac-117">Das Pixel Format der neuen Bitmap.</span><span class="sxs-lookup"><span data-stu-id="51cac-117">The pixel format of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="51cac-118">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51cac-118">*option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51cac-119">Typ: **[ **wicbitmapkreatecacheoption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span><span class="sxs-lookup"><span data-stu-id="51cac-119">Type: **[**WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span></span>

<span data-ttu-id="51cac-120">Die Cache Erstellungs Optionen der neuen Bitmap.</span><span class="sxs-lookup"><span data-stu-id="51cac-120">The cache creation options of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="51cac-121">*ppibitmap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="51cac-121">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51cac-122">Typ: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="51cac-122">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="51cac-123">Ein Zeiger, der einen Zeiger auf die neue Bitmap empfängt.</span><span class="sxs-lookup"><span data-stu-id="51cac-123">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51cac-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51cac-124">Return value</span></span>

<span data-ttu-id="51cac-125">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="51cac-125">Type: **HRESULT**</span></span>

<span data-ttu-id="51cac-126">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="51cac-126">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="51cac-127">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="51cac-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="51cac-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51cac-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="51cac-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="51cac-129">Requirements</span></span>



| <span data-ttu-id="51cac-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51cac-130">Requirement</span></span> | <span data-ttu-id="51cac-131">Wert</span><span class="sxs-lookup"><span data-stu-id="51cac-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51cac-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51cac-132">Minimum supported client</span></span><br/> | <span data-ttu-id="51cac-133">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51cac-133">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="51cac-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51cac-134">Minimum supported server</span></span><br/> | <span data-ttu-id="51cac-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51cac-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="51cac-136">DLL</span><span class="sxs-lookup"><span data-stu-id="51cac-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51cac-137"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51cac-137"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





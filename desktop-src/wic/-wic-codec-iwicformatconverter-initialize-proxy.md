---
description: 'IWICFormatConverter_Initialize_Proxy-Funktion: Proxyfunktion für die Initialize-Methode.'
ms.assetid: 26112d52-95e2-4c67-83fc-cf5e28712730
title: IWICFormatConverter_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFormatConverter_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d70d852adc8f810438ce46dc30345e68fa27e0fd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097158"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a><span data-ttu-id="82b3b-103">IWICFormatConverter-Funktion \_ "Proxy initialisieren" \_</span><span class="sxs-lookup"><span data-stu-id="82b3b-103">IWICFormatConverter\_Initialize\_Proxy function</span></span>

<span data-ttu-id="82b3b-104">Proxyfunktion für die [**Initialize-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize)</span><span class="sxs-lookup"><span data-stu-id="82b3b-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="82b3b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="82b3b-105">Syntax</span></span>


```C++
HRESULT IWICFormatConverter_Initialize_Proxy(
  _In_ IWICFormatConverter   *THIS_PTR,
  _In_ IWICBitmapSource      *pISource,
  _In_ REFWICPixelFormatGUID dstFormat,
  _In_ WICBitmapDitherType   dither,
  _In_ IWICPalette           *pIPalette,
  _In_ double                alphaThresholdPercent,
  _In_ WICBitmapPaletteType  paletteTranslate
);
```



## <a name="parameters"></a><span data-ttu-id="82b3b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="82b3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82b3b-107">*DIES \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82b3b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b3b-108">Typ: **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\***</span><span class="sxs-lookup"><span data-stu-id="82b3b-108">Type: **[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\***</span></span>

<span data-ttu-id="82b3b-109">Zeiger auf dieses [**IWICFormatConverter-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)</span><span class="sxs-lookup"><span data-stu-id="82b3b-109">Pointer to this [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span>

</dd> <dt>

<span data-ttu-id="82b3b-110">*pISource* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="82b3b-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b3b-111">Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="82b3b-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="82b3b-112">Die zu konvertierende Eingabebitmap</span><span class="sxs-lookup"><span data-stu-id="82b3b-112">The input bitmap to convert</span></span>

</dd> <dt>

<span data-ttu-id="82b3b-113">*dstFormat* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="82b3b-113">*dstFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b3b-114">Typ: **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="82b3b-114">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="82b3b-115">Die Zielpixelformat-GUID.</span><span class="sxs-lookup"><span data-stu-id="82b3b-115">The destination pixel format GUID.</span></span>

</dd> <dt>

<span data-ttu-id="82b3b-116">*Dither* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="82b3b-116">*dither* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b3b-117">Typ: **[ **WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span><span class="sxs-lookup"><span data-stu-id="82b3b-117">Type: **[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span></span>

<span data-ttu-id="82b3b-118">Der für die Konvertierung verwendete [**WICBitmapDitherType.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)</span><span class="sxs-lookup"><span data-stu-id="82b3b-118">The [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) used for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="82b3b-119">*pIPalette* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="82b3b-119">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b3b-120">Typ: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="82b3b-120">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="82b3b-121">Die Palette, die für die Konvertierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="82b3b-121">The palette to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="82b3b-122">*alphaThresholdPercent* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="82b3b-122">*alphaThresholdPercent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b3b-123">Typ: **double**</span><span class="sxs-lookup"><span data-stu-id="82b3b-123">Type: **double**</span></span>

<span data-ttu-id="82b3b-124">Der Alphaschwellenwert, der für die Konvertierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="82b3b-124">The alpha threshold to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="82b3b-125">*paletteTranslate* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="82b3b-125">*paletteTranslate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b3b-126">Typ: **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="82b3b-126">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="82b3b-127">Der Für die Konvertierung zu verwendende Palettenübersetzungstyp.</span><span class="sxs-lookup"><span data-stu-id="82b3b-127">The palette translation type to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82b3b-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82b3b-128">Return value</span></span>

<span data-ttu-id="82b3b-129">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="82b3b-129">Type: **HRESULT**</span></span>

<span data-ttu-id="82b3b-130">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="82b3b-130">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="82b3b-131">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="82b3b-131">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="82b3b-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82b3b-132">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="82b3b-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="82b3b-133">Requirements</span></span>



| <span data-ttu-id="82b3b-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82b3b-134">Requirement</span></span> | <span data-ttu-id="82b3b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="82b3b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82b3b-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82b3b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="82b3b-137">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82b3b-137">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="82b3b-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82b3b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="82b3b-139">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82b3b-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="82b3b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="82b3b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82b3b-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="82b3b-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





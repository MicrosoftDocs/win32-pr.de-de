---
description: Proxy Funktion für die Initialize-Methode.
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
ms.openlocfilehash: 6450c1a508507db73e44ef8b88b4f94970ac6004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217666"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a><span data-ttu-id="72a77-103">IWICFormatConverter \_ Initialisieren der \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="72a77-103">IWICFormatConverter\_Initialize\_Proxy function</span></span>

<span data-ttu-id="72a77-104">Proxy Funktion für die [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) -Methode.</span><span class="sxs-lookup"><span data-stu-id="72a77-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="72a77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="72a77-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="72a77-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72a77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72a77-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72a77-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72a77-108">Typ: \**[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) \** _</span><span class="sxs-lookup"><span data-stu-id="72a77-108">Type: \**[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\** _</span></span>

<span data-ttu-id="72a77-109">Zeiger auf dieses [_ *IWICFormatConverter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="72a77-109">Pointer to this [_ *IWICFormatConverter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span>

</dd> <dt>

<span data-ttu-id="72a77-110">*pisource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72a77-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72a77-111">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="72a77-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="72a77-112">Die zu konvertierende Eingabe Bitmap.</span><span class="sxs-lookup"><span data-stu-id="72a77-112">The input bitmap to convert</span></span>

</dd> <dt>

<span data-ttu-id="72a77-113">_dstFormat \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72a77-113">_dstFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72a77-114">Typ: **reberwicpixelformatguid**</span><span class="sxs-lookup"><span data-stu-id="72a77-114">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="72a77-115">Die GUID des Ziel Pixel Formats.</span><span class="sxs-lookup"><span data-stu-id="72a77-115">The destination pixel format GUID.</span></span>

</dd> <dt>

<span data-ttu-id="72a77-116">*Dithering* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72a77-116">*dither* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72a77-117">Typ: **[ **wicbitmapdithertype**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span><span class="sxs-lookup"><span data-stu-id="72a77-117">Type: **[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span></span>

<span data-ttu-id="72a77-118">Der für die Konvertierung verwendete [**wicbitmapdithertype**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) .</span><span class="sxs-lookup"><span data-stu-id="72a77-118">The [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) used for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="72a77-119">*pipalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72a77-119">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72a77-120">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="72a77-120">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="72a77-121">Die für die Konvertierung zu verwendende Palette.</span><span class="sxs-lookup"><span data-stu-id="72a77-121">The palette to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="72a77-122">_alphaThresholdPercent \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72a77-122">_alphaThresholdPercent\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72a77-123">Typ: **Double**</span><span class="sxs-lookup"><span data-stu-id="72a77-123">Type: **double**</span></span>

<span data-ttu-id="72a77-124">Der für die Konvertierung zu verwendende Alpha Schwellenwert.</span><span class="sxs-lookup"><span data-stu-id="72a77-124">The alpha threshold to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="72a77-125">*palettetranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72a77-125">*paletteTranslate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72a77-126">Typ: **[ **wicbitmappalettetype**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="72a77-126">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="72a77-127">Der palettenübersetzungs Typ, der für die Konvertierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72a77-127">The palette translation type to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72a77-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72a77-128">Return value</span></span>

<span data-ttu-id="72a77-129">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="72a77-129">Type: **HRESULT**</span></span>

<span data-ttu-id="72a77-130">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="72a77-130">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="72a77-131">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="72a77-131">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="72a77-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72a77-132">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="72a77-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="72a77-133">Requirements</span></span>



| <span data-ttu-id="72a77-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72a77-134">Requirement</span></span> | <span data-ttu-id="72a77-135">Wert</span><span class="sxs-lookup"><span data-stu-id="72a77-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72a77-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72a77-136">Minimum supported client</span></span><br/> | <span data-ttu-id="72a77-137">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72a77-137">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="72a77-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72a77-138">Minimum supported server</span></span><br/> | <span data-ttu-id="72a77-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72a77-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="72a77-140">DLL</span><span class="sxs-lookup"><span data-stu-id="72a77-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72a77-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72a77-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





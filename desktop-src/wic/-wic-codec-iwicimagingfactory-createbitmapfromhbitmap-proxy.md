---
description: Proxy Funktion für die Methode "kreatebitmapfromhbitmap".
ms.assetid: e4e9a6b4-00d9-4f87-aeec-f2c02c3f44ab
title: IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6599a9699e6fb83c1678cd0360f906cc8e0668c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351466"
---
# <a name="iwicimagingfactory_createbitmapfromhbitmap_proxy-function"></a><span data-ttu-id="6c442-103">IWICImagingFactory- \_ Funktion "endbitmapfromhbitmap" \_</span><span class="sxs-lookup"><span data-stu-id="6c442-103">IWICImagingFactory\_CreateBitmapFromHBITMAP\_Proxy function</span></span>

<span data-ttu-id="6c442-104">Proxy Funktion für die Methode " [**kreatebitmapfromhbitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) ".</span><span class="sxs-lookup"><span data-stu-id="6c442-104">Proxy function for the [**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c442-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c442-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy(
  _In_  IWICImagingFactory          *pFactory,
  _In_  HBITMAP                     hBitmap,
  _In_  HPALETTE                    hPalette,
  _In_  WICBitmapAlphaChannelOption options,
  _Out_ IWICBitmap                  **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="6c442-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c442-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c442-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c442-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c442-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="6c442-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="6c442-109">_hBitmap \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c442-109">_hBitmap\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c442-110">Typ: **hBitmap**</span><span class="sxs-lookup"><span data-stu-id="6c442-110">Type: **HBITMAP**</span></span>

<span data-ttu-id="6c442-111">Ein Bitmap-Handle, aus dem die Bitmap erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c442-111">A bitmap handle to create the bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="6c442-112">*hpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c442-112">*hPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c442-113">Typ: **hpalette**</span><span class="sxs-lookup"><span data-stu-id="6c442-113">Type: **HPALETTE**</span></span>

<span data-ttu-id="6c442-114">Ein Palettenhandle, das zum Erstellen der Bitmap verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6c442-114">A palette handle used to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="6c442-115">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c442-115">*options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c442-116">Typ: **[ **wicbitmapalphachanneloption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**</span><span class="sxs-lookup"><span data-stu-id="6c442-116">Type: **[**WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**</span></span>

<span data-ttu-id="6c442-117">Die Alphakanal Optionen zum Erstellen der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="6c442-117">The alpha channel options to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="6c442-118">*ppibitmap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6c442-118">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c442-119">Typ: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="6c442-119">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="6c442-120">Ein Zeiger, der einen Zeiger auf die neue Bitmap empfängt.</span><span class="sxs-lookup"><span data-stu-id="6c442-120">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c442-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c442-121">Return value</span></span>

<span data-ttu-id="6c442-122">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6c442-122">Type: **HRESULT**</span></span>

<span data-ttu-id="6c442-123">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6c442-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6c442-124">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c442-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c442-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c442-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6c442-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6c442-126">Requirements</span></span>



| <span data-ttu-id="6c442-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c442-127">Requirement</span></span> | <span data-ttu-id="6c442-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6c442-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c442-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c442-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6c442-130">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c442-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6c442-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c442-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6c442-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c442-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6c442-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6c442-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c442-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c442-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





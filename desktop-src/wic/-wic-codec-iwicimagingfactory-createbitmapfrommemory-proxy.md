---
description: Proxy Funktion für die Methode "kreatebitmapfrommemory".
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: IWICImagingFactory_CreateBitmapFromMemory_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 79893952bb6dcdbab6c4a1cea4f57355831d31c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351025"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a><span data-ttu-id="2edf2-103">IWICImagingFactory- \_ Funktion "endbitmapfrommemory" \_</span><span class="sxs-lookup"><span data-stu-id="2edf2-103">IWICImagingFactory\_CreateBitmapFromMemory\_Proxy function</span></span>

<span data-ttu-id="2edf2-104">Proxy Funktion für die Methode " [**kreatebitmapfrommemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) ".</span><span class="sxs-lookup"><span data-stu-id="2edf2-104">Proxy function for the [**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2edf2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2edf2-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromMemory_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _In_  UINT                  uiWidth,
  _In_  UINT                  uiHeight,
  _In_  REFWICPixelFormatGUID pixelFormat,
  _In_  UINT                  cbStride,
  _In_  UINT                  cbBufferSize,
  _In_  BYTE                  *pbBuffer,
  _Out_ IWICBitmap            **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="2edf2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2edf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2edf2-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2edf2-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2edf2-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="2edf2-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="2edf2-109">_uiWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2edf2-109">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2edf2-110">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="2edf2-110">Type: **UINT**</span></span>

<span data-ttu-id="2edf2-111">Die Breite der neuen Bitmap.</span><span class="sxs-lookup"><span data-stu-id="2edf2-111">The width of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="2edf2-112">*uiheight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2edf2-112">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2edf2-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="2edf2-113">Type: **UINT**</span></span>

<span data-ttu-id="2edf2-114">Die Höhe der neuen Bitmap.</span><span class="sxs-lookup"><span data-stu-id="2edf2-114">The height of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="2edf2-115">*Pixel Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2edf2-115">*pixelFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2edf2-116">Typ: **reberwicpixelformatguid**</span><span class="sxs-lookup"><span data-stu-id="2edf2-116">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="2edf2-117">Das Pixel Format der neuen Bitmap.</span><span class="sxs-lookup"><span data-stu-id="2edf2-117">The pixel format of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="2edf2-118">*cbStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2edf2-118">*cbStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2edf2-119">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="2edf2-119">Type: **UINT**</span></span>

<span data-ttu-id="2edf2-120">Der [*Schritt*](/windows) der angegebenen Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="2edf2-120">The [*stride*](/windows) of the given pixel data.</span></span>

</dd> <dt>

<span data-ttu-id="2edf2-121">*cbBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2edf2-121">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2edf2-122">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="2edf2-122">Type: **UINT**</span></span>

<span data-ttu-id="2edf2-123">Die Größe von *pbBuffer*.</span><span class="sxs-lookup"><span data-stu-id="2edf2-123">The size of *pbBuffer*.</span></span>

</dd> <dt>

<span data-ttu-id="2edf2-124">*pbBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2edf2-124">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2edf2-125">Typ: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="2edf2-125">Type: \**BYTE\** _</span></span>

<span data-ttu-id="2edf2-126">Der zum Erstellen der Bitmap verwendete Puffer.</span><span class="sxs-lookup"><span data-stu-id="2edf2-126">The buffer used to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="2edf2-127">_ppIBitmap \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2edf2-127">_ppIBitmap\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2edf2-128">Typ: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="2edf2-128">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="2edf2-129">Ein Zeiger, der einen Zeiger auf die neue Bitmap empfängt.</span><span class="sxs-lookup"><span data-stu-id="2edf2-129">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2edf2-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2edf2-130">Return value</span></span>

<span data-ttu-id="2edf2-131">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2edf2-131">Type: **HRESULT**</span></span>

<span data-ttu-id="2edf2-132">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2edf2-132">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2edf2-133">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2edf2-133">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2edf2-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2edf2-134">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2edf2-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2edf2-135">Requirements</span></span>



| <span data-ttu-id="2edf2-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2edf2-136">Requirement</span></span> | <span data-ttu-id="2edf2-137">Wert</span><span class="sxs-lookup"><span data-stu-id="2edf2-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2edf2-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2edf2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2edf2-139">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2edf2-139">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2edf2-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2edf2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2edf2-141">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2edf2-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2edf2-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2edf2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2edf2-143"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2edf2-143"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 


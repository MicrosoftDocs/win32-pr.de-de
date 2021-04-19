---
description: Proxy Funktion für die getbitsperpixel-Methode.
ms.assetid: bb98daeb-3886-473b-9c8e-5c606602249a
title: IWICPixelFormatInfo_GetBitsPerPixel_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetBitsPerPixel_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f8d3469ca7c1eacf1f6755cbf5b6243527639d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355336"
---
# <a name="iwicpixelformatinfo_getbitsperpixel_proxy-function"></a><span data-ttu-id="7d93c-103">Iwicpixelformatinfo- \_ getbitsperpixel- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="7d93c-103">IWICPixelFormatInfo\_GetBitsPerPixel\_Proxy function</span></span>

<span data-ttu-id="7d93c-104">Proxy Funktion für die [**getbitsperpixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7d93c-104">Proxy function for the [**GetBitsPerPixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d93c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d93c-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetBitsPerPixel_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiBitsPerPixel
);
```



## <a name="parameters"></a><span data-ttu-id="7d93c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d93c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d93c-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d93c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d93c-108">Typ: \**[**iwicpixelformatinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="7d93c-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="7d93c-109">Zeiger auf dieses [_ *iwicpixelformatinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7d93c-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="7d93c-110">*puibitsperpixel* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7d93c-110">*puiBitsPerPixel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d93c-111">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="7d93c-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="7d93c-112">Ein Zeiger, der den bpp des Pixel Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="7d93c-112">Pointer that receives the BPP of the pixel format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d93c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d93c-113">Return value</span></span>

<span data-ttu-id="7d93c-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="7d93c-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="7d93c-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7d93c-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7d93c-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7d93c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d93c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d93c-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7d93c-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7d93c-118">Requirements</span></span>



| <span data-ttu-id="7d93c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d93c-119">Requirement</span></span> | <span data-ttu-id="7d93c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7d93c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d93c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d93c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7d93c-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d93c-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7d93c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d93c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7d93c-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d93c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7d93c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7d93c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d93c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d93c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





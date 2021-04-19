---
description: Proxy Funktion für das Aushandeln des Pixel Formats und der Palette für den Encoder.
ms.assetid: 01179598-ba40-4aed-a7c4-888cb4e851f4
title: WICSetEncoderFormat_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICSetEncoderFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7ea0988d29d1d9ed04668dfbe8ce86b97af6534a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348070"
---
# <a name="wicsetencoderformat_proxy-function"></a><span data-ttu-id="20254-103">Wicsetencoderformat- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="20254-103">WICSetEncoderFormat\_Proxy function</span></span>

<span data-ttu-id="20254-104">Proxy Funktion für das Aushandeln des Pixel Formats und der Palette für den Encoder.</span><span class="sxs-lookup"><span data-stu-id="20254-104">Proxy function for negotiating the pixel format and the palette for the encoder.</span></span>

## <a name="syntax"></a><span data-ttu-id="20254-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="20254-105">Syntax</span></span>


```C++
HRESULT WICSetEncoderFormat_Proxy(
  _In_  IWICBitmapSource      *pSourceIn,
  _In_  IWICPalette           *pIPalette,
  _In_  IWICBitmapFrameEncode *pIFrameEncode,
  _Out_ IWICBitmapSource      **ppSourceOut
);
```



## <a name="parameters"></a><span data-ttu-id="20254-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20254-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20254-107">*psourcein* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20254-107">*pSourceIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20254-108">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="20254-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="20254-109">Ein Zeiger auf die Quell Bitmap.</span><span class="sxs-lookup"><span data-stu-id="20254-109">Pointer to the source bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="20254-110">_pIPalette \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20254-110">_pIPalette\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20254-111">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="20254-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="20254-112">Zeiger auf die Palette, die für die Codierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="20254-112">Pointer to the palette to use for encoding.</span></span>

</dd> <dt>

<span data-ttu-id="20254-113">_pIFrameEncode \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20254-113">_pIFrameEncode\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20254-114">Typ: \**[**iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="20254-114">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="20254-115">Zeiger auf das Frame-codierobjekt.</span><span class="sxs-lookup"><span data-stu-id="20254-115">Pointer to the frame encode object.</span></span>

</dd> <dt>

<span data-ttu-id="20254-116">_ppSourceOut \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="20254-116">_ppSourceOut\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20254-117">Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="20254-117">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="20254-118">Ein Zeiger, der einen Zeiger auf die Ausgabe Quelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="20254-118">Pointer that receives a pointer to the output source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20254-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20254-119">Return value</span></span>

<span data-ttu-id="20254-120">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="20254-120">Type: **HRESULT**</span></span>

<span data-ttu-id="20254-121">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="20254-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="20254-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="20254-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="20254-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20254-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="20254-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="20254-124">Requirements</span></span>



| <span data-ttu-id="20254-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20254-125">Requirement</span></span> | <span data-ttu-id="20254-126">Wert</span><span class="sxs-lookup"><span data-stu-id="20254-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20254-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20254-127">Minimum supported client</span></span><br/> | <span data-ttu-id="20254-128">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20254-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="20254-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20254-129">Minimum supported server</span></span><br/> | <span data-ttu-id="20254-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20254-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="20254-131">DLL</span><span class="sxs-lookup"><span data-stu-id="20254-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20254-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20254-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





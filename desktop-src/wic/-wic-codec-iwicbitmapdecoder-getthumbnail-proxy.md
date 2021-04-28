---
description: 'IWICBitmapDecoder_GetThumbnail_Proxy-Funktion: Proxyfunktion für die GetThumbnail-Methode.'
ms.assetid: 37a6ba78-0d1b-47f6-9b12-8ad123c8ee86
title: IWICBitmapDecoder_GetThumbnail_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3fb4d6ae050772bb6392e1d94c88ef5bfc23d2ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100608"
---
# <a name="iwicbitmapdecoder_getthumbnail_proxy-function"></a><span data-ttu-id="0ea3d-103">IWICBitmapDecoder \_ GetThumbnail-Proxyfunktion \_</span><span class="sxs-lookup"><span data-stu-id="0ea3d-103">IWICBitmapDecoder\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="0ea3d-104">Proxyfunktion für die [**GetThumbnail-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)</span><span class="sxs-lookup"><span data-stu-id="0ea3d-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea3d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ea3d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetThumbnail_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="0ea3d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ea3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ea3d-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ea3d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ea3d-108">Typ: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="0ea3d-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="0ea3d-109">Zeiger auf dieses [**IWICBitmapDecoder-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)</span><span class="sxs-lookup"><span data-stu-id="0ea3d-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="0ea3d-110">*ppIThumbnail* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0ea3d-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ea3d-111">Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="0ea3d-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="0ea3d-112">Ein Zeiger, der einen Zeiger auf [**die IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) der Miniaturansicht empfängt.</span><span class="sxs-lookup"><span data-stu-id="0ea3d-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ea3d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ea3d-113">Return value</span></span>

<span data-ttu-id="0ea3d-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0ea3d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0ea3d-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="0ea3d-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0ea3d-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0ea3d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ea3d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ea3d-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0ea3d-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0ea3d-118">Requirements</span></span>



| <span data-ttu-id="0ea3d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ea3d-119">Requirement</span></span> | <span data-ttu-id="0ea3d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0ea3d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea3d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ea3d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0ea3d-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ea3d-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0ea3d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ea3d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0ea3d-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ea3d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0ea3d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0ea3d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ea3d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ea3d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





---
description: 'IWICBitmapFrameEncode_SetThumbnail_Proxy-Funktion: Proxyfunktion für die SetThumbnail-Methode.'
ms.assetid: 3ad473ec-9218-4ed1-961d-a2aa0d542119
title: IWICBitmapFrameEncode_SetThumbnail_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9af9dd2d4f8fe71a6dc94420db17383a5da6da28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116598"
---
# <a name="iwicbitmapframeencode_setthumbnail_proxy-function"></a><span data-ttu-id="79ff6-103">IWICBitmapFrameEncode \_ SetThumbnail-Proxyfunktion \_</span><span class="sxs-lookup"><span data-stu-id="79ff6-103">IWICBitmapFrameEncode\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="79ff6-104">Proxyfunktion für die [**SetThumbnail-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)</span><span class="sxs-lookup"><span data-stu-id="79ff6-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="79ff6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="79ff6-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetThumbnail_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="79ff6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79ff6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79ff6-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79ff6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79ff6-108">Typ: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="79ff6-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="79ff6-109">Zeiger auf dieses [**IWICBitmapFrameEncode-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="79ff6-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="79ff6-110">*pIThumbnail* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="79ff6-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79ff6-111">Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="79ff6-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="79ff6-112">Die Bitmapquelle, die als Miniaturansicht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="79ff6-112">The bitmap source to use as the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79ff6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79ff6-113">Return value</span></span>

<span data-ttu-id="79ff6-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="79ff6-114">Type: **HRESULT**</span></span>

<span data-ttu-id="79ff6-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="79ff6-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="79ff6-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="79ff6-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="79ff6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79ff6-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="79ff6-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="79ff6-118">Requirements</span></span>



| <span data-ttu-id="79ff6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79ff6-119">Requirement</span></span> | <span data-ttu-id="79ff6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="79ff6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79ff6-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79ff6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="79ff6-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79ff6-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="79ff6-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79ff6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="79ff6-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79ff6-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="79ff6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="79ff6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79ff6-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="79ff6-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





---
description: Proxy Funktion für die setminiatur-Methode.
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
ms.openlocfilehash: 052e73911178ef0db957c5dd8edcf6e9d6892ace
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866768"
---
# <a name="iwicbitmapframeencode_setthumbnail_proxy-function"></a><span data-ttu-id="48006-103">IWICBitmapFrameEncode- \_ setminiatur- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="48006-103">IWICBitmapFrameEncode\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="48006-104">Proxy Funktion für die [**setminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) -Methode.</span><span class="sxs-lookup"><span data-stu-id="48006-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="48006-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48006-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetThumbnail_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="48006-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48006-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48006-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48006-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48006-108">Typ: \**[**iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="48006-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="48006-109">Zeiger auf dieses [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="48006-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="48006-110">*piminiatur* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48006-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48006-111">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="48006-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="48006-112">Die als Miniaturansicht zu verwendende Bitmapquelle.</span><span class="sxs-lookup"><span data-stu-id="48006-112">The bitmap source to use as the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48006-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48006-113">Return value</span></span>

<span data-ttu-id="48006-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="48006-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="48006-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="48006-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="48006-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48006-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="48006-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48006-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="48006-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="48006-118">Requirements</span></span>



| <span data-ttu-id="48006-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48006-119">Requirement</span></span> | <span data-ttu-id="48006-120">Wert</span><span class="sxs-lookup"><span data-stu-id="48006-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48006-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48006-121">Minimum supported client</span></span><br/> | <span data-ttu-id="48006-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48006-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="48006-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48006-123">Minimum supported server</span></span><br/> | <span data-ttu-id="48006-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48006-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="48006-125">DLL</span><span class="sxs-lookup"><span data-stu-id="48006-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48006-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48006-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





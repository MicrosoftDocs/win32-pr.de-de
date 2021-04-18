---
description: Proxy Funktion für die GetPixelFormat-Methode.
ms.assetid: 0879bfb7-0175-4275-a093-a69b39c66a41
title: IWICBitmapSource_GetPixelFormat_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetPixelFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ff795dd028c8d8f1e18a944df60a87f1e7cee670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358973"
---
# <a name="iwicbitmapsource_getpixelformat_proxy-function"></a><span data-ttu-id="13658-103">IWICBitmapSource \_ GetPixelFormat- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="13658-103">IWICBitmapSource\_GetPixelFormat\_Proxy function</span></span>

<span data-ttu-id="13658-104">Proxy Funktion für die [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="13658-104">Proxy function for the [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="13658-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13658-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetPixelFormat_Proxy(
  _In_  IWICBitmapSource   *THIS_PTR,
  _Out_ WICPixelFormatGUID *pPixelFormat
);
```



## <a name="parameters"></a><span data-ttu-id="13658-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13658-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13658-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13658-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13658-108">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="13658-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="13658-109">Zeiger auf dieses [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="13658-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="13658-110">*pPixelFormat* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13658-110">*pPixelFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13658-111">Geben Sie Folgendes ein: \**wicpixelformatguid \** _</span><span class="sxs-lookup"><span data-stu-id="13658-111">Type: \**WICPixelFormatGUID\** _</span></span>

<span data-ttu-id="13658-112">Ein Zeiger, der die GUID des Pixel Formats empfängt, in der die Bitmap gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="13658-112">A pointer that receives the pixel format GUID the bitmap is stored in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13658-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13658-113">Return value</span></span>

<span data-ttu-id="13658-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="13658-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="13658-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="13658-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="13658-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13658-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="13658-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13658-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="13658-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="13658-118">Requirements</span></span>



| <span data-ttu-id="13658-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13658-119">Requirement</span></span> | <span data-ttu-id="13658-120">Wert</span><span class="sxs-lookup"><span data-stu-id="13658-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13658-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13658-121">Minimum supported client</span></span><br/> | <span data-ttu-id="13658-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13658-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="13658-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13658-123">Minimum supported server</span></span><br/> | <span data-ttu-id="13658-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13658-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="13658-125">DLL</span><span class="sxs-lookup"><span data-stu-id="13658-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13658-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13658-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





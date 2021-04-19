---
description: Proxy Funktion für die getminiatur-Methode.
ms.assetid: 377f8aac-3cdc-44dc-8c60-9b6bce915486
title: IWICBitmapFrameDecode_GetThumbnail_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c29b62b4d3839b7cd3db51574f38ab824b215310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356739"
---
# <a name="iwicbitmapframedecode_getthumbnail_proxy-function"></a><span data-ttu-id="bb3a9-103">IWICBitmapFrameDecode \_ getminiatur- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="bb3a9-103">IWICBitmapFrameDecode\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="bb3a9-104">Proxy Funktion für die [**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bb3a9-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb3a9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb3a9-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetThumbnail_Proxy(
  _In_  IWICBitmapFrameDecode *THIS_PTR,
  _Out_ IWICBitmapSource      **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="bb3a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb3a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb3a9-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb3a9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb3a9-108">Typ: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="bb3a9-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="bb3a9-109">Zeiger auf dieses [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="bb3a9-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="bb3a9-110">*ppiminiatur Ansicht* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bb3a9-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb3a9-111">Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="bb3a9-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="bb3a9-112">Ein Zeiger, der einen Zeiger auf die [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) der Miniaturansicht empfängt.</span><span class="sxs-lookup"><span data-stu-id="bb3a9-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb3a9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb3a9-113">Return value</span></span>

<span data-ttu-id="bb3a9-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bb3a9-114">Type: **HRESULT**</span></span>

<span data-ttu-id="bb3a9-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="bb3a9-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb3a9-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bb3a9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb3a9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb3a9-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bb3a9-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bb3a9-118">Requirements</span></span>



| <span data-ttu-id="bb3a9-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb3a9-119">Requirement</span></span> | <span data-ttu-id="bb3a9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="bb3a9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb3a9-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb3a9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bb3a9-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb3a9-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bb3a9-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb3a9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bb3a9-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb3a9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bb3a9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bb3a9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb3a9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb3a9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





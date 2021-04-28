---
description: 'IWICBitmapFrameDecode_GetThumbnail_Proxy-Funktion: Proxyfunktion für die GetThumbnail-Methode.'
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
ms.openlocfilehash: 7f3c94461ac13aa39d14b97f13fe5e9e8d7569a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113638"
---
# <a name="iwicbitmapframedecode_getthumbnail_proxy-function"></a><span data-ttu-id="dd2b3-103">IWICBitmapFrameDecode \_ GetThumbnail-Proxyfunktion \_</span><span class="sxs-lookup"><span data-stu-id="dd2b3-103">IWICBitmapFrameDecode\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="dd2b3-104">Proxyfunktion für die [**GetThumbnail-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)</span><span class="sxs-lookup"><span data-stu-id="dd2b3-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd2b3-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetThumbnail_Proxy(
  _In_  IWICBitmapFrameDecode *THIS_PTR,
  _Out_ IWICBitmapSource      **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="dd2b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd2b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd2b3-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd2b3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2b3-108">Typ: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="dd2b3-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="dd2b3-109">Zeiger auf dieses [**IWICBitmapFrameDecode-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)</span><span class="sxs-lookup"><span data-stu-id="dd2b3-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="dd2b3-110">*ppIThumbnail* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dd2b3-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2b3-111">Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="dd2b3-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="dd2b3-112">Ein Zeiger, der einen Zeiger auf [**die IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) der Miniaturansicht empfängt.</span><span class="sxs-lookup"><span data-stu-id="dd2b3-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd2b3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd2b3-113">Return value</span></span>

<span data-ttu-id="dd2b3-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dd2b3-114">Type: **HRESULT**</span></span>

<span data-ttu-id="dd2b3-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="dd2b3-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dd2b3-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dd2b3-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd2b3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd2b3-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="dd2b3-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="dd2b3-118">Requirements</span></span>



| <span data-ttu-id="dd2b3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd2b3-119">Requirement</span></span> | <span data-ttu-id="dd2b3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="dd2b3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2b3-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd2b3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dd2b3-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd2b3-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="dd2b3-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd2b3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dd2b3-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd2b3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="dd2b3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dd2b3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd2b3-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd2b3-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





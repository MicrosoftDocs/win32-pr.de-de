---
description: Proxy Funktion für die GetSize-Methode.
ms.assetid: a9b7d01c-78d9-47b8-a373-a7c49f7bccfd
title: IWICBitmapSource_GetSize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 978748125b7c7f643027077182b9136b577cb00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349902"
---
# <a name="iwicbitmapsource_getsize_proxy-function"></a><span data-ttu-id="873b5-103">IWICBitmapSource \_ GetSize- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="873b5-103">IWICBitmapSource\_GetSize\_Proxy function</span></span>

<span data-ttu-id="873b5-104">Proxy Funktion für die [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) -Methode.</span><span class="sxs-lookup"><span data-stu-id="873b5-104">Proxy function for the [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="873b5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="873b5-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetSize_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ UINT             *puiWidth,
  _Out_ UINT             *puiHeight
);
```



## <a name="parameters"></a><span data-ttu-id="873b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="873b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="873b5-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="873b5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="873b5-108">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="873b5-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="873b5-109">Zeiger auf dieses [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="873b5-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="873b5-110">*puiWidth* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="873b5-110">*puiWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="873b5-111">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="873b5-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="873b5-112">Ein Zeiger, der die Pixel Breite der Bitmap empfängt.</span><span class="sxs-lookup"><span data-stu-id="873b5-112">A pointer that receives the pixel width of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="873b5-113">_puiHeight \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="873b5-113">_puiHeight\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="873b5-114">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="873b5-114">Type: \**UINT\** _</span></span>

<span data-ttu-id="873b5-115">Ein Zeiger, der die Pixelhöhe der Bitmap empfängt.</span><span class="sxs-lookup"><span data-stu-id="873b5-115">A pointer that receives the pixel height of the bitmap</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="873b5-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="873b5-116">Return value</span></span>

<span data-ttu-id="873b5-117">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="873b5-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="873b5-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="873b5-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="873b5-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="873b5-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="873b5-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="873b5-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="873b5-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="873b5-121">Requirements</span></span>



| <span data-ttu-id="873b5-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="873b5-122">Requirement</span></span> | <span data-ttu-id="873b5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="873b5-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="873b5-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="873b5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="873b5-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="873b5-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="873b5-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="873b5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="873b5-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="873b5-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="873b5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="873b5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="873b5-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="873b5-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





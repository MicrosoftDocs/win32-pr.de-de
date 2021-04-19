---
description: Proxy Funktion für die SetResolution-Methode.
ms.assetid: dc8df5bb-c38b-4be3-a4c6-60e7d5e1cd1b
title: IWICBitmapFrameEncode_SetResolution_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9801384e305f2449c6a31b80cb238fc92f7b63b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360608"
---
# <a name="iwicbitmapframeencode_setresolution_proxy-function"></a><span data-ttu-id="aa7fb-103">IWICBitmapFrameEncode \_ SetResolution- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="aa7fb-103">IWICBitmapFrameEncode\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="aa7fb-104">Proxy Funktion für die [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) -Methode.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa7fb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa7fb-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetResolution_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ double                dpiX,
  _In_ double                dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="aa7fb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa7fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa7fb-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa7fb-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa7fb-108">Typ: \**[**iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="aa7fb-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="aa7fb-109">Zeiger auf dieses [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="aa7fb-110">*Dpix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa7fb-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa7fb-111">Typ: **Double**</span><span class="sxs-lookup"><span data-stu-id="aa7fb-111">Type: **double**</span></span>

<span data-ttu-id="aa7fb-112">Der Wert für die horizontale Auflösung.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-112">The horizontal resolution value.</span></span>

</dd> <dt>

<span data-ttu-id="aa7fb-113">*DpiY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa7fb-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa7fb-114">Typ: **Double**</span><span class="sxs-lookup"><span data-stu-id="aa7fb-114">Type: **double**</span></span>

<span data-ttu-id="aa7fb-115">Der Wert für die vertikale Auflösung.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-115">The vertical resolution value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa7fb-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa7fb-116">Return value</span></span>

<span data-ttu-id="aa7fb-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="aa7fb-117">Type: **HRESULT**</span></span>

<span data-ttu-id="aa7fb-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aa7fb-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aa7fb-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa7fb-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa7fb-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="aa7fb-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="aa7fb-121">Requirements</span></span>



| <span data-ttu-id="aa7fb-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa7fb-122">Requirement</span></span> | <span data-ttu-id="aa7fb-123">Wert</span><span class="sxs-lookup"><span data-stu-id="aa7fb-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa7fb-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa7fb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aa7fb-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa7fb-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="aa7fb-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa7fb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="aa7fb-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa7fb-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="aa7fb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="aa7fb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa7fb-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa7fb-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





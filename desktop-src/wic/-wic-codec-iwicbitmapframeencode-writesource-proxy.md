---
description: Proxy Funktion für die "Write tesource"-Methode.
ms.assetid: d95ad80f-7a26-45a7-8103-2673989143b7
title: IWICBitmapFrameEncode_WriteSource_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_WriteSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9eb5ab9db9341d138c72d350304407966a6293d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218703"
---
# <a name="iwicbitmapframeencode_writesource_proxy-function"></a><span data-ttu-id="8d701-103">IWICBitmapFrameEncode- \_ \_ Proxy Funktion für schreibgeschützte Datenquelle</span><span class="sxs-lookup"><span data-stu-id="8d701-103">IWICBitmapFrameEncode\_WriteSource\_Proxy function</span></span>

<span data-ttu-id="8d701-104">Proxy Funktion für die " [**Write tesource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) "-Methode.</span><span class="sxs-lookup"><span data-stu-id="8d701-104">Proxy function for the [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d701-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d701-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_WriteSource_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ WICRect               *prc
);
```



## <a name="parameters"></a><span data-ttu-id="8d701-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d701-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d701-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d701-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d701-108">Typ: \**[**iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="8d701-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="8d701-109">Zeiger auf dieses [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8d701-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="8d701-110">*pibitmapsource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d701-110">*pIBitmapSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d701-111">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="8d701-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="8d701-112">Die zu codierende Bitmap-Quelle.</span><span class="sxs-lookup"><span data-stu-id="8d701-112">The bitmap source to encode.</span></span>

</dd> <dt>

<span data-ttu-id="8d701-113">_prc \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d701-113">_prc\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d701-114">Typ: \**[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="8d701-114">Type: \**[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="8d701-115">Das Größen Rechteck der Bitmapquelle.</span><span class="sxs-lookup"><span data-stu-id="8d701-115">The size rectangle of the bitmap source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d701-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d701-116">Return value</span></span>

<span data-ttu-id="8d701-117">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8d701-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8d701-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8d701-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8d701-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d701-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d701-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d701-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8d701-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8d701-121">Requirements</span></span>



| <span data-ttu-id="8d701-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d701-122">Requirement</span></span> | <span data-ttu-id="8d701-123">Wert</span><span class="sxs-lookup"><span data-stu-id="8d701-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d701-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d701-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8d701-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d701-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8d701-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d701-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8d701-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d701-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8d701-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8d701-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d701-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d701-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





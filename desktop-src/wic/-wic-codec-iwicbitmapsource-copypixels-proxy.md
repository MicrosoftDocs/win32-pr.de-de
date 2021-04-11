---
description: Proxy Funktion für die CopyPixels-Methode.
ms.assetid: 020c11e9-0847-468e-b240-20529f6460cd
title: IWICBitmapSource_CopyPixels_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPixels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5c759bd1731e2f3cbc4da9c40cb590e0f39686de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217667"
---
# <a name="iwicbitmapsource_copypixels_proxy-function"></a><span data-ttu-id="c560f-103">IWICBitmapSource \_ CopyPixels- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="c560f-103">IWICBitmapSource\_CopyPixels\_Proxy function</span></span>

<span data-ttu-id="c560f-104">Proxy Funktion für die [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c560f-104">Proxy function for the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c560f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c560f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPixels_Proxy(
  _In_        IWICBitmapSource *THIS_PTR,
  _In_  const WICRect          *prc,
  _In_        UINT             cbStride,
  _In_        UINT             cbBufferSize,
  _Out_       BYTE             *pbBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="c560f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c560f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c560f-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c560f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c560f-108">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="c560f-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="c560f-109">Zeiger auf dieses [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c560f-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="c560f-110">*Volksrepublik China* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c560f-110">*prc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c560f-111">Typ: \* Konstante *[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="c560f-111">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="c560f-112">Das Rechteck, das kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c560f-112">The rectangle to copy.</span></span> <span data-ttu-id="c560f-113">Ein NULL-Wert gibt die gesamte Bitmap an.</span><span class="sxs-lookup"><span data-stu-id="c560f-113">A NULL value specifies the entire bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="c560f-114">_cbStride \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c560f-114">_cbStride\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c560f-115">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="c560f-115">Type: **UINT**</span></span>

<span data-ttu-id="c560f-116">Der Schritt der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="c560f-116">The stride of the bitmap</span></span>

</dd> <dt>

<span data-ttu-id="c560f-117">*cbBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c560f-117">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c560f-118">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="c560f-118">Type: **UINT**</span></span>

<span data-ttu-id="c560f-119">Die Größe des Puffers.</span><span class="sxs-lookup"><span data-stu-id="c560f-119">The size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c560f-120">*pbBuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c560f-120">*pbBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c560f-121">Typ: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="c560f-121">Type: \**BYTE\** _</span></span>

<span data-ttu-id="c560f-122">Ein Zeiger auf den Puffer.</span><span class="sxs-lookup"><span data-stu-id="c560f-122">A pointer to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c560f-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c560f-123">Return value</span></span>

<span data-ttu-id="c560f-124">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c560f-124">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c560f-125">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c560f-125">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c560f-126">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c560f-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c560f-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c560f-127">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c560f-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c560f-128">Requirements</span></span>



| <span data-ttu-id="c560f-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c560f-129">Requirement</span></span> | <span data-ttu-id="c560f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="c560f-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c560f-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c560f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c560f-132">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c560f-132">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c560f-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c560f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c560f-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c560f-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c560f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c560f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c560f-136"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c560f-136"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





---
description: IWICBitmapDecoder_GetColorContexts_Proxy - Proxyfunktion für die GetColorContexts-Methode.
ms.assetid: 2a6db3bd-d3e1-4e87-a04d-0d1c3ea858fb
title: IWICBitmapDecoder_GetColorContexts_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e550ca4ebd863e58a4bd285c48a2a01aad059b03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086258"
---
# <a name="iwicbitmapdecoder_getcolorcontexts_proxy-function"></a><span data-ttu-id="a6529-103">IWICBitmapDecoder \_ \_ GetColorContexts-Proxyfunktion</span><span class="sxs-lookup"><span data-stu-id="a6529-103">IWICBitmapDecoder\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="a6529-104">Proxyfunktion für die [**GetColorContexts-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)</span><span class="sxs-lookup"><span data-stu-id="a6529-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6529-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6529-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetColorContexts_Proxy(
  _In_    IWICBitmapDecoder *THIS_PTR,
  _In_    UINT              cCount,
  _Inout_ IWICColorContext  **ppIColorContexts,
  _Out_   UINT              *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="a6529-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6529-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6529-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6529-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6529-108">Typ: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="a6529-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="a6529-109">Zeiger auf dieses [**IWICBitmapDecoder-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)</span><span class="sxs-lookup"><span data-stu-id="a6529-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="a6529-110">*cCount* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a6529-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6529-111">Typ: **UINT**</span><span class="sxs-lookup"><span data-stu-id="a6529-111">Type: **UINT**</span></span>

<span data-ttu-id="a6529-112">Die Anzahl der abzurufenden Farbkontexte.</span><span class="sxs-lookup"><span data-stu-id="a6529-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="a6529-113">Dieser Wert muss die Größe von oder kleiner als die größe sein, die *ppIColorContexts zur Verfügung steht.*</span><span class="sxs-lookup"><span data-stu-id="a6529-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="a6529-114">*ppIColorContexts* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a6529-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6529-115">Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="a6529-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="a6529-116">Ein Zeiger, der einen Zeiger auf [**den IWICColorContext empfängt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)</span><span class="sxs-lookup"><span data-stu-id="a6529-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="a6529-117">*pcActualCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a6529-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6529-118">Typ: **UINT \***</span><span class="sxs-lookup"><span data-stu-id="a6529-118">Type: **UINT\***</span></span>

<span data-ttu-id="a6529-119">Ein Zeiger, der die Anzahl der im Bild enthaltenen Farbkontexte empfängt.</span><span class="sxs-lookup"><span data-stu-id="a6529-119">A pointer that receives the number of color contexts contained in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6529-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6529-120">Return value</span></span>

<span data-ttu-id="a6529-121">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a6529-121">Type: **HRESULT**</span></span>

<span data-ttu-id="a6529-122">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="a6529-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a6529-123">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a6529-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6529-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6529-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a6529-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a6529-125">Requirements</span></span>



| <span data-ttu-id="a6529-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6529-126">Requirement</span></span> | <span data-ttu-id="a6529-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a6529-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6529-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6529-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a6529-129">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6529-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a6529-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6529-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a6529-131">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6529-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a6529-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a6529-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6529-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6529-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





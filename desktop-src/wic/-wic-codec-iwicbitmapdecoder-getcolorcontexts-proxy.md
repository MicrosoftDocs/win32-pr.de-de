---
description: Proxy Funktion für die getcolorkontexte-Methode.
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
ms.openlocfilehash: 737ad4b8bbb0014a04129d3a264cecaed4b5fe8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348665"
---
# <a name="iwicbitmapdecoder_getcolorcontexts_proxy-function"></a><span data-ttu-id="673a0-103">IWICBitmapDecoder \_ getcolorkontexte- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="673a0-103">IWICBitmapDecoder\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="673a0-104">Proxy Funktion für die [**getcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) -Methode.</span><span class="sxs-lookup"><span data-stu-id="673a0-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="673a0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="673a0-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetColorContexts_Proxy(
  _In_    IWICBitmapDecoder *THIS_PTR,
  _In_    UINT              cCount,
  _Inout_ IWICColorContext  **ppIColorContexts,
  _Out_   UINT              *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="673a0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="673a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="673a0-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="673a0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="673a0-108">Typ: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="673a0-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="673a0-109">Zeiger auf dieses [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="673a0-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="673a0-110">*ccount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="673a0-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="673a0-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="673a0-111">Type: **UINT**</span></span>

<span data-ttu-id="673a0-112">Die Anzahl der abzurufenden Farb Kontexte.</span><span class="sxs-lookup"><span data-stu-id="673a0-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="673a0-113">Dieser Wert muss die Größe von (oder kleiner als) sein, die für *ppicolorkontexte* verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="673a0-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="673a0-114">*ppicolorkontexte* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="673a0-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="673a0-115">Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="673a0-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="673a0-116">Ein Zeiger, der einen Zeiger auf [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)empfängt.</span><span class="sxs-lookup"><span data-stu-id="673a0-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="673a0-117">*pcActualCount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="673a0-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="673a0-118">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="673a0-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="673a0-119">Ein Zeiger, der die Anzahl der Farb Kontexte im Bild empfängt.</span><span class="sxs-lookup"><span data-stu-id="673a0-119">A pointer that receives the number of color contexts contained in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="673a0-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="673a0-120">Return value</span></span>

<span data-ttu-id="673a0-121">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="673a0-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="673a0-122">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="673a0-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="673a0-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="673a0-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="673a0-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="673a0-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="673a0-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="673a0-125">Requirements</span></span>



| <span data-ttu-id="673a0-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="673a0-126">Requirement</span></span> | <span data-ttu-id="673a0-127">Wert</span><span class="sxs-lookup"><span data-stu-id="673a0-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="673a0-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="673a0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="673a0-129">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="673a0-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="673a0-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="673a0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="673a0-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="673a0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="673a0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="673a0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="673a0-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="673a0-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





---
description: Proxy Funktion für die GetDecoderInfo-Methode.
ms.assetid: 4117492e-d652-4c72-9979-cc4e554a6fd8
title: IWICBitmapDecoder_GetDecoderInfo_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetDecoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ca3e234bc6bbff8899b88c89169a59d9838350b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484771"
---
# <a name="iwicbitmapdecoder_getdecoderinfo_proxy-function"></a><span data-ttu-id="12e87-103">IWICBitmapDecoder \_ GetDecoderInfo- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="12e87-103">IWICBitmapDecoder\_GetDecoderInfo\_Proxy function</span></span>

<span data-ttu-id="12e87-104">Proxy Funktion für die [**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) -Methode.</span><span class="sxs-lookup"><span data-stu-id="12e87-104">Proxy function for the [**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="12e87-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="12e87-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetDecoderInfo_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _Out_ IWICBitmapDecoderInfo **ppIDecoderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="12e87-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="12e87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12e87-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12e87-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12e87-108">Typ: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="12e87-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="12e87-109">Zeiger auf dieses [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="12e87-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="12e87-110">*ppidecoderinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="12e87-110">*ppIDecoderInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12e87-111">Typ: **[ **IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="12e87-111">Type: **[**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***</span></span>

<span data-ttu-id="12e87-112">Ein Zeiger, der einen Zeiger auf ein [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)-Element empfängt.</span><span class="sxs-lookup"><span data-stu-id="12e87-112">A pointer that receives a pointer to an [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12e87-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12e87-113">Return value</span></span>

<span data-ttu-id="12e87-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="12e87-114">Type: **HRESULT**</span></span>

<span data-ttu-id="12e87-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="12e87-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="12e87-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="12e87-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="12e87-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12e87-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="12e87-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="12e87-118">Requirements</span></span>



| <span data-ttu-id="12e87-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12e87-119">Requirement</span></span> | <span data-ttu-id="12e87-120">Wert</span><span class="sxs-lookup"><span data-stu-id="12e87-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12e87-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12e87-121">Minimum supported client</span></span><br/> | <span data-ttu-id="12e87-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12e87-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="12e87-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12e87-123">Minimum supported server</span></span><br/> | <span data-ttu-id="12e87-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12e87-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="12e87-125">DLL</span><span class="sxs-lookup"><span data-stu-id="12e87-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12e87-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12e87-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





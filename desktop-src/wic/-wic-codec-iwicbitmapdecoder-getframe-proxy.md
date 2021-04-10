---
description: Proxy Funktion für die GetFrame-Methode.
ms.assetid: 31612afa-5017-4ddb-bdf8-25555db35da5
title: IWICBitmapDecoder_GetFrame_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 996c0f412aafe6063e25a346552f9c257a51eed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343228"
---
# <a name="iwicbitmapdecoder_getframe_proxy-function"></a><span data-ttu-id="13d9b-103">IWICBitmapDecoder \_ GetFrame- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="13d9b-103">IWICBitmapDecoder\_GetFrame\_Proxy function</span></span>

<span data-ttu-id="13d9b-104">Proxy Funktion für die [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) -Methode.</span><span class="sxs-lookup"><span data-stu-id="13d9b-104">Proxy function for the [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="13d9b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13d9b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetFrame_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _In_  UINT                  index,
  _Out_ IWICBitmapFrameDecode **ppIBitmapFrame
);
```



## <a name="parameters"></a><span data-ttu-id="13d9b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13d9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13d9b-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13d9b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13d9b-108">Typ: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="13d9b-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="13d9b-109">Zeiger auf dieses [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="13d9b-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="13d9b-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13d9b-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13d9b-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="13d9b-111">Type: **UINT**</span></span>

<span data-ttu-id="13d9b-112">Der jeweilige Frame, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="13d9b-112">The particular frame to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="13d9b-113">*ppibitmapframe* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13d9b-113">*ppIBitmapFrame* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13d9b-114">Typ: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***</span><span class="sxs-lookup"><span data-stu-id="13d9b-114">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***</span></span>

<span data-ttu-id="13d9b-115">Ein Zeiger, der einen Zeiger auf [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)empfängt.</span><span class="sxs-lookup"><span data-stu-id="13d9b-115">A pointer that receives a pointer to the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13d9b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13d9b-116">Return value</span></span>

<span data-ttu-id="13d9b-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="13d9b-117">Type: **HRESULT**</span></span>

<span data-ttu-id="13d9b-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="13d9b-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="13d9b-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13d9b-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="13d9b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13d9b-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="13d9b-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="13d9b-121">Requirements</span></span>



| <span data-ttu-id="13d9b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13d9b-122">Requirement</span></span> | <span data-ttu-id="13d9b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="13d9b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13d9b-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13d9b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="13d9b-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13d9b-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="13d9b-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13d9b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="13d9b-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13d9b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="13d9b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="13d9b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13d9b-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13d9b-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





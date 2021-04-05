---
description: Proxy Funktion für die GetFrameCount-Methode.
ms.assetid: 2103af73-60a2-4c1c-8db2-7dfd474440eb
title: IWICBitmapDecoder_GetFrameCount_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrameCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 784f362d711f22f5bfe1728f41309cdd7c22e788
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751240"
---
# <a name="iwicbitmapdecoder_getframecount_proxy-function"></a><span data-ttu-id="5aa93-103">IWICBitmapDecoder \_ GetFrameCount- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="5aa93-103">IWICBitmapDecoder\_GetFrameCount\_Proxy function</span></span>

<span data-ttu-id="5aa93-104">Proxy Funktion für die [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5aa93-104">Proxy function for the [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa93-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5aa93-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetFrameCount_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="5aa93-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5aa93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aa93-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5aa93-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa93-108">Typ: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="5aa93-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="5aa93-109">Zeiger auf dieses [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5aa93-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="5aa93-110">*pcount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5aa93-110">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa93-111">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="5aa93-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="5aa93-112">Ein Zeiger, der die Gesamtzahl der Frames im Bild empfängt.</span><span class="sxs-lookup"><span data-stu-id="5aa93-112">A pointer that receives the total number of frames in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aa93-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5aa93-113">Return value</span></span>

<span data-ttu-id="5aa93-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="5aa93-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="5aa93-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5aa93-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5aa93-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5aa93-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aa93-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5aa93-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa93-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5aa93-118">Requirements</span></span>



| <span data-ttu-id="5aa93-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5aa93-119">Requirement</span></span> | <span data-ttu-id="5aa93-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5aa93-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa93-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5aa93-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5aa93-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5aa93-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5aa93-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5aa93-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5aa93-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5aa93-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5aa93-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5aa93-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5aa93-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5aa93-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





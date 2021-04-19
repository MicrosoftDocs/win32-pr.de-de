---
description: Proxy Funktion für die getchannelcount-Methode.
ms.assetid: f74916d9-d4b5-4b1b-adba-489d46c8d81c
title: IWICPixelFormatInfo_GetChannelCount_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6bf3f0d8aaf6cf95633fa4cce771bd7c7e8db85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369101"
---
# <a name="iwicpixelformatinfo_getchannelcount_proxy-function"></a><span data-ttu-id="de741-103">Iwicpixelformatinfo ( \_ getchannelcount- \_ Proxy Funktion)</span><span class="sxs-lookup"><span data-stu-id="de741-103">IWICPixelFormatInfo\_GetChannelCount\_Proxy function</span></span>

<span data-ttu-id="de741-104">Proxy Funktion für die [**getchannelcount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) -Methode.</span><span class="sxs-lookup"><span data-stu-id="de741-104">Proxy function for the [**GetChannelCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="de741-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="de741-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetChannelCount_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiChannelCount
);
```



## <a name="parameters"></a><span data-ttu-id="de741-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="de741-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de741-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de741-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de741-108">Typ: \**[**iwicpixelformatinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="de741-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="de741-109">Zeiger auf dieses [_ *iwicpixelformatinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="de741-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="de741-110">*puichannelcount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="de741-110">*puiChannelCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de741-111">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="de741-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="de741-112">Ein Zeiger, der die Kanalanzahl empfängt.</span><span class="sxs-lookup"><span data-stu-id="de741-112">Pointer that receives the channel count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de741-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de741-113">Return value</span></span>

<span data-ttu-id="de741-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="de741-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="de741-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="de741-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de741-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="de741-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="de741-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de741-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="de741-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="de741-118">Requirements</span></span>



| <span data-ttu-id="de741-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de741-119">Requirement</span></span> | <span data-ttu-id="de741-120">Wert</span><span class="sxs-lookup"><span data-stu-id="de741-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de741-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de741-121">Minimum supported client</span></span><br/> | <span data-ttu-id="de741-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de741-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="de741-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de741-123">Minimum supported server</span></span><br/> | <span data-ttu-id="de741-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de741-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="de741-125">DLL</span><span class="sxs-lookup"><span data-stu-id="de741-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de741-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de741-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





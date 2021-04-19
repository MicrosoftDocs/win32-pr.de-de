---
description: Proxy Funktion für die CreateFastMetadataEncoderFromFrameDecode-Methode.
ms.assetid: 0edc3387-47e9-401c-9153-76c8c32b52de
title: IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 101bb6aca30f3511a8eb370afa8eb8fd6dda1c21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359519"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromframedecode_proxy-function"></a><span data-ttu-id="33b86-103">IWICImagingFactory \_ CreateFastMetadataEncoderFromFrameDecode \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="33b86-103">IWICImagingFactory\_CreateFastMetadataEncoderFromFrameDecode\_Proxy function</span></span>

<span data-ttu-id="33b86-104">Proxy Funktion für die [**CreateFastMetadataEncoderFromFrameDecode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode) -Methode.</span><span class="sxs-lookup"><span data-stu-id="33b86-104">Proxy function for the [**CreateFastMetadataEncoderFromFrameDecode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="33b86-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33b86-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapFrameDecode   *pIFrameDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a><span data-ttu-id="33b86-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33b86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33b86-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33b86-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33b86-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="33b86-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="33b86-109">_pIFrameDecoder \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33b86-109">_pIFrameDecoder\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33b86-110">Typ: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="33b86-110">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="33b86-111">Das [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Element, aus dem der [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="33b86-111">The [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) to create the [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) from.</span></span>

</dd> <dt>

<span data-ttu-id="33b86-112">*ppif Me* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="33b86-112">*ppIFME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33b86-113">Typ: **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="33b86-113">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span></span>

<span data-ttu-id="33b86-114">Ein Zeiger, der einen Zeiger auf ein neues [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)empfängt.</span><span class="sxs-lookup"><span data-stu-id="33b86-114">A pointer that receives a pointer to a new [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33b86-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33b86-115">Return value</span></span>

<span data-ttu-id="33b86-116">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="33b86-116">Type: **HRESULT**</span></span>

<span data-ttu-id="33b86-117">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="33b86-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33b86-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="33b86-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="33b86-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33b86-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="33b86-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="33b86-120">Requirements</span></span>



| <span data-ttu-id="33b86-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33b86-121">Requirement</span></span> | <span data-ttu-id="33b86-122">Wert</span><span class="sxs-lookup"><span data-stu-id="33b86-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33b86-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33b86-123">Minimum supported client</span></span><br/> | <span data-ttu-id="33b86-124">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33b86-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="33b86-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33b86-125">Minimum supported server</span></span><br/> | <span data-ttu-id="33b86-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33b86-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="33b86-127">DLL</span><span class="sxs-lookup"><span data-stu-id="33b86-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33b86-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33b86-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





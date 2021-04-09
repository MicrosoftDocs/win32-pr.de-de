---
description: Proxy Funktion für die Methode "samatedecoderfromstream".
ms.assetid: 8395d647-c8c9-4715-b15d-a30755ae0a98
title: IWICImagingFactory_CreateDecoderFromStream_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1f6f84c9c29d10243f1b3bcb2cad43967547eeae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760189"
---
# <a name="iwicimagingfactory_createdecoderfromstream_proxy-function"></a><span data-ttu-id="634ae-103">IWICImagingFactory- \_ Funktion "deedecoderfromstream" \_</span><span class="sxs-lookup"><span data-stu-id="634ae-103">IWICImagingFactory\_CreateDecoderFromStream\_Proxy function</span></span>

<span data-ttu-id="634ae-104">Proxy Funktion für die Methode " [**samatedecoderfromstream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) ".</span><span class="sxs-lookup"><span data-stu-id="634ae-104">Proxy function for the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="634ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="634ae-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromStream_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        IStream            *pIStream,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="634ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="634ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="634ae-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="634ae-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="634ae-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="634ae-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="634ae-109">_pIStream \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="634ae-109">_pIStream\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="634ae-110">Typ: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="634ae-110">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="634ae-111">Der Stream, aus dem der Decoder erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="634ae-111">The stream to create the decoder from.</span></span>

</dd> <dt>

<span data-ttu-id="634ae-112">_pguidVendor \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="634ae-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="634ae-113">Geben Sie Folgendes ein: \* Konstante *GUID \** _</span><span class="sxs-lookup"><span data-stu-id="634ae-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="634ae-114">Die Anbieter-GUID für den Decoder.</span><span class="sxs-lookup"><span data-stu-id="634ae-114">The vendor GUID for the decoder .</span></span>

</dd> <dt>

<span data-ttu-id="634ae-115">_metadataOptions \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="634ae-115">_metadataOptions\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="634ae-116">Typ: **[ **wicdecodeoptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="634ae-116">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="634ae-117">Die [**wicdecodeoptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) , die beim Erstellen des Decoders verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="634ae-117">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="634ae-118">*ppidecoder* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="634ae-118">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="634ae-119">Typ: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="634ae-119">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="634ae-120">Ein Zeiger, der einen Zeiger auf einen neuen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)empfängt.</span><span class="sxs-lookup"><span data-stu-id="634ae-120">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="634ae-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="634ae-121">Return value</span></span>

<span data-ttu-id="634ae-122">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="634ae-122">Type: **HRESULT**</span></span>

<span data-ttu-id="634ae-123">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="634ae-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="634ae-124">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="634ae-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="634ae-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="634ae-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="634ae-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="634ae-126">Requirements</span></span>



| <span data-ttu-id="634ae-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="634ae-127">Requirement</span></span> | <span data-ttu-id="634ae-128">Wert</span><span class="sxs-lookup"><span data-stu-id="634ae-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="634ae-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="634ae-129">Minimum supported client</span></span><br/> | <span data-ttu-id="634ae-130">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="634ae-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="634ae-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="634ae-131">Minimum supported server</span></span><br/> | <span data-ttu-id="634ae-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="634ae-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="634ae-133">DLL</span><span class="sxs-lookup"><span data-stu-id="634ae-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="634ae-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="634ae-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 


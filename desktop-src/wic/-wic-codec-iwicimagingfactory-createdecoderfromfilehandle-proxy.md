---
description: Proxy Funktion für die Methode "fiatedecoderfromfilehandle".
ms.assetid: bc7f8a07-6d82-4d95-88ef-979d571758f4
title: IWICImagingFactory_CreateDecoderFromFileHandle_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFileHandle_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 15c515bb17641e2e7b70b79552fe3bacf1f1c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959944"
---
# <a name="iwicimagingfactory_createdecoderfromfilehandle_proxy-function"></a><span data-ttu-id="2ecfe-103">IWICImagingFactory- \_ Funktion "inatedecoderfromfilehandle" \_</span><span class="sxs-lookup"><span data-stu-id="2ecfe-103">IWICImagingFactory\_CreateDecoderFromFileHandle\_Proxy function</span></span>

<span data-ttu-id="2ecfe-104">Proxy Funktion für die Methode " [**fiatedecoderfromfilehandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) ".</span><span class="sxs-lookup"><span data-stu-id="2ecfe-104">Proxy function for the [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ecfe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ecfe-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFileHandle_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        ULONG_PTR          hFile,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="2ecfe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ecfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ecfe-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ecfe-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecfe-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="2ecfe-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="2ecfe-109">_hFile \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ecfe-109">_hFile\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecfe-110">Typ: **ulong \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="2ecfe-110">Type: **ULONG\_PTR**</span></span>

<span data-ttu-id="2ecfe-111">Das Datei Handle, aus dem der Decoder erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ecfe-111">The file handle to create the decoder from.</span></span>

</dd> <dt>

<span data-ttu-id="2ecfe-112">*pguidVendor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ecfe-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecfe-113">Geben Sie Folgendes ein: \* Konstante *GUID \** _</span><span class="sxs-lookup"><span data-stu-id="2ecfe-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="2ecfe-114">Die Anbieter-GUID für den Decoder.</span><span class="sxs-lookup"><span data-stu-id="2ecfe-114">The vendor GUID for the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="2ecfe-115">_metadataOptions \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ecfe-115">_metadataOptions\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecfe-116">Typ: **[ **wicdecodeoptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="2ecfe-116">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="2ecfe-117">Die [**wicdecodeoptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) , die beim Erstellen des Decoders verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2ecfe-117">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="2ecfe-118">*ppidecoder* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2ecfe-118">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecfe-119">Typ: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="2ecfe-119">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="2ecfe-120">Ein Zeiger, der einen Zeiger auf einen neuen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)empfängt.</span><span class="sxs-lookup"><span data-stu-id="2ecfe-120">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ecfe-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ecfe-121">Return value</span></span>

<span data-ttu-id="2ecfe-122">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2ecfe-122">Type: **HRESULT**</span></span>

<span data-ttu-id="2ecfe-123">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2ecfe-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2ecfe-124">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2ecfe-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ecfe-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ecfe-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2ecfe-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2ecfe-126">Requirements</span></span>



| <span data-ttu-id="2ecfe-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ecfe-127">Requirement</span></span> | <span data-ttu-id="2ecfe-128">Wert</span><span class="sxs-lookup"><span data-stu-id="2ecfe-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ecfe-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ecfe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2ecfe-130">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ecfe-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2ecfe-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ecfe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2ecfe-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ecfe-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2ecfe-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2ecfe-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ecfe-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ecfe-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





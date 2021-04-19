---
description: Proxy Funktion für die Methode "samatedecoderfromfilename".
ms.assetid: 12c60899-0fe0-47d0-9026-48c74df328ef
title: IWICImagingFactory_CreateDecoderFromFilename_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFilename_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3497d71475198d035a496909e65c47df6c5f8b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359584"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a><span data-ttu-id="8b40f-103">IWICImagingFactory | \_ atedecoderfromfilename- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="8b40f-103">IWICImagingFactory\_CreateDecoderFromFilename\_Proxy function</span></span>

<span data-ttu-id="8b40f-104">Proxy Funktion für die Methode " [**samatedecoderfromfilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) ".</span><span class="sxs-lookup"><span data-stu-id="8b40f-104">Proxy function for the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b40f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b40f-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFilename_Proxy(
  _In_        IWICImagingFactory  *pFactory,
  _In_        LPCWSTR             wzFilename,
  _In_  const GUID                *pguidVendor,
  _In_        DWORD               dwDesiredAccess,
  _In_        WICDecodeOptions    metadataOptions,
  _Out_       IWICBitmapDecoder   **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="8b40f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b40f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b40f-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b40f-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b40f-108">Typ: \**IWICImagingFactory \** _</span><span class="sxs-lookup"><span data-stu-id="8b40f-108">Type: \**IWICImagingFactory \** _</span></span>

</dd> <dt>

<span data-ttu-id="8b40f-109">_wzFilename \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b40f-109">_wzFilename\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b40f-110">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="8b40f-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="8b40f-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen eines zu erstellenden oder zu öffnenden Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="8b40f-111">A pointer to a null-terminated string that specifies the name of an object to create or open.</span></span>

</dd> <dt>

<span data-ttu-id="8b40f-112">*pguidVendor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b40f-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b40f-113">Geben Sie Folgendes ein: \* Konstante *GUID \** _</span><span class="sxs-lookup"><span data-stu-id="8b40f-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="8b40f-114">Die Anbieter-GUID für den Decoder.</span><span class="sxs-lookup"><span data-stu-id="8b40f-114">The vendor GUID for the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="8b40f-115">_dwDesiredAccess \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b40f-115">_dwDesiredAccess\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b40f-116">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8b40f-116">Type: **DWORD**</span></span>

<span data-ttu-id="8b40f-117">Der Zugriff auf das-Objekt, das gelesen oder geschrieben werden kann, oder beides.</span><span class="sxs-lookup"><span data-stu-id="8b40f-117">The access to the object, which can be read, write, or both.</span></span>

<span data-ttu-id="8b40f-118">Weitere Informationen finden Sie unter [Datei Sicherheit und Zugriffsrechte \[ Dateien \] ](../fileio/file-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="8b40f-118">For more information, see [File Security and Access Rights \[Files\]](../fileio/file-security-and-access-rights.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b40f-119">*metadataOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b40f-119">*metadataOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b40f-120">Typ: **[ **wicdecodeoptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="8b40f-120">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="8b40f-121">Die [**wicdecodeoptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) , die beim Erstellen des Decoders verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8b40f-121">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="8b40f-122">*ppidecoder* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8b40f-122">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b40f-123">Typ: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="8b40f-123">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="8b40f-124">Ein Zeiger, der einen Zeiger auf den neuen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)empfängt.</span><span class="sxs-lookup"><span data-stu-id="8b40f-124">A pointer that receives a pointer to the new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b40f-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b40f-125">Return value</span></span>

<span data-ttu-id="8b40f-126">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8b40f-126">Type: **HRESULT**</span></span>

<span data-ttu-id="8b40f-127">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8b40f-127">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8b40f-128">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8b40f-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b40f-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b40f-129">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8b40f-130">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8b40f-130">Requirements</span></span>



| <span data-ttu-id="8b40f-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b40f-131">Requirement</span></span> | <span data-ttu-id="8b40f-132">Wert</span><span class="sxs-lookup"><span data-stu-id="8b40f-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b40f-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b40f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8b40f-134">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b40f-134">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8b40f-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b40f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8b40f-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b40f-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8b40f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8b40f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b40f-138"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b40f-138"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 


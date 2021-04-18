---
description: Proxy Funktion für die CreateFastMetadataEncoderFromDecoder-Methode.
ms.assetid: eae7ed9c-9205-4e41-91b2-461fd1f5d093
title: IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cdeb682139feb03c19cd66e999b6e3b8b7b366d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347615"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromdecoder_proxy-function"></a><span data-ttu-id="67a3b-103">IWICImagingFactory \_ CreateFastMetadataEncoderFromDecoder \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="67a3b-103">IWICImagingFactory\_CreateFastMetadataEncoderFromDecoder\_Proxy function</span></span>

<span data-ttu-id="67a3b-104">Proxy Funktion für die [**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder) -Methode.</span><span class="sxs-lookup"><span data-stu-id="67a3b-104">Proxy function for the [**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="67a3b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="67a3b-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapDecoder       *pIDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a><span data-ttu-id="67a3b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="67a3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67a3b-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67a3b-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67a3b-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="67a3b-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="67a3b-109">_pIDecoder \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67a3b-109">_pIDecoder\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67a3b-110">Typ: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="67a3b-110">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="67a3b-111">Der Decoder, aus dem [_ *IWICFastMetadataEncoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="67a3b-111">The decoder to create the [_ *IWICFastMetadataEncoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) from.</span></span>

</dd> <dt>

<span data-ttu-id="67a3b-112">*ppif Me* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="67a3b-112">*ppIFME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67a3b-113">Typ: **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="67a3b-113">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span></span>

<span data-ttu-id="67a3b-114">Ein Zeiger, der einen Zeiger auf den neuen [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)empfängt.</span><span class="sxs-lookup"><span data-stu-id="67a3b-114">A pointer that receives a pointer to the new [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67a3b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67a3b-115">Return value</span></span>

<span data-ttu-id="67a3b-116">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="67a3b-116">Type: **HRESULT**</span></span>

<span data-ttu-id="67a3b-117">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="67a3b-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="67a3b-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="67a3b-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="67a3b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67a3b-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="67a3b-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="67a3b-120">Requirements</span></span>



| <span data-ttu-id="67a3b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67a3b-121">Requirement</span></span> | <span data-ttu-id="67a3b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="67a3b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67a3b-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67a3b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="67a3b-124">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67a3b-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="67a3b-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67a3b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="67a3b-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67a3b-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="67a3b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="67a3b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67a3b-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67a3b-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





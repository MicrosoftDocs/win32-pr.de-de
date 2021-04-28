---
description: 'IWICBitmapDecoder_GetMetadataQueryReader_Proxy-Funktion: Proxyfunktion für die GetMetadataQueryReader-Methode.'
ms.assetid: cc32bdf1-d807-46ac-87b7-77bf2d498e72
title: IWICBitmapDecoder_GetMetadataQueryReader_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ebda8edb5c2007b1dfb39ca9f406855da05c456a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100648"
---
# <a name="iwicbitmapdecoder_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="1f2f0-103">Proxyfunktion "IWICBitmapDecoder \_ GetMetadataQueryReader" \_</span><span class="sxs-lookup"><span data-stu-id="1f2f0-103">IWICBitmapDecoder\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="1f2f0-104">Proxyfunktion für die [**GetMetadataQueryReader-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)</span><span class="sxs-lookup"><span data-stu-id="1f2f0-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f2f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f2f0-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapDecoder       *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="1f2f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f2f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f2f0-107">*DIES \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f2f0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f2f0-108">Typ: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="1f2f0-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="1f2f0-109">Zeiger auf dieses [**IWICBitmapDecoder-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)</span><span class="sxs-lookup"><span data-stu-id="1f2f0-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="1f2f0-110">*ppIMetadataQueryReader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1f2f0-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f2f0-111">Typ: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="1f2f0-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="1f2f0-112">Ein Zeiger, der einen Zeiger auf die Metadaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="1f2f0-112">A pointer that receives a pointer to the metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f2f0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f2f0-113">Return value</span></span>

<span data-ttu-id="1f2f0-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1f2f0-114">Type: **HRESULT**</span></span>

<span data-ttu-id="1f2f0-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1f2f0-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1f2f0-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1f2f0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f2f0-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f2f0-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1f2f0-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1f2f0-118">Requirements</span></span>



| <span data-ttu-id="1f2f0-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f2f0-119">Requirement</span></span> | <span data-ttu-id="1f2f0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1f2f0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f2f0-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f2f0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1f2f0-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f2f0-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1f2f0-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f2f0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1f2f0-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f2f0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1f2f0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1f2f0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f2f0-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f2f0-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





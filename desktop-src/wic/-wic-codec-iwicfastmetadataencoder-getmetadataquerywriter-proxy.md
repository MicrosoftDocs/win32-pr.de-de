---
description: 'IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy-Funktion: Proxyfunktion für die GetMetadataQueryWriter-Methode.'
ms.assetid: 64d2c6d8-f1dd-4397-8487-4d23c69aea82
title: IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b06bc6fbcdc65c9d1163ccb4a862d6046b455c9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097168"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="a6da7-103">IWICFastMetadataEncoder \_ GetMetadataQueryWriter-Proxyfunktion \_</span><span class="sxs-lookup"><span data-stu-id="a6da7-103">IWICFastMetadataEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="a6da7-104">Proxyfunktion für die [**GetMetadataQueryWriter-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter)</span><span class="sxs-lookup"><span data-stu-id="a6da7-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6da7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6da7-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="a6da7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6da7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6da7-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6da7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6da7-108">Typ: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="a6da7-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="a6da7-109">Zeiger auf dieses [**IWICBitmapFrameDecode-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)</span><span class="sxs-lookup"><span data-stu-id="a6da7-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="a6da7-110">*ppIMetadataQueryWriter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a6da7-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6da7-111">Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="a6da7-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="a6da7-112">Ein Zeiger, der einen Zeiger auf den Metadatenabfragewriter des Encoders empfängt.</span><span class="sxs-lookup"><span data-stu-id="a6da7-112">A pointer that receives a pointer to the encoder's metadata query writer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6da7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6da7-113">Return value</span></span>

<span data-ttu-id="a6da7-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a6da7-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a6da7-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="a6da7-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a6da7-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a6da7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6da7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6da7-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a6da7-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a6da7-118">Requirements</span></span>



| <span data-ttu-id="a6da7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6da7-119">Requirement</span></span> | <span data-ttu-id="a6da7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a6da7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6da7-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6da7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a6da7-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6da7-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a6da7-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6da7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a6da7-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6da7-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a6da7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a6da7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6da7-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6da7-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





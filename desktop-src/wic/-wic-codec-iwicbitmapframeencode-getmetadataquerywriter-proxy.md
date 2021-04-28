---
description: 'IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy-Funktion: Proxyfunktion für die GetMetadataQueryWriter-Methode.'
ms.assetid: b2c61dee-b72b-408c-8cb9-de2587587f1f
title: IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 89eb7342277d335c78ee2bc6807f2fc4d170bb9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113608"
---
# <a name="iwicbitmapframeencode_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="40452-103">IWICBitmapFrameEncode-Funktion \_ "GetMetadataQueryWriter \_ Proxy"</span><span class="sxs-lookup"><span data-stu-id="40452-103">IWICBitmapFrameEncode\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="40452-104">Proxyfunktion für die [**GetMetadataQueryWriter-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter)</span><span class="sxs-lookup"><span data-stu-id="40452-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="40452-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="40452-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameEncode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="40452-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="40452-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40452-107">*DIES \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40452-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40452-108">Typ: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="40452-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="40452-109">Zeiger auf dieses [**IWICBitmapFrameEncode-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="40452-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="40452-110">*ppIMetadataQueryWriter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="40452-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40452-111">Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="40452-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="40452-112">Ein Zeiger, der einen Metadatenabfrage-Writer für den Frame empfängt.</span><span class="sxs-lookup"><span data-stu-id="40452-112">A pointer that receives a metadata query writer for the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40452-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40452-113">Return value</span></span>

<span data-ttu-id="40452-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="40452-114">Type: **HRESULT**</span></span>

<span data-ttu-id="40452-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="40452-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="40452-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="40452-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="40452-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40452-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="40452-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="40452-118">Requirements</span></span>



| <span data-ttu-id="40452-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40452-119">Requirement</span></span> | <span data-ttu-id="40452-120">Wert</span><span class="sxs-lookup"><span data-stu-id="40452-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40452-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40452-121">Minimum supported client</span></span><br/> | <span data-ttu-id="40452-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40452-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="40452-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40452-123">Minimum supported server</span></span><br/> | <span data-ttu-id="40452-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40452-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="40452-125">DLL</span><span class="sxs-lookup"><span data-stu-id="40452-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40452-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="40452-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





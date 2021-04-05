---
description: Proxy Funktion für die GetMetadataQueryWriter-Methode.
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
ms.openlocfilehash: b6668ffc4261310bfa76424afcae92e14c4ed921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751224"
---
# <a name="iwicbitmapframeencode_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="28f91-103">IWICBitmapFrameEncode \_ GetMetadataQueryWriter \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="28f91-103">IWICBitmapFrameEncode\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="28f91-104">Proxy Funktion für die [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) -Methode.</span><span class="sxs-lookup"><span data-stu-id="28f91-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="28f91-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28f91-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameEncode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="28f91-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="28f91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28f91-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="28f91-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28f91-108">Typ: \**[**iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="28f91-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="28f91-109">Zeiger auf dieses [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="28f91-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="28f91-110">*ppIMetadataQueryWriter* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="28f91-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28f91-111">Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="28f91-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="28f91-112">Ein Zeiger, der einen Metadatenabfragewriter für den Frame empfängt.</span><span class="sxs-lookup"><span data-stu-id="28f91-112">A pointer that receives a metadata query writer for the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28f91-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28f91-113">Return value</span></span>

<span data-ttu-id="28f91-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="28f91-114">Type: **HRESULT**</span></span>

<span data-ttu-id="28f91-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="28f91-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="28f91-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="28f91-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="28f91-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28f91-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="28f91-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="28f91-118">Requirements</span></span>



| <span data-ttu-id="28f91-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28f91-119">Requirement</span></span> | <span data-ttu-id="28f91-120">Wert</span><span class="sxs-lookup"><span data-stu-id="28f91-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28f91-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28f91-121">Minimum supported client</span></span><br/> | <span data-ttu-id="28f91-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28f91-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="28f91-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28f91-123">Minimum supported server</span></span><br/> | <span data-ttu-id="28f91-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28f91-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="28f91-125">DLL</span><span class="sxs-lookup"><span data-stu-id="28f91-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28f91-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28f91-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





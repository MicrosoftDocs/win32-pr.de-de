---
description: 'IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy-Funktion: Proxyfunktion für die GetMetadataQueryReader-Methode.'
ms.assetid: 2a3e0a59-3524-4da4-993a-607a3727faba
title: IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c6c00cc4463bd8540e5baeb41a10577e9f67e85c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091138"
---
# <a name="iwicbitmapframedecode_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="117f5-103">Proxyfunktion \_ "GetMetadataQueryReader" für IWICBitmapFrameDecode \_</span><span class="sxs-lookup"><span data-stu-id="117f5-103">IWICBitmapFrameDecode\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="117f5-104">Proxyfunktion für die [**GetMetadataQueryReader-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)</span><span class="sxs-lookup"><span data-stu-id="117f5-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="117f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="117f5-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="117f5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="117f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="117f5-107">*DIES \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="117f5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="117f5-108">Typ: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="117f5-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="117f5-109">Zeiger auf dieses [**IWICBitmapFrameDecode-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)</span><span class="sxs-lookup"><span data-stu-id="117f5-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="117f5-110">*ppIMetadataQueryReader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="117f5-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="117f5-111">Typ: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="117f5-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="117f5-112">Ein Zeiger, der einen Zeiger auf einen [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)empfängt.</span><span class="sxs-lookup"><span data-stu-id="117f5-112">A pointer that receives a pointer to an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="117f5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="117f5-113">Return value</span></span>

<span data-ttu-id="117f5-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="117f5-114">Type: **HRESULT**</span></span>

<span data-ttu-id="117f5-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="117f5-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="117f5-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="117f5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="117f5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="117f5-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="117f5-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="117f5-118">Requirements</span></span>



| <span data-ttu-id="117f5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="117f5-119">Requirement</span></span> | <span data-ttu-id="117f5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="117f5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="117f5-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="117f5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="117f5-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="117f5-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="117f5-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="117f5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="117f5-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="117f5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="117f5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="117f5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="117f5-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="117f5-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





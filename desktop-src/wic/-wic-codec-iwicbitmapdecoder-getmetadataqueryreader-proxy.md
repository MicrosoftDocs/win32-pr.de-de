---
description: Proxy Funktion für die GetMetadataQueryReader-Methode.
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
ms.openlocfilehash: 72b47652c76934fdf3ea518925990d6d4d1d3eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343219"
---
# <a name="iwicbitmapdecoder_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="f9d52-103">IWICBitmapDecoder \_ GetMetadataQueryReader \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="f9d52-103">IWICBitmapDecoder\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="f9d52-104">Proxy Funktion für die [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f9d52-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9d52-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9d52-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapDecoder       *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="f9d52-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9d52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9d52-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9d52-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d52-108">Typ: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="f9d52-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="f9d52-109">Zeiger auf dieses [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f9d52-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="f9d52-110">*ppIMetadataQueryReader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f9d52-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d52-111">Typ: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="f9d52-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="f9d52-112">Ein Zeiger, der einen Zeiger auf die Metadaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="f9d52-112">A pointer that receives a pointer to the metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9d52-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9d52-113">Return value</span></span>

<span data-ttu-id="f9d52-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f9d52-114">Type: **HRESULT**</span></span>

<span data-ttu-id="f9d52-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f9d52-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f9d52-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f9d52-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9d52-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9d52-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f9d52-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f9d52-118">Requirements</span></span>



| <span data-ttu-id="f9d52-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9d52-119">Requirement</span></span> | <span data-ttu-id="f9d52-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f9d52-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9d52-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9d52-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f9d52-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9d52-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f9d52-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9d52-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f9d52-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9d52-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f9d52-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f9d52-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9d52-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9d52-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





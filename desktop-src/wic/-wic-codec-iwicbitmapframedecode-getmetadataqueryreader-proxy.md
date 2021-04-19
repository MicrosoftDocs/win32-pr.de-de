---
description: Proxy Funktion für die GetMetadataQueryReader-Methode.
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
ms.openlocfilehash: e549fdfbacb5bd508a442c70c203595b8819750f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348983"
---
# <a name="iwicbitmapframedecode_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="0fa52-103">IWICBitmapFrameDecode \_ GetMetadataQueryReader \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="0fa52-103">IWICBitmapFrameDecode\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="0fa52-104">Proxy Funktion für die [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0fa52-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fa52-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fa52-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="0fa52-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fa52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fa52-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0fa52-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fa52-108">Typ: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="0fa52-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="0fa52-109">Zeiger auf dieses [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="0fa52-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="0fa52-110">*ppIMetadataQueryReader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0fa52-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fa52-111">Typ: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="0fa52-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="0fa52-112">Ein Zeiger, der einen Zeiger auf eine [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)empfängt.</span><span class="sxs-lookup"><span data-stu-id="0fa52-112">A pointer that receives a pointer to an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fa52-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fa52-113">Return value</span></span>

<span data-ttu-id="0fa52-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0fa52-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0fa52-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="0fa52-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0fa52-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0fa52-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fa52-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fa52-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0fa52-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0fa52-118">Requirements</span></span>



| <span data-ttu-id="0fa52-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fa52-119">Requirement</span></span> | <span data-ttu-id="0fa52-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0fa52-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa52-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fa52-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0fa52-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fa52-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0fa52-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fa52-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0fa52-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fa52-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0fa52-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0fa52-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fa52-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fa52-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





---
description: 'IWICBitmapEncoder_GetMetadataQueryWriter_Proxy-Funktion: Proxyfunktion für die GetMetadataQueryWriter-Methode.'
ms.assetid: 3186d473-f8a7-405a-8429-3f50104bee4a
title: IWICBitmapEncoder_GetMetadataQueryWriter_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 798a9b5bafb2f5011e42e603b8b2c98b0ba79b37
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091168"
---
# <a name="iwicbitmapencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="d5e68-103">IWICBitmapEncoder \_ GetMetadataQueryWriter-Proxyfunktion \_</span><span class="sxs-lookup"><span data-stu-id="d5e68-103">IWICBitmapEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="d5e68-104">Proxyfunktion für die [**GetMetadataQueryWriter-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)</span><span class="sxs-lookup"><span data-stu-id="d5e68-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5e68-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5e68-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapEncoder       *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="d5e68-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5e68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5e68-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5e68-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5e68-108">Typ: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="d5e68-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="d5e68-109">Zeiger auf dieses [**IWICBitmapEncoder-Objekt.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)</span><span class="sxs-lookup"><span data-stu-id="d5e68-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="d5e68-110">*ppIMetadataQueryWriter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d5e68-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5e68-111">Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="d5e68-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="d5e68-112">Ein Zeiger, der einen Zeiger auf einen [**IWICMetadataQueryWriter empfängt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)</span><span class="sxs-lookup"><span data-stu-id="d5e68-112">A pointer that receives a pointer to an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5e68-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5e68-113">Return value</span></span>

<span data-ttu-id="d5e68-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d5e68-114">Type: **HRESULT**</span></span>

<span data-ttu-id="d5e68-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="d5e68-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d5e68-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d5e68-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5e68-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5e68-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d5e68-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d5e68-118">Requirements</span></span>



| <span data-ttu-id="d5e68-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5e68-119">Requirement</span></span> | <span data-ttu-id="d5e68-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d5e68-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e68-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5e68-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d5e68-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5e68-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d5e68-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5e68-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d5e68-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5e68-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d5e68-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d5e68-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5e68-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5e68-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





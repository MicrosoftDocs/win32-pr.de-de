---
description: Proxy Funktion für die GetMetadataQueryWriter-Methode.
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
ms.openlocfilehash: b536e7c4c0553df5dae0f8e11db33c6d709e8c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356740"
---
# <a name="iwicbitmapencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="fcb4d-103">Iwicbitmapcoder \_ GetMetadataQueryWriter \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="fcb4d-103">IWICBitmapEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="fcb4d-104">Proxy Funktion für die [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) -Methode.</span><span class="sxs-lookup"><span data-stu-id="fcb4d-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb4d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcb4d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapEncoder       *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="fcb4d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcb4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcb4d-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcb4d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcb4d-108">Typ: \**[**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="fcb4d-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="fcb4d-109">Zeiger auf dieses [_ *iwicbitmapcoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="fcb4d-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="fcb4d-110">*ppIMetadataQueryWriter* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fcb4d-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcb4d-111">Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="fcb4d-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="fcb4d-112">Ein Zeiger, der einen Zeiger auf eine [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)empfängt.</span><span class="sxs-lookup"><span data-stu-id="fcb4d-112">A pointer that receives a pointer to an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcb4d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fcb4d-113">Return value</span></span>

<span data-ttu-id="fcb4d-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fcb4d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="fcb4d-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fcb4d-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fcb4d-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fcb4d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcb4d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcb4d-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="fcb4d-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fcb4d-118">Requirements</span></span>



| <span data-ttu-id="fcb4d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fcb4d-119">Requirement</span></span> | <span data-ttu-id="fcb4d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="fcb4d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcb4d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fcb4d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fcb4d-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fcb4d-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="fcb4d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fcb4d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fcb4d-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fcb4d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="fcb4d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fcb4d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcb4d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcb4d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





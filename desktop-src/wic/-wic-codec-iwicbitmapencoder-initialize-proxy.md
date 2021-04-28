---
description: IWICBitmapEncoder_Initialize_Proxy- Proxyfunktion für die Initialize-Methode.
ms.assetid: 0db79eb4-dcb2-491a-9bea-a0dec418f80f
title: IWICBitmapEncoder_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d346d1379ae92f19a530c65daff07cb98b2e0e50
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100618"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a><span data-ttu-id="c55a9-103">IWICBitmapEncoder Initialize \_ \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="c55a9-103">IWICBitmapEncoder\_Initialize\_Proxy function</span></span>

<span data-ttu-id="c55a9-104">Proxyfunktion für die [**Initialize-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)</span><span class="sxs-lookup"><span data-stu-id="c55a9-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c55a9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c55a9-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a><span data-ttu-id="c55a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c55a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c55a9-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c55a9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c55a9-108">Typ: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="c55a9-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="c55a9-109">Zeiger auf dieses [**IWICBitmapEncoder-Objekt.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)</span><span class="sxs-lookup"><span data-stu-id="c55a9-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="c55a9-110">*pIStream* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c55a9-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c55a9-111">Typ: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***</span><span class="sxs-lookup"><span data-stu-id="c55a9-111">Type: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***</span></span>

<span data-ttu-id="c55a9-112">Der Ausgabestream.</span><span class="sxs-lookup"><span data-stu-id="c55a9-112">The output stream.</span></span>

</dd> <dt>

<span data-ttu-id="c55a9-113">*cacheOption* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c55a9-113">*cacheOption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c55a9-114">Typ: **[ **WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span><span class="sxs-lookup"><span data-stu-id="c55a9-114">Type: **[**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span></span>

<span data-ttu-id="c55a9-115">Die bei der Initialisierung verwendete [**WICBitmapEncoderCacheOption.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)</span><span class="sxs-lookup"><span data-stu-id="c55a9-115">The [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) used on initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c55a9-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c55a9-116">Return value</span></span>

<span data-ttu-id="c55a9-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c55a9-117">Type: **HRESULT**</span></span>

<span data-ttu-id="c55a9-118">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="c55a9-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c55a9-119">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c55a9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c55a9-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c55a9-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c55a9-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c55a9-121">Requirements</span></span>



| <span data-ttu-id="c55a9-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c55a9-122">Requirement</span></span> | <span data-ttu-id="c55a9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c55a9-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c55a9-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c55a9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c55a9-125">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c55a9-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c55a9-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c55a9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c55a9-127">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c55a9-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c55a9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c55a9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c55a9-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c55a9-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 


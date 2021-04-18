---
description: Proxy Funktion für die Initialize-Methode.
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
ms.openlocfilehash: c1a2e684059b75e41c1d89e2d3dd5379cc208b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352470"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a><span data-ttu-id="7d1c7-103">Iwicbitmapcoder- \_ \_ Proxy Funktion initialisieren</span><span class="sxs-lookup"><span data-stu-id="7d1c7-103">IWICBitmapEncoder\_Initialize\_Proxy function</span></span>

<span data-ttu-id="7d1c7-104">Proxy Funktion für die [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d1c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d1c7-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a><span data-ttu-id="7d1c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d1c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d1c7-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d1c7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d1c7-108">Typ: \**[**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="7d1c7-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="7d1c7-109">Zeiger auf dieses [_ *iwicbitmapcoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="7d1c7-110">*pIStream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d1c7-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d1c7-111">Typ: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="7d1c7-111">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="7d1c7-112">Der Ausgabestream.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-112">The output stream.</span></span>

</dd> <dt>

<span data-ttu-id="7d1c7-113">_cacheOption \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d1c7-113">_cacheOption\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d1c7-114">Typ: **[ **wicbitmapcodercacheoption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span><span class="sxs-lookup"><span data-stu-id="7d1c7-114">Type: **[**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span></span>

<span data-ttu-id="7d1c7-115">Die bei der Initialisierung verwendete [**wicbitmapcodercacheoption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) .</span><span class="sxs-lookup"><span data-stu-id="7d1c7-115">The [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) used on initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d1c7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d1c7-116">Return value</span></span>

<span data-ttu-id="7d1c7-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7d1c7-117">Type: **HRESULT**</span></span>

<span data-ttu-id="7d1c7-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7d1c7-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d1c7-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d1c7-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7d1c7-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7d1c7-121">Requirements</span></span>



| <span data-ttu-id="7d1c7-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d1c7-122">Requirement</span></span> | <span data-ttu-id="7d1c7-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7d1c7-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d1c7-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d1c7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7d1c7-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d1c7-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7d1c7-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d1c7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7d1c7-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d1c7-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7d1c7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7d1c7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d1c7-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d1c7-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 


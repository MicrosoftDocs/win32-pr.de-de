---
description: Proxy Funktion für die Initialize-Methode.
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: IWICBitmapFlipRotator_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFlipRotator_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 82a1aa5648edd47d0b635a407adc001c25183b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343664"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a><span data-ttu-id="df8ac-103">IWICBitmapFlipRotator \_ Initialize \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="df8ac-103">IWICBitmapFlipRotator\_Initialize\_Proxy function</span></span>

<span data-ttu-id="df8ac-104">Proxy Funktion für die [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) -Methode.</span><span class="sxs-lookup"><span data-stu-id="df8ac-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="df8ac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df8ac-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a><span data-ttu-id="df8ac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="df8ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df8ac-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df8ac-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8ac-108">Typ: \**[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) \** _</span><span class="sxs-lookup"><span data-stu-id="df8ac-108">Type: \**[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\** _</span></span>

<span data-ttu-id="df8ac-109">Zeiger auf dieses [_ *IWICBitmapFlipRotator* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="df8ac-109">Pointer to this [_ *IWICBitmapFlipRotator*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) object.</span></span>

</dd> <dt>

<span data-ttu-id="df8ac-110">*pisource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df8ac-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8ac-111">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="df8ac-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="df8ac-112">Die Eingabe Bitmap-Quelle.</span><span class="sxs-lookup"><span data-stu-id="df8ac-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="df8ac-113">_options \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df8ac-113">_options\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8ac-114">Typ: **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span><span class="sxs-lookup"><span data-stu-id="df8ac-114">Type: **[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span></span>

<span data-ttu-id="df8ac-115">Die [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) zum Kippen oder Drehen des Bilds.</span><span class="sxs-lookup"><span data-stu-id="df8ac-115">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) to flip or rotate the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df8ac-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df8ac-116">Return value</span></span>

<span data-ttu-id="df8ac-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="df8ac-117">Type: **HRESULT**</span></span>

<span data-ttu-id="df8ac-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="df8ac-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="df8ac-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="df8ac-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="df8ac-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df8ac-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="df8ac-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="df8ac-121">Requirements</span></span>



| <span data-ttu-id="df8ac-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df8ac-122">Requirement</span></span> | <span data-ttu-id="df8ac-123">Wert</span><span class="sxs-lookup"><span data-stu-id="df8ac-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df8ac-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df8ac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="df8ac-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df8ac-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="df8ac-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df8ac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="df8ac-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df8ac-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="df8ac-128">DLL</span><span class="sxs-lookup"><span data-stu-id="df8ac-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df8ac-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df8ac-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





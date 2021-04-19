---
description: Proxy Funktion für die Initialize-Methode.
ms.assetid: 47a717d2-9aac-4230-bdb3-093212eb5448
title: IWICBitmapScaler_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapScaler_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cc317adc831b0cf0759580d5c6924fb3f0997524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369102"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a><span data-ttu-id="b01bd-103">IWICBitmapScaler \_ Initialize \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="b01bd-103">IWICBitmapScaler\_Initialize\_Proxy function</span></span>

<span data-ttu-id="b01bd-104">Proxy Funktion für die [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b01bd-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b01bd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b01bd-105">Syntax</span></span>


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a><span data-ttu-id="b01bd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b01bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b01bd-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b01bd-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b01bd-108">Typ: \**[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) \** _</span><span class="sxs-lookup"><span data-stu-id="b01bd-108">Type: \**[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\** _</span></span>

<span data-ttu-id="b01bd-109">Zeiger auf dieses [_ *IWICBitmapScaler* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b01bd-109">Pointer to this [_ *IWICBitmapScaler*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) object.</span></span>

</dd> <dt>

<span data-ttu-id="b01bd-110">*pisource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b01bd-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b01bd-111">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="b01bd-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="b01bd-112">Die Eingabe Bitmap-Quelle.</span><span class="sxs-lookup"><span data-stu-id="b01bd-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="b01bd-113">_uiWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b01bd-113">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b01bd-114">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="b01bd-114">Type: **UINT**</span></span>

<span data-ttu-id="b01bd-115">Die Ziel Breite.</span><span class="sxs-lookup"><span data-stu-id="b01bd-115">The destination width.</span></span>

</dd> <dt>

<span data-ttu-id="b01bd-116">*uiheight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b01bd-116">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b01bd-117">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="b01bd-117">Type: **UINT**</span></span>

<span data-ttu-id="b01bd-118">Die Höhe der Größe.</span><span class="sxs-lookup"><span data-stu-id="b01bd-118">The desination height.</span></span>

</dd> <dt>

<span data-ttu-id="b01bd-119">*Modus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b01bd-119">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b01bd-120">Typ: **[ **wicbitmapinterpolationmode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span><span class="sxs-lookup"><span data-stu-id="b01bd-120">Type: **[**WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span></span>

<span data-ttu-id="b01bd-121">Der Interpolations Modus, der bei der Skalierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b01bd-121">The interpolation mode to use when scaling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b01bd-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b01bd-122">Return value</span></span>

<span data-ttu-id="b01bd-123">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b01bd-123">Type: **HRESULT**</span></span>

<span data-ttu-id="b01bd-124">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b01bd-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b01bd-125">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b01bd-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b01bd-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b01bd-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b01bd-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b01bd-127">Requirements</span></span>



| <span data-ttu-id="b01bd-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b01bd-128">Requirement</span></span> | <span data-ttu-id="b01bd-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b01bd-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b01bd-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b01bd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b01bd-131">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b01bd-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b01bd-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b01bd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b01bd-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b01bd-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b01bd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b01bd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b01bd-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b01bd-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





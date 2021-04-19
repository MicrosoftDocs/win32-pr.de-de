---
description: Proxy Funktion für die GetPreview-Methode.
ms.assetid: 8251af14-68db-4e4a-a501-115e7bbd53cd
title: IWICBitmapDecoder_GetPreview_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetPreview_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0fc6808d94cdc1cdcdaf65e252107b939e12eeaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350418"
---
# <a name="iwicbitmapdecoder_getpreview_proxy-function"></a><span data-ttu-id="0311b-103">IWICBitmapDecoder \_ GetPreview- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="0311b-103">IWICBitmapDecoder\_GetPreview\_Proxy function</span></span>

<span data-ttu-id="0311b-104">Proxy Funktion für die [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0311b-104">Proxy function for the [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0311b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0311b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetPreview_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIBitmapSource
);
```



## <a name="parameters"></a><span data-ttu-id="0311b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0311b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0311b-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0311b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0311b-108">Typ: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="0311b-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="0311b-109">Zeiger auf dieses [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="0311b-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="0311b-110">*ppibitmapsource* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0311b-110">*ppIBitmapSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0311b-111">Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="0311b-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="0311b-112">Ein Zeiger, der einen Zeiger auf die Vorschau Bitmap erhält, sofern dies unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="0311b-112">A pointer that receives a pointer to the preview bitmap if supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0311b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0311b-113">Return value</span></span>

<span data-ttu-id="0311b-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0311b-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0311b-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="0311b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0311b-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0311b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0311b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0311b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0311b-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0311b-118">Requirements</span></span>



| <span data-ttu-id="0311b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0311b-119">Requirement</span></span> | <span data-ttu-id="0311b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0311b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0311b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0311b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0311b-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0311b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0311b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0311b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0311b-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0311b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0311b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0311b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0311b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0311b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





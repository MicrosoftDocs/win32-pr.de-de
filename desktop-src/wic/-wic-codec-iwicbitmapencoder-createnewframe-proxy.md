---
description: Proxy Funktion für die Methode "kreatenewframe".
ms.assetid: b23e8689-0fdc-49a7-a004-148b50420127
title: IWICBitmapEncoder_CreateNewFrame_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_CreateNewFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c0ddf0141e5b13e370f199e3f211e74c3a0e6e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355337"
---
# <a name="iwicbitmapencoder_createnewframe_proxy-function"></a><span data-ttu-id="91c7c-103">Iwicbitmapcoder- \_ \_ Proxy Funktion von "depcoder"</span><span class="sxs-lookup"><span data-stu-id="91c7c-103">IWICBitmapEncoder\_CreateNewFrame\_Proxy function</span></span>

<span data-ttu-id="91c7c-104">Proxy Funktion für die Methode " [**kreatenewframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) ".</span><span class="sxs-lookup"><span data-stu-id="91c7c-104">Proxy function for the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c7c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="91c7c-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_CreateNewFrame_Proxy(
  _In_    IWICBitmapEncoder     *THIS_PTR,
  _Out_   IWICBitmapFrameEncode **ppIFrameEncode,
  _Inout_ IPropertyBag2         **ppIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="91c7c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="91c7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91c7c-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91c7c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91c7c-108">Typ: \**[**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="91c7c-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="91c7c-109">Zeiger auf dieses [_ *iwicbitmapcoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="91c7c-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="91c7c-110">*ppiframecodieren* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="91c7c-110">*ppIFrameEncode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91c7c-111">Typ: **[ **iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***</span><span class="sxs-lookup"><span data-stu-id="91c7c-111">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***</span></span>

<span data-ttu-id="91c7c-112">Ein Zeiger, der einen Zeiger auf die neue Instanz von [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)empfängt.</span><span class="sxs-lookup"><span data-stu-id="91c7c-112">A pointer that receives a pointer to the new instance of an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span>

</dd> <dt>

<span data-ttu-id="91c7c-113">*ppIEncoderOptions* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="91c7c-113">*ppIEncoderOptions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="91c7c-114">Typ: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***</span><span class="sxs-lookup"><span data-stu-id="91c7c-114">Type: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***</span></span>

<span data-ttu-id="91c7c-115">Die benannten Eigenschaften, die für die Frame Initialisierung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="91c7c-115">The named properties to use for frame initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91c7c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91c7c-116">Return value</span></span>

<span data-ttu-id="91c7c-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="91c7c-117">Type: **HRESULT**</span></span>

<span data-ttu-id="91c7c-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="91c7c-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="91c7c-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="91c7c-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="91c7c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91c7c-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="91c7c-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="91c7c-121">Requirements</span></span>



| <span data-ttu-id="91c7c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91c7c-122">Requirement</span></span> | <span data-ttu-id="91c7c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="91c7c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91c7c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91c7c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="91c7c-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91c7c-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="91c7c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91c7c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="91c7c-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91c7c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="91c7c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="91c7c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91c7c-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91c7c-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 


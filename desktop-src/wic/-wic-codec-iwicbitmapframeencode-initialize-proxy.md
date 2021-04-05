---
description: Proxy Funktion für die Initialize-Methode.
ms.assetid: af9e204c-7072-47b8-84eb-47a754968d5b
title: IWICBitmapFrameEncode_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: da9192409636de96dbd9d35d9614df2c926c9032
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751217"
---
# <a name="iwicbitmapframeencode_initialize_proxy-function"></a><span data-ttu-id="ed3d6-103">IWICBitmapFrameEncode- \_ \_ Proxy Funktion initialisieren</span><span class="sxs-lookup"><span data-stu-id="ed3d6-103">IWICBitmapFrameEncode\_Initialize\_Proxy function</span></span>

<span data-ttu-id="ed3d6-104">Proxy Funktion für die [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ed3d6-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed3d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed3d6-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Initialize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IPropertyBag2         *pIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="ed3d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed3d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed3d6-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed3d6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed3d6-108">Typ: \**[**iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="ed3d6-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="ed3d6-109">Zeiger auf dieses [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ed3d6-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="ed3d6-110">*pIEncoderOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed3d6-110">*pIEncoderOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed3d6-111">Typ: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="ed3d6-111">Type: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\** _</span></span>

<span data-ttu-id="ed3d6-112">Der Satz von Eigenschaften, die für die Initialisierung von [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ed3d6-112">The set of properties to use for [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed3d6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed3d6-113">Return value</span></span>

<span data-ttu-id="ed3d6-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ed3d6-114">Type: **HRESULT**</span></span>

<span data-ttu-id="ed3d6-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ed3d6-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ed3d6-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ed3d6-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed3d6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed3d6-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ed3d6-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ed3d6-118">Requirements</span></span>



| <span data-ttu-id="ed3d6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed3d6-119">Requirement</span></span> | <span data-ttu-id="ed3d6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ed3d6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed3d6-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed3d6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ed3d6-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed3d6-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ed3d6-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed3d6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ed3d6-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed3d6-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ed3d6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ed3d6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed3d6-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed3d6-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 


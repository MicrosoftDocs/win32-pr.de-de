---
description: 'IWICBitmapFrameEncode_Initialize_Proxy Funktion: Proxyfunktion für die Initialize-Methode.'
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
ms.openlocfilehash: e8c8a7526343e6dfcda9859fd06259700019a9bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100548"
---
# <a name="iwicbitmapframeencode_initialize_proxy-function"></a><span data-ttu-id="45857-103">IWICBitmapFrameEncode-Funktion \_ "Proxy initialisieren" \_</span><span class="sxs-lookup"><span data-stu-id="45857-103">IWICBitmapFrameEncode\_Initialize\_Proxy function</span></span>

<span data-ttu-id="45857-104">Proxyfunktion für die [**Initialize-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize)</span><span class="sxs-lookup"><span data-stu-id="45857-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="45857-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="45857-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Initialize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IPropertyBag2         *pIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="45857-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="45857-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45857-107">*DIES \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45857-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45857-108">Typ: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="45857-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="45857-109">Zeiger auf dieses [**IWICBitmapFrameEncode-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="45857-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="45857-110">*pIEncoderOptions* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="45857-110">*pIEncoderOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45857-111">Typ: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="45857-111">Type: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\***</span></span>

<span data-ttu-id="45857-112">Der Satz von Eigenschaften, die für die Initialisierung von [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="45857-112">The set of properties to use for [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45857-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45857-113">Return value</span></span>

<span data-ttu-id="45857-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="45857-114">Type: **HRESULT**</span></span>

<span data-ttu-id="45857-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="45857-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="45857-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="45857-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="45857-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45857-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="45857-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="45857-118">Requirements</span></span>



| <span data-ttu-id="45857-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45857-119">Requirement</span></span> | <span data-ttu-id="45857-120">Wert</span><span class="sxs-lookup"><span data-stu-id="45857-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45857-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45857-121">Minimum supported client</span></span><br/> | <span data-ttu-id="45857-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45857-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="45857-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45857-123">Minimum supported server</span></span><br/> | <span data-ttu-id="45857-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45857-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="45857-125">DLL</span><span class="sxs-lookup"><span data-stu-id="45857-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45857-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="45857-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 


---
description: Proxy Funktion für die SetSize-Methode.
ms.assetid: 28b4967f-4c8a-475c-8f86-c19e5d424a26
title: IWICBitmapFrameEncode_SetSize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0a8046ede01cdd30d6a30eb81cbc1617531ef1d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350324"
---
# <a name="iwicbitmapframeencode_setsize_proxy-function"></a><span data-ttu-id="8ea55-103">IWICBitmapFrameEncode- \_ SetSize- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="8ea55-103">IWICBitmapFrameEncode\_SetSize\_Proxy function</span></span>

<span data-ttu-id="8ea55-104">Proxy Funktion für die [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8ea55-104">Proxy function for the [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea55-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ea55-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetSize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  uiWidth,
  _In_ UINT                  uiHeight
);
```



## <a name="parameters"></a><span data-ttu-id="8ea55-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ea55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ea55-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ea55-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea55-108">Typ: \**[**iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="8ea55-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="8ea55-109">Zeiger auf dieses [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8ea55-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="8ea55-110">*uiwidth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ea55-110">*uiWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea55-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="8ea55-111">Type: **UINT**</span></span>

<span data-ttu-id="8ea55-112">Die Breite des Ausgabe Bilds.</span><span class="sxs-lookup"><span data-stu-id="8ea55-112">The width of the output image.</span></span>

</dd> <dt>

<span data-ttu-id="8ea55-113">*uiheight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ea55-113">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea55-114">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="8ea55-114">Type: **UINT**</span></span>

<span data-ttu-id="8ea55-115">Die Höhe des Ausgabe Bilds.</span><span class="sxs-lookup"><span data-stu-id="8ea55-115">The height of the output image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ea55-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ea55-116">Return value</span></span>

<span data-ttu-id="8ea55-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8ea55-117">Type: **HRESULT**</span></span>

<span data-ttu-id="8ea55-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8ea55-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ea55-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ea55-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ea55-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ea55-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8ea55-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8ea55-121">Requirements</span></span>



| <span data-ttu-id="8ea55-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ea55-122">Requirement</span></span> | <span data-ttu-id="8ea55-123">Wert</span><span class="sxs-lookup"><span data-stu-id="8ea55-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea55-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ea55-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8ea55-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ea55-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8ea55-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ea55-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8ea55-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ea55-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8ea55-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8ea55-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ea55-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ea55-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





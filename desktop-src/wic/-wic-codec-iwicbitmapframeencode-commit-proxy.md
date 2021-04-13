---
description: Proxy Funktion für die Commit-Methode.
ms.assetid: 605801e5-00f8-4e4f-87d3-ad34d3568ee5
title: IWICBitmapFrameEncode_Commit_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0da0cb95a13148082d8263f622bb4089a7c9bd30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343208"
---
# <a name="iwicbitmapframeencode_commit_proxy-function"></a><span data-ttu-id="ef282-103">IWICBitmapFrameEncode \_ Commit- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="ef282-103">IWICBitmapFrameEncode\_Commit\_Proxy function</span></span>

<span data-ttu-id="ef282-104">Proxy Funktion für die [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ef282-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef282-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef282-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Commit_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="ef282-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef282-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef282-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef282-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef282-108">Typ: \**[**iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="ef282-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="ef282-109">Zeiger auf dieses [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ef282-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef282-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef282-110">Return value</span></span>

<span data-ttu-id="ef282-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ef282-111">Type: **HRESULT**</span></span>

<span data-ttu-id="ef282-112">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ef282-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ef282-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ef282-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef282-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef282-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ef282-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ef282-115">Requirements</span></span>



| <span data-ttu-id="ef282-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef282-116">Requirement</span></span> | <span data-ttu-id="ef282-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ef282-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef282-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef282-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ef282-119">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef282-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ef282-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef282-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ef282-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef282-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ef282-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ef282-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef282-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef282-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





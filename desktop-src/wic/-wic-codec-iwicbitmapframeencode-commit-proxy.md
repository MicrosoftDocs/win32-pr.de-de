---
description: 'IWICBitmapFrameEncode_Commit_Proxy-Funktion: Proxyfunktion für die Commit-Methode.'
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
ms.openlocfilehash: 0f8ab87860c77cf58f73491a1fb5fc1b658ed67f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091118"
---
# <a name="iwicbitmapframeencode_commit_proxy-function"></a><span data-ttu-id="9ddb9-103">IWICBitmapFrameEncode-Commitproxyfunktion \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ddb9-103">IWICBitmapFrameEncode\_Commit\_Proxy function</span></span>

<span data-ttu-id="9ddb9-104">Proxyfunktion für die [**Commit-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit)</span><span class="sxs-lookup"><span data-stu-id="9ddb9-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ddb9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ddb9-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Commit_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="9ddb9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ddb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ddb9-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ddb9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ddb9-108">Typ: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="9ddb9-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="9ddb9-109">Zeiger auf dieses [**IWICBitmapFrameEncode-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="9ddb9-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ddb9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ddb9-110">Return value</span></span>

<span data-ttu-id="9ddb9-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9ddb9-111">Type: **HRESULT**</span></span>

<span data-ttu-id="9ddb9-112">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="9ddb9-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ddb9-113">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ddb9-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ddb9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ddb9-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9ddb9-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9ddb9-115">Requirements</span></span>



| <span data-ttu-id="9ddb9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ddb9-116">Requirement</span></span> | <span data-ttu-id="9ddb9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9ddb9-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ddb9-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ddb9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9ddb9-119">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ddb9-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9ddb9-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ddb9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9ddb9-121">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ddb9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9ddb9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9ddb9-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ddb9-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ddb9-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





---
description: 'IWICBitmapEncoder_Commit_Proxy-Funktion: Proxyfunktion für die Commit-Methode.'
ms.assetid: f7f1be43-fe44-47eb-a5ba-3446c0db22a6
title: IWICBitmapEncoder_Commit_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 934b2e21097a671c2b52ea77ab07caf25ab521a3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091188"
---
# <a name="iwicbitmapencoder_commit_proxy-function"></a><span data-ttu-id="06860-103">IWICBitmapEncoder-Commitproxyfunktion \_ \_</span><span class="sxs-lookup"><span data-stu-id="06860-103">IWICBitmapEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="06860-104">Proxyfunktion für [](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) die Commit-Methode.</span><span class="sxs-lookup"><span data-stu-id="06860-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06860-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="06860-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Commit_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="06860-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="06860-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06860-107">*DIES \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06860-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06860-108">Typ: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="06860-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="06860-109">Zeiger auf dieses [**IWICBitmapEncoder-Objekt.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)</span><span class="sxs-lookup"><span data-stu-id="06860-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06860-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06860-110">Return value</span></span>

<span data-ttu-id="06860-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="06860-111">Type: **HRESULT**</span></span>

<span data-ttu-id="06860-112">Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06860-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06860-113">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06860-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="06860-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06860-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="06860-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="06860-115">Requirements</span></span>



| <span data-ttu-id="06860-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06860-116">Requirement</span></span> | <span data-ttu-id="06860-117">Wert</span><span class="sxs-lookup"><span data-stu-id="06860-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06860-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06860-118">Minimum supported client</span></span><br/> | <span data-ttu-id="06860-119">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06860-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="06860-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06860-120">Minimum supported server</span></span><br/> | <span data-ttu-id="06860-121">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06860-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="06860-122">DLL</span><span class="sxs-lookup"><span data-stu-id="06860-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06860-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="06860-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





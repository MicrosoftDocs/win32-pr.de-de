---
description: 'IWICBitmapEncoder_SetThumbnail_Proxy-Funktion: Proxyfunktion für die SetThumbnail-Methode.'
ms.assetid: 6c062eaf-27a4-4d48-8315-be9bf168f999
title: IWICBitmapEncoder_SetThumbnail_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7666fffbac7813db8021daf38ebae9c4e68c57a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100598"
---
# <a name="iwicbitmapencoder_setthumbnail_proxy-function"></a><span data-ttu-id="e8469-103">IWICBitmapEncoder-Funktion \_ "SetThumbnail \_ Proxy"</span><span class="sxs-lookup"><span data-stu-id="e8469-103">IWICBitmapEncoder\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="e8469-104">Proxyfunktion für die [**SetThumbnail-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)</span><span class="sxs-lookup"><span data-stu-id="e8469-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8469-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8469-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetThumbnail_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICBitmapSource  *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="e8469-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8469-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8469-107">*DIES \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8469-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8469-108">Typ: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="e8469-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="e8469-109">Zeiger auf dieses [**IWICBitmapEncoder-Objekt.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)</span><span class="sxs-lookup"><span data-stu-id="e8469-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="e8469-110">*pIThumbnail* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8469-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8469-111">Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="e8469-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="e8469-112">Die [**IWICBitmapSource,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) die als globale Miniaturansicht festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8469-112">The [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to set as the global thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8469-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8469-113">Return value</span></span>

<span data-ttu-id="e8469-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e8469-114">Type: **HRESULT**</span></span>

<span data-ttu-id="e8469-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e8469-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e8469-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e8469-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8469-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8469-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e8469-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e8469-118">Requirements</span></span>



| <span data-ttu-id="e8469-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8469-119">Requirement</span></span> | <span data-ttu-id="e8469-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e8469-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8469-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8469-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e8469-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8469-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e8469-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8469-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e8469-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8469-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e8469-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e8469-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8469-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8469-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





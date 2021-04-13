---
description: Proxy Funktion für die setminiatur-Methode.
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
ms.openlocfilehash: d2670dae0d8ba9eeda7ca1d6dce5d3957dc59b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484763"
---
# <a name="iwicbitmapencoder_setthumbnail_proxy-function"></a><span data-ttu-id="d3538-103">Iwicbitmapcoder \_ setminiatur- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="d3538-103">IWICBitmapEncoder\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="d3538-104">Proxy Funktion für die [**setminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d3538-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3538-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3538-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetThumbnail_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICBitmapSource  *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="d3538-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3538-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3538-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3538-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3538-108">Typ: \**[**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="d3538-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="d3538-109">Zeiger auf dieses [_ *iwicbitmapcoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d3538-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="d3538-110">*piminiatur* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3538-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3538-111">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="d3538-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="d3538-112">Das [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Element, das als globale Miniaturansicht festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3538-112">The [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to set as the global thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3538-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3538-113">Return value</span></span>

<span data-ttu-id="d3538-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d3538-114">Type: **HRESULT**</span></span>

<span data-ttu-id="d3538-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d3538-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3538-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d3538-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3538-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3538-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d3538-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d3538-118">Requirements</span></span>



| <span data-ttu-id="d3538-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3538-119">Requirement</span></span> | <span data-ttu-id="d3538-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d3538-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3538-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3538-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d3538-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3538-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d3538-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3538-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d3538-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3538-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d3538-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d3538-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3538-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3538-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





---
description: Proxy Funktion für die SetResolution-Methode.
ms.assetid: c4e3927c-6f9d-401d-acd7-711674cdbb53
title: IWICBitmap_SetResolution_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eef599147a67986c6b9853f7a67e53a15be68e00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372809"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a><span data-ttu-id="c9941-103">IWICBitmap \_ SetResolution- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="c9941-103">IWICBitmap\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="c9941-104">Proxy Funktion für die [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c9941-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9941-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9941-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="c9941-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9941-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9941-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9941-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9941-108">Typ: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="c9941-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="c9941-109">Zeiger auf dieses [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c9941-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="c9941-110">*Dpix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9941-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9941-111">Typ: **Double**</span><span class="sxs-lookup"><span data-stu-id="c9941-111">Type: **double**</span></span>

<span data-ttu-id="c9941-112">Die horizontale Auflösung.</span><span class="sxs-lookup"><span data-stu-id="c9941-112">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="c9941-113">*DpiY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9941-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9941-114">Typ: **Double**</span><span class="sxs-lookup"><span data-stu-id="c9941-114">Type: **double**</span></span>

<span data-ttu-id="c9941-115">Die vertikale Auflösung.</span><span class="sxs-lookup"><span data-stu-id="c9941-115">The vertical resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9941-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9941-116">Return value</span></span>

<span data-ttu-id="c9941-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c9941-117">Type: **HRESULT**</span></span>

<span data-ttu-id="c9941-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c9941-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c9941-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c9941-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9941-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9941-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c9941-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c9941-121">Requirements</span></span>



| <span data-ttu-id="c9941-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9941-122">Requirement</span></span> | <span data-ttu-id="c9941-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c9941-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9941-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9941-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c9941-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9941-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c9941-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9941-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c9941-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9941-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c9941-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c9941-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9941-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9941-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





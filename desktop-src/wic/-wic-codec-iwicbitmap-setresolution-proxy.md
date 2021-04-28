---
description: 'IWICBitmap_SetResolution_Proxy-Funktion: Proxyfunktion für die SetResolution-Methode.'
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
ms.openlocfilehash: f11189307ad14dde6ea1e1373583a8ab4b08b9be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086378"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a><span data-ttu-id="1b88e-103">IWICBitmap \_ \_ SetResolution-Proxyfunktion</span><span class="sxs-lookup"><span data-stu-id="1b88e-103">IWICBitmap\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="1b88e-104">Proxyfunktion für die [**SetResolution-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution)</span><span class="sxs-lookup"><span data-stu-id="1b88e-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b88e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b88e-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="1b88e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b88e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b88e-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b88e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b88e-108">Typ: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span><span class="sxs-lookup"><span data-stu-id="1b88e-108">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span></span>

<span data-ttu-id="1b88e-109">Zeiger auf dieses [**IWICBitmap-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)</span><span class="sxs-lookup"><span data-stu-id="1b88e-109">Pointer to this [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="1b88e-110">*dpiX* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1b88e-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b88e-111">Typ: **double**</span><span class="sxs-lookup"><span data-stu-id="1b88e-111">Type: **double**</span></span>

<span data-ttu-id="1b88e-112">Die horizontale Auflösung.</span><span class="sxs-lookup"><span data-stu-id="1b88e-112">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="1b88e-113">*dpiY* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1b88e-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b88e-114">Typ: **double**</span><span class="sxs-lookup"><span data-stu-id="1b88e-114">Type: **double**</span></span>

<span data-ttu-id="1b88e-115">Die vertikale Auflösung.</span><span class="sxs-lookup"><span data-stu-id="1b88e-115">The vertical resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b88e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b88e-116">Return value</span></span>

<span data-ttu-id="1b88e-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1b88e-117">Type: **HRESULT**</span></span>

<span data-ttu-id="1b88e-118">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="1b88e-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b88e-119">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b88e-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b88e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b88e-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1b88e-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1b88e-121">Requirements</span></span>



| <span data-ttu-id="1b88e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b88e-122">Requirement</span></span> | <span data-ttu-id="1b88e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1b88e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b88e-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b88e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1b88e-125">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b88e-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1b88e-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b88e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1b88e-127">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b88e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1b88e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1b88e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b88e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b88e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





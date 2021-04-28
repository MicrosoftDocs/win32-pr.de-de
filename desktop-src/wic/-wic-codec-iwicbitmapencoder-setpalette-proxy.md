---
description: 'IWICBitmapEncoder_SetPalette_Proxy-Funktion: Proxyfunktion für die SetPalette-Methode.'
ms.assetid: d8e2c36e-6886-4959-b2a2-469bebfe1cdc
title: IWICBitmapEncoder_SetPalette_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8503698a1e91b86698ba288e56cc65e4447c906e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091178"
---
# <a name="iwicbitmapencoder_setpalette_proxy-function"></a><span data-ttu-id="41e71-103">IWICBitmapEncoder \_ \_ SetPalette-Proxyfunktion</span><span class="sxs-lookup"><span data-stu-id="41e71-103">IWICBitmapEncoder\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="41e71-104">Proxyfunktion für die [**SetPalette-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette)</span><span class="sxs-lookup"><span data-stu-id="41e71-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e71-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="41e71-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetPalette_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="41e71-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="41e71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41e71-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41e71-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e71-108">Typ: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="41e71-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="41e71-109">Zeiger auf dieses [**IWICBitmapEncoder-Objekt.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)</span><span class="sxs-lookup"><span data-stu-id="41e71-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="41e71-110">*pIPalette* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="41e71-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e71-111">Typ: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="41e71-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="41e71-112">Die [**IWICPalette,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) die als globale Palette verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="41e71-112">The [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) to use as the global palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41e71-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41e71-113">Return value</span></span>

<span data-ttu-id="41e71-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="41e71-114">Type: **HRESULT**</span></span>

<span data-ttu-id="41e71-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="41e71-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="41e71-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="41e71-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="41e71-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41e71-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="41e71-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="41e71-118">Requirements</span></span>



| <span data-ttu-id="41e71-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41e71-119">Requirement</span></span> | <span data-ttu-id="41e71-120">Wert</span><span class="sxs-lookup"><span data-stu-id="41e71-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41e71-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41e71-121">Minimum supported client</span></span><br/> | <span data-ttu-id="41e71-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41e71-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="41e71-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41e71-123">Minimum supported server</span></span><br/> | <span data-ttu-id="41e71-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41e71-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="41e71-125">DLL</span><span class="sxs-lookup"><span data-stu-id="41e71-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41e71-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="41e71-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





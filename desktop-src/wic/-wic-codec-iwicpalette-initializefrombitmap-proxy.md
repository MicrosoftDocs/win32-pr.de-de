---
description: Proxy Funktion für die initializefrombitmap-Methode.
ms.assetid: 9559a56d-7201-4b39-a3cd-9c0e4eac611a
title: IWICPalette_InitializeFromBitmap_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf5e119acf1efca948281a02f61d8954f4e08818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350961"
---
# <a name="iwicpalette_initializefrombitmap_proxy-function"></a><span data-ttu-id="7f5ea-103">Iwicpalette \_ initializefrombitmap- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="7f5ea-103">IWICPalette\_InitializeFromBitmap\_Proxy function</span></span>

<span data-ttu-id="7f5ea-104">Proxy Funktion für die [**initializefrombitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7f5ea-104">Proxy function for the [**InitializeFromBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f5ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f5ea-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeFromBitmap_Proxy(
  _In_ IWICPalette      *THIS_PTR,
  _In_ IWICBitmapSource *pISurface,
  _In_ UINT             colorCount,
  _In_ BOOL             fAddTransparentColor
);
```



## <a name="parameters"></a><span data-ttu-id="7f5ea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f5ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f5ea-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f5ea-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f5ea-108">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="7f5ea-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="7f5ea-109">Zeiger auf dieses [_ *iwicpalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7f5ea-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="7f5ea-110">*pisurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f5ea-110">*pISurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f5ea-111">Typ: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="7f5ea-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="7f5ea-112">Ein Zeiger auf die Quell Bitmap.</span><span class="sxs-lookup"><span data-stu-id="7f5ea-112">Pointer to the source bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="7f5ea-113">_colorCount \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f5ea-113">_colorCount\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f5ea-114">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="7f5ea-114">Type: **UINT**</span></span>

<span data-ttu-id="7f5ea-115">Die Anzahl der Farben, mit denen die Palette initialisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f5ea-115">The number of colors to initialize the palette with.</span></span>

</dd> <dt>

<span data-ttu-id="7f5ea-116">*faddtransparentcolor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f5ea-116">*fAddTransparentColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f5ea-117">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="7f5ea-117">Type: **BOOL**</span></span>

<span data-ttu-id="7f5ea-118">Ein Wert, der angibt, ob eine transparente Farbe hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f5ea-118">A value to indicate whether to add a transparent color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f5ea-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f5ea-119">Return value</span></span>

<span data-ttu-id="7f5ea-120">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7f5ea-120">Type: **HRESULT**</span></span>

<span data-ttu-id="7f5ea-121">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7f5ea-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7f5ea-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7f5ea-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f5ea-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f5ea-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7f5ea-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7f5ea-124">Requirements</span></span>



| <span data-ttu-id="7f5ea-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f5ea-125">Requirement</span></span> | <span data-ttu-id="7f5ea-126">Wert</span><span class="sxs-lookup"><span data-stu-id="7f5ea-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f5ea-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f5ea-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7f5ea-128">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f5ea-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7f5ea-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f5ea-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7f5ea-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f5ea-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7f5ea-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7f5ea-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f5ea-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f5ea-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





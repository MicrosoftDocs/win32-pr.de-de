---
description: Proxy Funktion für die initializevordefinierten-Methode.
ms.assetid: 78137d43-c32f-4d60-b289-2e2154cf4d1e
title: IWICPalette_InitializePredefined_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializePredefined_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d65202d9d7800763e15f52ef0eb03b16bc348e78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758850"
---
# <a name="iwicpalette_initializepredefined_proxy-function"></a><span data-ttu-id="97208-103">Iwicpalette \_ initializevordefinierten \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="97208-103">IWICPalette\_InitializePredefined\_Proxy function</span></span>

<span data-ttu-id="97208-104">Proxy Funktion für die [**initializevordefinierten**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) -Methode.</span><span class="sxs-lookup"><span data-stu-id="97208-104">Proxy function for the [**InitializePredefined**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="97208-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97208-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializePredefined_Proxy(
  _In_ IWICPalette          *THIS_PTR,
  _In_ WICBitmapPaletteType ePaletteType,
  _In_ BOOL                 fAddTransparentColor
);
```



## <a name="parameters"></a><span data-ttu-id="97208-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97208-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97208-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97208-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97208-108">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="97208-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="97208-109">Zeiger auf dieses [_ *iwicpalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="97208-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="97208-110">*epalettetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97208-110">*ePaletteType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97208-111">Typ: **[ **wicbitmappalettetype**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="97208-111">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="97208-112">Der gewünschte vordefinierte Palettentyp.</span><span class="sxs-lookup"><span data-stu-id="97208-112">The desired pre-defined palette type.</span></span>

</dd> <dt>

<span data-ttu-id="97208-113">*faddtransparentcolor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97208-113">*fAddTransparentColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97208-114">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="97208-114">Type: **BOOL**</span></span>

<span data-ttu-id="97208-115">Die optionale übergeordnete Farbe, die der Palette hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="97208-115">The optional tranparent color to add to the palette.</span></span> <span data-ttu-id="97208-116">Wenn keine transparente Farbe erforderlich ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="97208-116">If no transparent color is needed, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97208-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97208-117">Return value</span></span>

<span data-ttu-id="97208-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="97208-118">Type: **HRESULT**</span></span>

<span data-ttu-id="97208-119">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="97208-119">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="97208-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97208-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="97208-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97208-121">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="97208-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="97208-122">Requirements</span></span>



| <span data-ttu-id="97208-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97208-123">Requirement</span></span> | <span data-ttu-id="97208-124">Wert</span><span class="sxs-lookup"><span data-stu-id="97208-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97208-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97208-125">Minimum supported client</span></span><br/> | <span data-ttu-id="97208-126">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97208-126">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="97208-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97208-127">Minimum supported server</span></span><br/> | <span data-ttu-id="97208-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97208-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="97208-129">DLL</span><span class="sxs-lookup"><span data-stu-id="97208-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97208-130"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97208-130"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





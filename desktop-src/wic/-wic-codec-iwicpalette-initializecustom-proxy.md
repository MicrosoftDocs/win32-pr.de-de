---
description: Proxy Funktion für die initializecustom-Methode.
ms.assetid: fe742b12-5338-41b0-b90b-aec852a26518
title: IWICPalette_InitializeCustom_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeCustom_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3b64daf458a6b916f0f9e2ba23e135d6c7328a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353917"
---
# <a name="iwicpalette_initializecustom_proxy-function"></a><span data-ttu-id="a7f6e-103">Iwicpalette \_ \_ initializecustomproxyfunktion</span><span class="sxs-lookup"><span data-stu-id="a7f6e-103">IWICPalette\_InitializeCustom\_Proxy function</span></span>

<span data-ttu-id="a7f6e-104">Proxy Funktion für die [**initializecustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a7f6e-104">Proxy function for the [**InitializeCustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f6e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7f6e-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeCustom_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ WICColor    *pColors,
  _In_ UINT        colorCount
);
```



## <a name="parameters"></a><span data-ttu-id="a7f6e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7f6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7f6e-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7f6e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f6e-108">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="a7f6e-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="a7f6e-109">Zeiger auf dieses [_ *iwicpalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a7f6e-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="a7f6e-110">*pcolors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7f6e-110">*pColors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f6e-111">Typ: \**wiccolor \** _</span><span class="sxs-lookup"><span data-stu-id="a7f6e-111">Type: \**WICColor\** _</span></span>

<span data-ttu-id="a7f6e-112">Zeiger auf das Farbarray.</span><span class="sxs-lookup"><span data-stu-id="a7f6e-112">Pointer to the color array.</span></span>

</dd> <dt>

<span data-ttu-id="a7f6e-113">_colorCount \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7f6e-113">_colorCount\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f6e-114">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="a7f6e-114">Type: **UINT**</span></span>

<span data-ttu-id="a7f6e-115">Die Anzahl der Farben in *pcolors*.</span><span class="sxs-lookup"><span data-stu-id="a7f6e-115">The number of colors in *pColors*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7f6e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7f6e-116">Return value</span></span>

<span data-ttu-id="a7f6e-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a7f6e-117">Type: **HRESULT**</span></span>

<span data-ttu-id="a7f6e-118">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a7f6e-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a7f6e-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a7f6e-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7f6e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7f6e-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f6e-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a7f6e-121">Requirements</span></span>



| <span data-ttu-id="a7f6e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7f6e-122">Requirement</span></span> | <span data-ttu-id="a7f6e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a7f6e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f6e-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7f6e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a7f6e-125">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7f6e-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a7f6e-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7f6e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a7f6e-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7f6e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a7f6e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a7f6e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7f6e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7f6e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





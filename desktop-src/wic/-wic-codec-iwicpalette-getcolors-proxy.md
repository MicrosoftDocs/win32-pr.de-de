---
description: Proxy Funktion für die getcolors-Methode.
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: IWICPalette_GetColors_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColors_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e39e8825b78175fabb5a37e331236e7bf0d9ed73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216971"
---
# <a name="iwicpalette_getcolors_proxy-function"></a><span data-ttu-id="29572-103">Iwicpalette \_ getcolors- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="29572-103">IWICPalette\_GetColors\_Proxy function</span></span>

<span data-ttu-id="29572-104">Proxy Funktion für die [**getcolors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) -Methode.</span><span class="sxs-lookup"><span data-stu-id="29572-104">Proxy function for the [**GetColors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="29572-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="29572-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetColors_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _In_  UINT        colorCount,
  _Out_ WICColor    *pColors,
  _Out_ UINT        *pcActualColors
);
```



## <a name="parameters"></a><span data-ttu-id="29572-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="29572-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29572-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29572-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29572-108">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="29572-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="29572-109">Zeiger auf dieses [_ *iwicpalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="29572-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="29572-110">*colorcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29572-110">*colorCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29572-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="29572-111">Type: **UINT**</span></span>

<span data-ttu-id="29572-112">Die Größe des *pcolors* -Arrays.</span><span class="sxs-lookup"><span data-stu-id="29572-112">The size of the *pColors* array.</span></span>

</dd> <dt>

<span data-ttu-id="29572-113">*pcolors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="29572-113">*pColors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29572-114">Typ: \**wiccolor \** _</span><span class="sxs-lookup"><span data-stu-id="29572-114">Type: \**WICColor\** _</span></span>

<span data-ttu-id="29572-115">Ein Zeiger, der die Farben der Palette empfängt.</span><span class="sxs-lookup"><span data-stu-id="29572-115">Pointer that receives the colors of the palette.</span></span>

</dd> <dt>

<span data-ttu-id="29572-116">_pcActualColors \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="29572-116">_pcActualColors\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29572-117">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="29572-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="29572-118">Die tatsächliche Größe, die zum Abrufen der Palettenfarben benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="29572-118">The actual size needed to obtain the palette colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29572-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29572-119">Return value</span></span>

<span data-ttu-id="29572-120">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="29572-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="29572-121">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="29572-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="29572-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="29572-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="29572-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29572-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="29572-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="29572-124">Requirements</span></span>



| <span data-ttu-id="29572-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29572-125">Requirement</span></span> | <span data-ttu-id="29572-126">Wert</span><span class="sxs-lookup"><span data-stu-id="29572-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29572-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29572-127">Minimum supported client</span></span><br/> | <span data-ttu-id="29572-128">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29572-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="29572-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29572-129">Minimum supported server</span></span><br/> | <span data-ttu-id="29572-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29572-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="29572-131">DLL</span><span class="sxs-lookup"><span data-stu-id="29572-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29572-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29572-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





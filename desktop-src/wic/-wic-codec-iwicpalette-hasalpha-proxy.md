---
description: Proxy Funktion für die hasalpha-Methode.
ms.assetid: 8af9f588-ac22-40c4-8973-9636951cc9e6
title: IWICPalette_HasAlpha_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_HasAlpha_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6f9398b2d570efb41048d88ddeeeb76d62f4ca37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960173"
---
# <a name="iwicpalette_hasalpha_proxy-function"></a><span data-ttu-id="18973-103">Iwicpalette \_ hasalpha- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="18973-103">IWICPalette\_HasAlpha\_Proxy function</span></span>

<span data-ttu-id="18973-104">Proxy Funktion für die [**hasalpha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) -Methode.</span><span class="sxs-lookup"><span data-stu-id="18973-104">Proxy function for the [**HasAlpha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="18973-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18973-105">Syntax</span></span>


```C++
HRESULT IWICPalette_HasAlpha_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ BOOL        *pfHasAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="18973-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="18973-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18973-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18973-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18973-108">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="18973-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="18973-109">Zeiger auf dieses [_ *iwicpalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="18973-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="18973-110">*pfhasalpha* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="18973-110">*pfHasAlpha* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18973-111">Typ: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="18973-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="18973-112">Ein Zeiger, `TRUE` der empfängt, wenn die Palette eine transparente Farbe enthält; andernfalls `FALSE` .</span><span class="sxs-lookup"><span data-stu-id="18973-112">Pointer that receives `TRUE` if the palette contains a transparent color; otherwise, `FALSE`.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18973-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18973-113">Return value</span></span>

<span data-ttu-id="18973-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="18973-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="18973-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="18973-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18973-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18973-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="18973-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18973-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="18973-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="18973-118">Requirements</span></span>



| <span data-ttu-id="18973-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18973-119">Requirement</span></span> | <span data-ttu-id="18973-120">Wert</span><span class="sxs-lookup"><span data-stu-id="18973-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18973-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18973-121">Minimum supported client</span></span><br/> | <span data-ttu-id="18973-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18973-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="18973-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18973-123">Minimum supported server</span></span><br/> | <span data-ttu-id="18973-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18973-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="18973-125">DLL</span><span class="sxs-lookup"><span data-stu-id="18973-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18973-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18973-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





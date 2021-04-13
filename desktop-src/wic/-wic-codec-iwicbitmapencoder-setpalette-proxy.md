---
description: Proxy Funktion für die SetPalette-Methode.
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
ms.openlocfilehash: 128953cd56c3bea17ec9761a2acf2b8bc89cacfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525928"
---
# <a name="iwicbitmapencoder_setpalette_proxy-function"></a><span data-ttu-id="a2f0b-103">Iwicbitmapcoder \_ SetPalette- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="a2f0b-103">IWICBitmapEncoder\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="a2f0b-104">Proxy Funktion für die [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a2f0b-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2f0b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2f0b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetPalette_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="a2f0b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2f0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2f0b-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2f0b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2f0b-108">Typ: \**[**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="a2f0b-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="a2f0b-109">Zeiger auf dieses [_ *iwicbitmapcoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a2f0b-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="a2f0b-110">*pipalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2f0b-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2f0b-111">Typ: \**[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="a2f0b-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="a2f0b-112">Die [_ *iwicpalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) , die als globale Palette verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2f0b-112">The [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) to use as the global palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2f0b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2f0b-113">Return value</span></span>

<span data-ttu-id="a2f0b-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a2f0b-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a2f0b-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a2f0b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a2f0b-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a2f0b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2f0b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2f0b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a2f0b-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a2f0b-118">Requirements</span></span>



| <span data-ttu-id="a2f0b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2f0b-119">Requirement</span></span> | <span data-ttu-id="a2f0b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a2f0b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2f0b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2f0b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a2f0b-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2f0b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a2f0b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2f0b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a2f0b-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2f0b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a2f0b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a2f0b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2f0b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2f0b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





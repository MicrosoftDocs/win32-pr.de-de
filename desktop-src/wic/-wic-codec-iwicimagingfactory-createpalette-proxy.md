---
description: Proxy Funktion für die CreatePalette-Methode.
ms.assetid: c83b4239-ce6b-4a4c-ab70-df31dfcdd26c
title: IWICImagingFactory_CreatePalette_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreatePalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 626c05ec5e4e365cf61304c4b33e621967cea5e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352773"
---
# <a name="iwicimagingfactory_createpalette_proxy-function"></a><span data-ttu-id="7009a-103">IWICImagingFactory \_ CreatePalette \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="7009a-103">IWICImagingFactory\_CreatePalette\_Proxy function</span></span>

<span data-ttu-id="7009a-104">Proxy Funktion für die [**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7009a-104">Proxy function for the [**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7009a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7009a-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreatePalette_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICPalette        **ppIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="7009a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7009a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7009a-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7009a-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7009a-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="7009a-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="7009a-109">_ppIPalette \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7009a-109">_ppIPalette\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7009a-110">Typ: **[ **iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***</span><span class="sxs-lookup"><span data-stu-id="7009a-110">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***</span></span>

<span data-ttu-id="7009a-111">Ein Zeiger, der einen Zeiger auf eine neue [**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)empfängt.</span><span class="sxs-lookup"><span data-stu-id="7009a-111">A pointer that receives a pointer to a new [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7009a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7009a-112">Return value</span></span>

<span data-ttu-id="7009a-113">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7009a-113">Type: **HRESULT**</span></span>

<span data-ttu-id="7009a-114">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7009a-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7009a-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7009a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7009a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7009a-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7009a-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7009a-117">Requirements</span></span>



| <span data-ttu-id="7009a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7009a-118">Requirement</span></span> | <span data-ttu-id="7009a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7009a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7009a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7009a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7009a-121">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7009a-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7009a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7009a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7009a-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7009a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7009a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7009a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7009a-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7009a-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





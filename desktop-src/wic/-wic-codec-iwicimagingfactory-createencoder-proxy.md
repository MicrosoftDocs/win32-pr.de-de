---
description: Proxy Funktion für die Methode "kreateencoder".
ms.assetid: e3ffad7f-eb0e-481d-81ee-caf18e14ba59
title: IWICImagingFactory_CreateEncoder_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateEncoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 38e5dd19ddc07de42f8be9e8c887a4f412a853b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347420"
---
# <a name="iwicimagingfactory_createencoder_proxy-function"></a><span data-ttu-id="66a18-103">IWICImagingFactory- \_ \_ Proxyfunktion</span><span class="sxs-lookup"><span data-stu-id="66a18-103">IWICImagingFactory\_CreateEncoder\_Proxy function</span></span>

<span data-ttu-id="66a18-104">Proxy Funktion für die Methode " [**kreateencoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder) ".</span><span class="sxs-lookup"><span data-stu-id="66a18-104">Proxy function for the [**CreateEncoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a18-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="66a18-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateEncoder_Proxy(
  _In_           IWICImagingFactory *pFactory,
  _In_           REFGUID            guidContainerFormat,
  _In_opt_ const GUID               *pguidVendor,
  _Out_          IWICBitmapEncoder  **ppIEncoder
);
```



## <a name="parameters"></a><span data-ttu-id="66a18-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="66a18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66a18-107">*pfactory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66a18-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a18-108">Typ: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="66a18-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="66a18-109">_guidContainerFormat \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66a18-109">_guidContainerFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a18-110">Typ: **reguid**</span><span class="sxs-lookup"><span data-stu-id="66a18-110">Type: **REFGUID**</span></span>

<span data-ttu-id="66a18-111">Die GUID für das gewünschte Containerformat.</span><span class="sxs-lookup"><span data-stu-id="66a18-111">The GUID for the desired container format.</span></span>

</dd> <dt>

<span data-ttu-id="66a18-112">*pguidVendor* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="66a18-112">*pguidVendor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="66a18-113">Geben Sie Folgendes ein: \* Konstante *GUID \** _</span><span class="sxs-lookup"><span data-stu-id="66a18-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="66a18-114">Die Anbieter-GUID für den Encoder.</span><span class="sxs-lookup"><span data-stu-id="66a18-114">The vendor GUID for the encoder.</span></span>

</dd> <dt>

<span data-ttu-id="66a18-115">_ppIEncoder \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="66a18-115">_ppIEncoder\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66a18-116">Typ: **[ **iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="66a18-116">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***</span></span>

<span data-ttu-id="66a18-117">Ein Zeiger, der einen Zeiger auf einen neuen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)empfängt.</span><span class="sxs-lookup"><span data-stu-id="66a18-117">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66a18-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66a18-118">Return value</span></span>

<span data-ttu-id="66a18-119">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="66a18-119">Type: **HRESULT**</span></span>

<span data-ttu-id="66a18-120">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="66a18-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="66a18-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="66a18-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="66a18-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66a18-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="66a18-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="66a18-123">Requirements</span></span>



| <span data-ttu-id="66a18-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66a18-124">Requirement</span></span> | <span data-ttu-id="66a18-125">Wert</span><span class="sxs-lookup"><span data-stu-id="66a18-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66a18-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66a18-126">Minimum supported client</span></span><br/> | <span data-ttu-id="66a18-127">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66a18-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="66a18-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66a18-128">Minimum supported server</span></span><br/> | <span data-ttu-id="66a18-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66a18-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="66a18-130">DLL</span><span class="sxs-lookup"><span data-stu-id="66a18-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66a18-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66a18-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





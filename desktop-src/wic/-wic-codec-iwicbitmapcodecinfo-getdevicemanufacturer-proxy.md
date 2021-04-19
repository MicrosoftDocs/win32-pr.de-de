---
description: Proxy Funktion für die getdevicemanufacturer-Methode.
ms.assetid: f4dbf67a-eb67-4138-a77a-7386567b95e6
title: IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3dc10df32325fd0ffc5bb24d1a4c7927b1adc7e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346302"
---
# <a name="iwicbitmapcodecinfo_getdevicemanufacturer_proxy-function"></a><span data-ttu-id="c65cb-103">Iwicbitmapcodecinfo \_ getdevicemanufakturer \_ Proxy-Funktion</span><span class="sxs-lookup"><span data-stu-id="c65cb-103">IWICBitmapCodecInfo\_GetDeviceManufacturer\_Proxy function</span></span>

<span data-ttu-id="c65cb-104">Proxy Funktion für die [**getdevicemanufacturer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c65cb-104">Proxy function for the [**GetDeviceManufacturer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c65cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c65cb-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceManufacturer,
  _Inout_ WCHAR               *wzDeviceManufacturer,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="c65cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c65cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c65cb-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c65cb-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65cb-108">Typ: \**[**iwicbitmapcodecinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="c65cb-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="c65cb-109">Zeiger auf dieses [_ *iwicbitmapcodecinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c65cb-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="c65cb-110">*cchdevicemanufakturer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c65cb-110">*cchDeviceManufacturer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65cb-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="c65cb-111">Type: **UINT**</span></span>

<span data-ttu-id="c65cb-112">Die Größe des Namens der Gerätefertigung.</span><span class="sxs-lookup"><span data-stu-id="c65cb-112">The size of the device manufacture's name.</span></span>

</dd> <dt>

<span data-ttu-id="c65cb-113">*wzdebug-emanufakturer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c65cb-113">*wzDeviceManufacturer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c65cb-114">Typ: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="c65cb-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="c65cb-115">Ein Zeiger, der den Namen der Geräte Herstellung empfängt.</span><span class="sxs-lookup"><span data-stu-id="c65cb-115">A pointer that receives the device manufacture's name.</span></span>

</dd> <dt>

<span data-ttu-id="c65cb-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c65cb-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c65cb-117">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="c65cb-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="c65cb-118">Die tatsächliche Puffergröße, die zum Abrufen des Namens der Gerätefertigung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="c65cb-118">The actual buffer size needed to retrieve the device manufacture's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c65cb-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c65cb-119">Return value</span></span>

<span data-ttu-id="c65cb-120">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c65cb-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c65cb-121">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c65cb-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c65cb-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c65cb-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c65cb-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c65cb-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c65cb-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c65cb-124">Requirements</span></span>



| <span data-ttu-id="c65cb-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c65cb-125">Requirement</span></span> | <span data-ttu-id="c65cb-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c65cb-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c65cb-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c65cb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c65cb-128">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c65cb-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c65cb-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c65cb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c65cb-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c65cb-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c65cb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c65cb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c65cb-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c65cb-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





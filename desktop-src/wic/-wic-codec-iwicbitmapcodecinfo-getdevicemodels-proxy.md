---
description: Proxy Funktion für die getdevicemodels-Methode.
ms.assetid: de8f91f7-fef7-48bc-94fc-34c43175248b
title: IWICBitmapCodecInfo_GetDeviceModels_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceModels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b8fa6d6df6984569aa3fe49fc734f7699aa504d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348163"
---
# <a name="iwicbitmapcodecinfo_getdevicemodels_proxy-function"></a><span data-ttu-id="1b4f3-103">Iwicbitmapcodecinfo \_ getdevicemodels- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="1b4f3-103">IWICBitmapCodecInfo\_GetDeviceModels\_Proxy function</span></span>

<span data-ttu-id="1b4f3-104">Proxy Funktion für die [**getdevicemodels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1b4f3-104">Proxy function for the [**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b4f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b4f3-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceModels_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceModels,
  _Inout_ WCHAR               *wzDeviceModels,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="1b4f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b4f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b4f3-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4f3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4f3-108">Typ: \**[**iwicbitmapcodecinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="1b4f3-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="1b4f3-109">Zeiger auf dieses [_ *iwicbitmapcodecinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b4f3-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="1b4f3-110">*cchdevicemodels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4f3-110">*cchDeviceModels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4f3-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="1b4f3-111">Type: **UINT**</span></span>

<span data-ttu-id="1b4f3-112">Die Größe des Gerätemodell Puffers.</span><span class="sxs-lookup"><span data-stu-id="1b4f3-112">The size of the device models buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1b4f3-113">*wzdevicemodels* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1b4f3-113">*wzDeviceModels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4f3-114">Typ: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="1b4f3-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="1b4f3-115">Ein Zeiger, der eine durch Trennzeichen getrennte Liste von Gerätemodell Namen empfängt, die dem Codec zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1b4f3-115">A pointer that receives a comma delimited list of device model names associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="1b4f3-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1b4f3-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4f3-117">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="1b4f3-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="1b4f3-118">Die tatsächliche Puffergröße, die zum Abrufen aller Gerätemodell Namen benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="1b4f3-118">The actual buffer size needed to retrieve all of the device model names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b4f3-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b4f3-119">Return value</span></span>

<span data-ttu-id="1b4f3-120">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1b4f3-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1b4f3-121">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="1b4f3-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b4f3-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b4f3-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b4f3-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b4f3-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1b4f3-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1b4f3-124">Requirements</span></span>



| <span data-ttu-id="1b4f3-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b4f3-125">Requirement</span></span> | <span data-ttu-id="1b4f3-126">Wert</span><span class="sxs-lookup"><span data-stu-id="1b4f3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b4f3-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b4f3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1b4f3-128">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b4f3-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1b4f3-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b4f3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1b4f3-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b4f3-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1b4f3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1b4f3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b4f3-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b4f3-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





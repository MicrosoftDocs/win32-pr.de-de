---
description: Proxy Funktion für die doessupportanimation-Methode.
ms.assetid: dd7ed856-14b5-4215-96da-8f5db19a7796
title: IWICBitmapCodecInfo_DoesSupportAnimation_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportAnimation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 443a8ec7871af6161de2efbb6d4f21d65e5ae9d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345045"
---
# <a name="iwicbitmapcodecinfo_doessupportanimation_proxy-function"></a><span data-ttu-id="bb29e-103">Iwicbitmapcodecinfo ( \_ doessupportanimation- \_ Proxy Funktion)</span><span class="sxs-lookup"><span data-stu-id="bb29e-103">IWICBitmapCodecInfo\_DoesSupportAnimation\_Proxy function</span></span>

<span data-ttu-id="bb29e-104">Proxy Funktion für die [**doessupportanimation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bb29e-104">Proxy function for the [**DoesSupportAnimation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb29e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb29e-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportAnimation_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportAnimation
);
```



## <a name="parameters"></a><span data-ttu-id="bb29e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb29e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb29e-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb29e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb29e-108">Typ: \**[**iwicbitmapcodecinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="bb29e-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="bb29e-109">Zeiger auf dieses [_ *iwicbitmapcodecinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="bb29e-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="bb29e-110">*pfsupportanimation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bb29e-110">*pfSupportAnimation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb29e-111">Typ: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="bb29e-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="bb29e-112">Ein Zeiger, der _ *true*\* empfängt, wenn der Codec Bilder mit Zeit Steuerungsinformationen unterstützt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="bb29e-112">A pointer that receives _ *TRUE*\* if the codec supports images with timing information; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb29e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb29e-113">Return value</span></span>

<span data-ttu-id="bb29e-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bb29e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="bb29e-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="bb29e-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb29e-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bb29e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb29e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb29e-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bb29e-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bb29e-118">Requirements</span></span>



| <span data-ttu-id="bb29e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb29e-119">Requirement</span></span> | <span data-ttu-id="bb29e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="bb29e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb29e-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb29e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bb29e-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb29e-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bb29e-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb29e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bb29e-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb29e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bb29e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bb29e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb29e-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb29e-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





---
description: Proxy Funktion für die doessupportlossless-Methode.
ms.assetid: c88d7971-cc93-458c-a31e-19a8b8350d09
title: IWICBitmapCodecInfo_DoesSupportLossless_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportLossless_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6f498af72391aa0a7745ed79d06c6e1d55317393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751248"
---
# <a name="iwicbitmapcodecinfo_doessupportlossless_proxy-function"></a><span data-ttu-id="cd760-103">Iwicbitmapcodecinfo ( \_ doessupportlossless- \_ Proxy Funktion)</span><span class="sxs-lookup"><span data-stu-id="cd760-103">IWICBitmapCodecInfo\_DoesSupportLossless\_Proxy function</span></span>

<span data-ttu-id="cd760-104">Proxy Funktion für die [**doessupportlossless**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportlossless) -Methode.</span><span class="sxs-lookup"><span data-stu-id="cd760-104">Proxy function for the [**DoesSupportLossless**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportlossless) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd760-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd760-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportLossless_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportLossless
);
```



## <a name="parameters"></a><span data-ttu-id="cd760-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd760-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd760-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd760-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd760-108">Typ: \**[**iwicbitmapcodecinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="cd760-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="cd760-109">Zeiger auf dieses [_ *iwicbitmapcodecinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="cd760-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="cd760-110">*pfsupportlossless* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cd760-110">*pfSupportLossless* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd760-111">Typ: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="cd760-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="cd760-112">Ein Zeiger, der _ *true*\* empfängt, wenn der Codec verlustfreie Formate unterstützt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="cd760-112">A pointer that receives _ *TRUE*\* if the codec supports lossless formats; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd760-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd760-113">Return value</span></span>

<span data-ttu-id="cd760-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cd760-114">Type: **HRESULT**</span></span>

<span data-ttu-id="cd760-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="cd760-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cd760-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cd760-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd760-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd760-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cd760-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cd760-118">Requirements</span></span>



| <span data-ttu-id="cd760-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd760-119">Requirement</span></span> | <span data-ttu-id="cd760-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cd760-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd760-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd760-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cd760-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd760-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cd760-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd760-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cd760-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd760-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cd760-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cd760-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd760-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd760-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





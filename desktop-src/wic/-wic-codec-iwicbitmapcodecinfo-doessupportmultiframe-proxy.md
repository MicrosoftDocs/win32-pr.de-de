---
description: Proxy Funktion für die doessupportmultiframe-Methode.
ms.assetid: ceee0090-ff23-4eb4-b0ea-de1d12bceef8
title: IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d148127345e77da027191114f7e411bdae564deb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128965"
---
# <a name="iwicbitmapcodecinfo_doessupportmultiframe_proxy-function"></a><span data-ttu-id="71772-103">Iwicbitmapcodecinfo \_ doessupportmultiframe- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="71772-103">IWICBitmapCodecInfo\_DoesSupportMultiframe\_Proxy function</span></span>

<span data-ttu-id="71772-104">Proxy Funktion für die [**doessupportmultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe) -Methode.</span><span class="sxs-lookup"><span data-stu-id="71772-104">Proxy function for the [**DoesSupportMultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="71772-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="71772-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportMultiframe
);
```



## <a name="parameters"></a><span data-ttu-id="71772-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="71772-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71772-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71772-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71772-108">Typ: \**[**iwicbitmapcodecinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="71772-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="71772-109">Zeiger auf dieses [_ *iwicbitmapcodecinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="71772-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="71772-110">*pfsupportmultiframe* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="71772-110">*pfSupportMultiframe* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71772-111">Typ: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="71772-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="71772-112">Ein Zeiger, der _ *true*\* empfängt, wenn der Codec Multiframe-Bilder unterstützt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="71772-112">A pointer that receives _ *TRUE*\* if the codec supports multi frame images; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71772-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71772-113">Return value</span></span>

<span data-ttu-id="71772-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="71772-114">Type: **HRESULT**</span></span>

<span data-ttu-id="71772-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="71772-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="71772-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="71772-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="71772-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71772-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="71772-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="71772-118">Requirements</span></span>



| <span data-ttu-id="71772-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71772-119">Requirement</span></span> | <span data-ttu-id="71772-120">Wert</span><span class="sxs-lookup"><span data-stu-id="71772-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71772-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71772-121">Minimum supported client</span></span><br/> | <span data-ttu-id="71772-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71772-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="71772-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71772-123">Minimum supported server</span></span><br/> | <span data-ttu-id="71772-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71772-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="71772-125">DLL</span><span class="sxs-lookup"><span data-stu-id="71772-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71772-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71772-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





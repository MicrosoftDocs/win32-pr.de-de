---
description: Proxy Funktion für die GetContainerFormat-Methode.
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: IWICBitmapCodecInfo_GetContainerFormat_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 896c2ff88085c0300cffcc56c2877b98cd4ab68a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214548"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a><span data-ttu-id="497f8-103">Iwicbitmapcodecinfo \_ GetContainerFormat- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="497f8-103">IWICBitmapCodecInfo\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="497f8-104">Proxy Funktion für die [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) -Methode.</span><span class="sxs-lookup"><span data-stu-id="497f8-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="497f8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="497f8-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="497f8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="497f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="497f8-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="497f8-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="497f8-108">Typ: \**[**iwicbitmapcodecinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="497f8-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="497f8-109">Zeiger auf dieses [_ *iwicbitmapcodecinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="497f8-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="497f8-110">*pguidcontainerformat* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="497f8-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="497f8-111">Geben Sie Folgendes ein: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="497f8-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="497f8-112">Ein Zeiger, der die Container-GUID empfängt.</span><span class="sxs-lookup"><span data-stu-id="497f8-112">A pointer that receives the container GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="497f8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="497f8-113">Return value</span></span>

<span data-ttu-id="497f8-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="497f8-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="497f8-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="497f8-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="497f8-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="497f8-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="497f8-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="497f8-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="497f8-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="497f8-118">Requirements</span></span>



| <span data-ttu-id="497f8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="497f8-119">Requirement</span></span> | <span data-ttu-id="497f8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="497f8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="497f8-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="497f8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="497f8-122">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="497f8-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="497f8-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="497f8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="497f8-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="497f8-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="497f8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="497f8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="497f8-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="497f8-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





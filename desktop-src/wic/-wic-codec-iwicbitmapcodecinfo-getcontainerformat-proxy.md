---
description: 'IWICBitmapCodecInfo_GetContainerFormat_Proxy-Funktion: Proxyfunktion für die GetContainerFormat-Methode.'
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
ms.openlocfilehash: 729b4e2fe0f21fd1e96082e53194fd49bbc39ae1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086368"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a><span data-ttu-id="0305d-103">IWICBitmapCodecInfo \_ \_ GetContainerFormat-Proxyfunktion</span><span class="sxs-lookup"><span data-stu-id="0305d-103">IWICBitmapCodecInfo\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="0305d-104">Proxyfunktion für die [**GetContainerFormat-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat)</span><span class="sxs-lookup"><span data-stu-id="0305d-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0305d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0305d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="0305d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0305d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0305d-107">*THIS \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0305d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0305d-108">Typ: **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***</span><span class="sxs-lookup"><span data-stu-id="0305d-108">Type: **[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***</span></span>

<span data-ttu-id="0305d-109">Zeiger auf dieses [**IWICBitmapCodecInfo-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)</span><span class="sxs-lookup"><span data-stu-id="0305d-109">Pointer to this [**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="0305d-110">*pguidContainerFormat* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0305d-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0305d-111">Typ: **GUID \***</span><span class="sxs-lookup"><span data-stu-id="0305d-111">Type: **GUID\***</span></span>

<span data-ttu-id="0305d-112">Ein Zeiger, der die Container-GUID empfängt.</span><span class="sxs-lookup"><span data-stu-id="0305d-112">A pointer that receives the container GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0305d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0305d-113">Return value</span></span>

<span data-ttu-id="0305d-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0305d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0305d-115">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="0305d-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0305d-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0305d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0305d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0305d-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0305d-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0305d-118">Requirements</span></span>



| <span data-ttu-id="0305d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0305d-119">Requirement</span></span> | <span data-ttu-id="0305d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0305d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0305d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0305d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0305d-122">Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0305d-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0305d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0305d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0305d-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0305d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0305d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0305d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0305d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0305d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





---
description: Proxy Funktion für die getFileExtensions-Methode.
ms.assetid: 1c9232c5-54f3-4186-a1c8-4531e8357d06
title: IWICBitmapCodecInfo_GetFileExtensions_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetFileExtensions_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7dc44622bb7d576bfe4dc8a70e69779a72c1c07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343229"
---
# <a name="iwicbitmapcodecinfo_getfileextensions_proxy-function"></a><span data-ttu-id="a544d-103">Iwicbitmapcodecinfo \_ getFileExtensions- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="a544d-103">IWICBitmapCodecInfo\_GetFileExtensions\_Proxy function</span></span>

<span data-ttu-id="a544d-104">Proxy Funktion für die [**getFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a544d-104">Proxy function for the [**GetFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a544d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a544d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetFileExtensions_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchFileExtensions,
  _Inout_ WCHAR               *wzFileExtensions,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="a544d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a544d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a544d-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a544d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a544d-108">Typ: \**[**iwicbitmapcodecinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="a544d-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="a544d-109">Zeiger auf dieses [_ *iwicbitmapcodecinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a544d-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="a544d-110">*cchfileextensions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a544d-110">*cchFileExtensions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a544d-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="a544d-111">Type: **UINT**</span></span>

<span data-ttu-id="a544d-112">Die Größe des Dateinamen-Erweiterungs Puffers.</span><span class="sxs-lookup"><span data-stu-id="a544d-112">The size of the file name extension buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a544d-113">*wzfileextensions* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a544d-113">*wzFileExtensions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a544d-114">Typ: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="a544d-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="a544d-115">Ein Zeiger, der die Dateinamen Erweiterungen empfängt, die dem Codec zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a544d-115">A pointer that receives the file name extensions associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="a544d-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a544d-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a544d-117">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="a544d-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="a544d-118">Die tatsächliche Puffergröße, die benötigt wird, um alle dem Codec zugeordneten Dateinamen Erweiterungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a544d-118">The actual buffer size needed to retrieve all file name extensions associated with the codec.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a544d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a544d-119">Return value</span></span>

<span data-ttu-id="a544d-120">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a544d-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a544d-121">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a544d-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a544d-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a544d-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a544d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a544d-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a544d-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a544d-124">Requirements</span></span>



| <span data-ttu-id="a544d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a544d-125">Requirement</span></span> | <span data-ttu-id="a544d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a544d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a544d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a544d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a544d-128">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a544d-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a544d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a544d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a544d-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a544d-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a544d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a544d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a544d-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a544d-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





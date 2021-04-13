---
description: Proxy Funktion für die getmimetypes-Methode.
ms.assetid: 9d05624f-da08-4475-933b-faa12bec9012
title: IWICBitmapCodecInfo_GetMimeTypes_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetMimeTypes_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eb00b2ae3cd935171a9333a55a76038ef9ae2ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525934"
---
# <a name="iwicbitmapcodecinfo_getmimetypes_proxy-function"></a><span data-ttu-id="1dafd-103">Iwicbitmapcodecinfo \_ getmimetypes- \_ Proxy Funktion</span><span class="sxs-lookup"><span data-stu-id="1dafd-103">IWICBitmapCodecInfo\_GetMimeTypes\_Proxy function</span></span>

<span data-ttu-id="1dafd-104">Proxy Funktion für die [**getmimetypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1dafd-104">Proxy function for the [**GetMimeTypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dafd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dafd-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetMimeTypes_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _In_  UINT                cchMimeTypes,
  _Out_ WCHAR               *wzMimeTypes,
  _Out_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="1dafd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dafd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dafd-107">*Dies \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dafd-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dafd-108">Typ: \**[**iwicbitmapcodecinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="1dafd-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="1dafd-109">Zeiger auf dieses [_ *iwicbitmapcodecinfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1dafd-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="1dafd-110">*cchmimetypes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dafd-110">*cchMimeTypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dafd-111">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="1dafd-111">Type: **UINT**</span></span>

<span data-ttu-id="1dafd-112">Die Größe des MIME-Typen Puffers.</span><span class="sxs-lookup"><span data-stu-id="1dafd-112">The size of the mime types buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1dafd-113">*wzmimetypes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1dafd-113">*wzMimeTypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dafd-114">Typ: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="1dafd-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="1dafd-115">Ein Zeiger, der die MIME-Typen empfängt, die dem Codec zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1dafd-115">A pointer that receives the mime types associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="1dafd-116">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1dafd-116">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dafd-117">Typ: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="1dafd-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="1dafd-118">Die tatsächliche Puffergröße, die zum Abrufen aller dem Codec zugeordneten MIME-Typen benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="1dafd-118">The actual buffer size needed to retrieve all mime types associated with the codec.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dafd-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1dafd-119">Return value</span></span>

<span data-ttu-id="1dafd-120">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1dafd-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1dafd-121">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="1dafd-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1dafd-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1dafd-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dafd-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1dafd-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1dafd-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1dafd-124">Requirements</span></span>



| <span data-ttu-id="1dafd-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1dafd-125">Requirement</span></span> | <span data-ttu-id="1dafd-126">Wert</span><span class="sxs-lookup"><span data-stu-id="1dafd-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dafd-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1dafd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1dafd-128">Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1dafd-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1dafd-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1dafd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1dafd-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1dafd-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1dafd-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1dafd-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dafd-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1dafd-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





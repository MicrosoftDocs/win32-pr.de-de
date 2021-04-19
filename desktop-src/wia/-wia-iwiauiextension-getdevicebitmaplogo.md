---
description: Ruft ein benutzerdefiniertes bitmaplogo für das Gerät ab.
ms.assetid: 56b3c7c9-64f4-4853-9eb7-d876d02a851f
title: 'Iwiauiextension:: getdevicebitmaplogo-Methode (wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceBitmapLogo
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 51db237c93a2167eb3c4bdae648f9d79da13319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348789"
---
# <a name="iwiauiextensiongetdevicebitmaplogo-method"></a><span data-ttu-id="73fd6-103">Iwiauiextension:: getdevicebitmaplogo-Methode</span><span class="sxs-lookup"><span data-stu-id="73fd6-103">IWiaUIExtension::GetDeviceBitmapLogo method</span></span>

<span data-ttu-id="73fd6-104">Ruft ein benutzerdefiniertes bitmaplogo für das Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="73fd6-104">Gets a custom bitmap logo for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="73fd6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="73fd6-105">Syntax</span></span>


```C++
HRESULT GetDeviceBitmapLogo(
  [in]  BSTR    bstrDeviceId,
  [out] HBITMAP *phBitmap,
  [in]  ULONG   nMaxWidth,
  [in]  ULONG   nMaxHeight
);
```



## <a name="parameters"></a><span data-ttu-id="73fd6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="73fd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73fd6-107">*bstraude viceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73fd6-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73fd6-108">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="73fd6-108">Type: **BSTR**</span></span>

<span data-ttu-id="73fd6-109">Gibt die Geräte-ID des WIA-Geräts an, für das das Symbol abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="73fd6-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="73fd6-110">*phbitmap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="73fd6-110">*phBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73fd6-111">Typ: \**hBitmap \** _</span><span class="sxs-lookup"><span data-stu-id="73fd6-111">Type: \**HBITMAP\** _</span></span>

<span data-ttu-id="73fd6-112">Verweist auf einen Speicherort, der ein Handle für das bitmaplogo für das Gerät empfängt.</span><span class="sxs-lookup"><span data-stu-id="73fd6-112">Points to a memory location that will receive a handle for the bitmap logo for the device.</span></span>

</dd> <dt>

<span data-ttu-id="73fd6-113">_nMaxWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73fd6-113">_nMaxWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73fd6-114">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="73fd6-114">Type: **ULONG**</span></span>

<span data-ttu-id="73fd6-115">Gibt die gewünschte Breite der Bitmap an.</span><span class="sxs-lookup"><span data-stu-id="73fd6-115">Specifies the desired width of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="73fd6-116">*nmaxheight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73fd6-116">*nMaxHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73fd6-117">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="73fd6-117">Type: **ULONG**</span></span>

<span data-ttu-id="73fd6-118">Gibt die gewünschte Höhe der Bitmap an.</span><span class="sxs-lookup"><span data-stu-id="73fd6-118">Specifies the desired height of the bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73fd6-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73fd6-119">Return value</span></span>

<span data-ttu-id="73fd6-120">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="73fd6-120">Type: **HRESULT**</span></span>

<span data-ttu-id="73fd6-121">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="73fd6-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73fd6-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="73fd6-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="73fd6-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73fd6-123">Requirements</span></span>



| <span data-ttu-id="73fd6-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73fd6-124">Requirement</span></span> | <span data-ttu-id="73fd6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="73fd6-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="73fd6-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73fd6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="73fd6-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73fd6-127">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="73fd6-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73fd6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="73fd6-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73fd6-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="73fd6-130">Header</span><span class="sxs-lookup"><span data-stu-id="73fd6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="73fd6-131"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="73fd6-131"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 





---
description: Fragt den Lese-/Schreibstatus einer DXVA-Decodierungs Oberfläche (DirectX Video Acceleration) ab.
ms.assetid: 8a4c3173-5911-49ec-8cb8-e30f96a4f1c9
title: 'IDirect3DDXVADevice9:: QueryStatus-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.QueryStatus
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ae2b16ef27b1e172b7927652304104563e120709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356833"
---
# <a name="idirect3ddxvadevice9querystatus-method"></a><span data-ttu-id="93c29-103">IDirect3DDXVADevice9:: QueryStatus-Methode</span><span class="sxs-lookup"><span data-stu-id="93c29-103">IDirect3DDXVADevice9::QueryStatus method</span></span>

<span data-ttu-id="93c29-104">Fragt den Lese-/Schreibstatus einer DXVA-Decodierungs Oberfläche (DirectX Video Acceleration) ab.</span><span class="sxs-lookup"><span data-stu-id="93c29-104">Queries the read/write status of a DirectX Video Acceleration (DXVA) decoding surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c29-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="93c29-105">Syntax</span></span>


```C++
HRESULT QueryStatus(
   IDirect3DSurface9 *pSurface,
   DWORD             Flags
);
```



## <a name="parameters"></a><span data-ttu-id="93c29-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="93c29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93c29-107">*pSurface*</span><span class="sxs-lookup"><span data-stu-id="93c29-107">*pSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="93c29-108">Ein Zeiger auf die **IDirect3DSurface9** -Schnittstelle der abzufragende Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="93c29-108">Pointer to the **IDirect3DSurface9** interface of the surface to query.</span></span>

</dd> <dt>

<span data-ttu-id="93c29-109">*Flags*</span><span class="sxs-lookup"><span data-stu-id="93c29-109">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="93c29-110">Gibt den Typ der auszuführenden Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="93c29-110">Specifies the type of query to perform.</span></span>



| <span data-ttu-id="93c29-111">Wert</span><span class="sxs-lookup"><span data-stu-id="93c29-111">Value</span></span>                                                                                                                             | <span data-ttu-id="93c29-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="93c29-112">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="0x00"></span><span id="0X00"></span><dl> <span data-ttu-id="93c29-113"><dt>**0x00**</dt></span><span class="sxs-lookup"><span data-stu-id="93c29-113"><dt>**0x00**</dt></span></span> </dl> | <span data-ttu-id="93c29-114">Testen Sie, ob die Oberfläche sicher zum Schreiben verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="93c29-114">Test whether the surface is safe to use for writing.</span></span><br/> |
| <span id="0x01"></span><span id="0X01"></span><dl> <span data-ttu-id="93c29-115"><dt>**0x01**</dt></span><span class="sxs-lookup"><span data-stu-id="93c29-115"><dt>**0x01**</dt></span></span> </dl> | <span data-ttu-id="93c29-116">Testen Sie, ob die Oberfläche sicher zum Lesen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="93c29-116">Test whether the surface is safe to use for reading.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93c29-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93c29-117">Return value</span></span>

<span data-ttu-id="93c29-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="93c29-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="93c29-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="93c29-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="93c29-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93c29-120">Requirements</span></span>



| <span data-ttu-id="93c29-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93c29-121">Requirement</span></span> | <span data-ttu-id="93c29-122">Wert</span><span class="sxs-lookup"><span data-stu-id="93c29-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="93c29-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93c29-123">Minimum supported client</span></span><br/> | <span data-ttu-id="93c29-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93c29-124">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="93c29-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93c29-125">Minimum supported server</span></span><br/> | <span data-ttu-id="93c29-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93c29-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="93c29-127">Header</span><span class="sxs-lookup"><span data-stu-id="93c29-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="93c29-128"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="93c29-128"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93c29-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93c29-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93c29-130">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="93c29-130">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 





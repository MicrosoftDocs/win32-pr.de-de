---
title: IMsRdpClient9 AttachEvent-Methode
description: Fügt ein Ereignis an.
ms.assetid: 3a887aeb-a74f-4477-8cf3-8ac43a31fa26
ms.tgt_platform: multiple
keywords:
- AttachEvent-Methode Remotedesktopdienste
- AttachEvent-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, AttachEvent-Methode
- AttachEvent-Methode Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10 Interface Remotedesktopdienste, AttachEvent-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient9.attachEvent
- IMsRdpClient10.attachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bd3fd518fba825c209a4170e6b314a7b774a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475243"
---
# <a name="imsrdpclient9attachevent-method"></a><span data-ttu-id="a2dc1-108">IMsRdpClient9:: AttachEvent-Methode</span><span class="sxs-lookup"><span data-stu-id="a2dc1-108">IMsRdpClient9::attachEvent method</span></span>

<span data-ttu-id="a2dc1-109">Fügt ein Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-109">Attaches an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2dc1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2dc1-110">Syntax</span></span>


```C++
HRESULT attachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a><span data-ttu-id="a2dc1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2dc1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2dc1-112">*EventName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2dc1-112">*eventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2dc1-113">Das anzufügende Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-113">The event to attach.</span></span>

</dd> <dt>

<span data-ttu-id="a2dc1-114">*Rückruf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2dc1-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2dc1-115">Der Rückruf.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-115">The callback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2dc1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2dc1-116">Return value</span></span>

<span data-ttu-id="a2dc1-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a2dc1-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2dc1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2dc1-119">Requirements</span></span>



| <span data-ttu-id="a2dc1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2dc1-120">Requirement</span></span> | <span data-ttu-id="a2dc1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a2dc1-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2dc1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2dc1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a2dc1-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a2dc1-123">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a2dc1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2dc1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a2dc1-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a2dc1-125">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="a2dc1-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a2dc1-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="a2dc1-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2dc1-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="a2dc1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a2dc1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2dc1-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2dc1-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="a2dc1-130">IID</span><span class="sxs-lookup"><span data-stu-id="a2dc1-130">IID</span></span><br/>                      | <span data-ttu-id="a2dc1-131">CLSID \_ MsRdpClient9 ist als 301b94ba-5d25-4a12-bffe-3b6e7a616585 definiert</span><span class="sxs-lookup"><span data-stu-id="a2dc1-131">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="a2dc1-132">CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-132">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="a2dc1-133">IID \_ IMsRdpClient9 ist als 28904001-04b6-436C-a55b-0af1a0883dc9 definiert.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-133">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2dc1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2dc1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2dc1-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="a2dc1-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="a2dc1-136">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a2dc1-136">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> </dl>

 

 






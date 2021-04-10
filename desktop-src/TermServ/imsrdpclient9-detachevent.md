---
title: IMsRdpClient9 DetachEvent-Methode
description: Trennt ein Ereignis.
ms.assetid: 6a3ca713-1d5c-4070-a527-ad4f532a4cbf
ms.tgt_platform: multiple
keywords:
- DetachEvent-Methode Remotedesktopdienste
- DetachEvent-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, DetachEvent-Methode
- DetachEvent-Methode Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10 Interface Remotedesktopdienste, DetachEvent-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient9.detachEvent
- IMsRdpClient10.detachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399611ea526338f4cfe40ef3a4d6543bf27f134a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102939"
---
# <a name="imsrdpclient9detachevent-method"></a><span data-ttu-id="39ce4-108">IMsRdpClient9::d etachevent-Methode</span><span class="sxs-lookup"><span data-stu-id="39ce4-108">IMsRdpClient9::detachEvent method</span></span>

<span data-ttu-id="39ce4-109">Trennt ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="39ce4-109">Detaches an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="39ce4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="39ce4-110">Syntax</span></span>


```C++
HRESULT detachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a><span data-ttu-id="39ce4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="39ce4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39ce4-112">*EventName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39ce4-112">*eventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39ce4-113">Name der Veranstaltung.</span><span class="sxs-lookup"><span data-stu-id="39ce4-113">Name of the event.</span></span>

</dd> <dt>

<span data-ttu-id="39ce4-114">*Rückruf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39ce4-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39ce4-115">Der dem Ereignis zugeordnete Rückruf.</span><span class="sxs-lookup"><span data-stu-id="39ce4-115">The callback associated with the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39ce4-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39ce4-116">Return value</span></span>

<span data-ttu-id="39ce4-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="39ce4-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="39ce4-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="39ce4-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="39ce4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39ce4-119">Requirements</span></span>



| <span data-ttu-id="39ce4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39ce4-120">Requirement</span></span> | <span data-ttu-id="39ce4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="39ce4-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39ce4-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39ce4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="39ce4-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="39ce4-123">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="39ce4-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39ce4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="39ce4-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="39ce4-125">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="39ce4-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="39ce4-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="39ce4-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39ce4-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="39ce4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="39ce4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39ce4-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39ce4-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="39ce4-130">IID</span><span class="sxs-lookup"><span data-stu-id="39ce4-130">IID</span></span><br/>                      | <span data-ttu-id="39ce4-131">CLSID \_ MsRdpClient9 ist als 301b94ba-5d25-4a12-bffe-3b6e7a616585 definiert</span><span class="sxs-lookup"><span data-stu-id="39ce4-131">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="39ce4-132">CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.</span><span class="sxs-lookup"><span data-stu-id="39ce4-132">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="39ce4-133">IID \_ IMsRdpClient9 ist als 28904001-04b6-436C-a55b-0af1a0883dc9 definiert.</span><span class="sxs-lookup"><span data-stu-id="39ce4-133">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39ce4-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39ce4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39ce4-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="39ce4-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="39ce4-136">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="39ce4-136">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> </dl>

 

 






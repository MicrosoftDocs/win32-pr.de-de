---
title: Ivmvirtualpcevents oneventlogger-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass Windows Virtual PC ein Ereignis protokolliert.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- Oneventlogger-Methode Virtual PC
- Oneventlogger-Methode Virtual PC, ivmvirtualpcevents-Schnittstelle
- Ivmvirtualpcevents Interface Virtual PC, oneventlogger-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnEventLogged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196d480383f488c9c0885e95857c8d1a053d5887
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518005"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a><span data-ttu-id="a7451-106">Ivmvirtualpcevents:: oneventlogger-Methode</span><span class="sxs-lookup"><span data-stu-id="a7451-106">IVMVirtualPCEvents::OnEventLogged method</span></span>

<span data-ttu-id="a7451-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a7451-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a7451-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a7451-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a7451-109">Empfängt eine Benachrichtigung, dass Windows Virtual PC ein Ereignis protokolliert.</span><span class="sxs-lookup"><span data-stu-id="a7451-109">Receives notification that Windows Virtual PC logs an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7451-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7451-110">Syntax</span></span>


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a><span data-ttu-id="a7451-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7451-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7451-112">*logmessageid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7451-112">*logMessageID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7451-113">Der Meldungs Bezeichner der Ereignisprotokoll Meldung, die protokolliert wurde.</span><span class="sxs-lookup"><span data-stu-id="a7451-113">The message identifier of the event log message that was logged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7451-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7451-114">Return value</span></span>

<span data-ttu-id="a7451-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a7451-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a7451-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a7451-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7451-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7451-117">Remarks</span></span>

<span data-ttu-id="a7451-118">Diese Methode wird aufgerufen, wenn Windows Virtual PC eine Meldung im Windows-Ereignisprotokoll protokolliert.</span><span class="sxs-lookup"><span data-stu-id="a7451-118">This method is called when Windows Virtual PC logs a message to the Windows event log.</span></span> <span data-ttu-id="a7451-119">Das Client Programm muss diese Schnittstellen Methode implementieren, um Benachrichtigungen über das Ereignis vom Typ " **vmvirtualpcevent Ereignis \_ protokolliert** " zu erhalten, das von [**ivmvirtualpc**](ivmvirtualpc.md)stammt.</span><span class="sxs-lookup"><span data-stu-id="a7451-119">The client program must implement this interface method to receive notification of the **vmVirtualPCEvent\_EventLogged** event originating from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7451-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7451-120">Requirements</span></span>



| <span data-ttu-id="a7451-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7451-121">Requirement</span></span> | <span data-ttu-id="a7451-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a7451-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7451-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7451-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a7451-124">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7451-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a7451-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7451-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a7451-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a7451-126">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a7451-127">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a7451-127">End of client support</span></span><br/>    | <span data-ttu-id="a7451-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a7451-128">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a7451-129">Produkt</span><span class="sxs-lookup"><span data-stu-id="a7451-129">Product</span></span><br/>                  | <span data-ttu-id="a7451-130">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a7451-130">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a7451-131">Header</span><span class="sxs-lookup"><span data-stu-id="a7451-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7451-132"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7451-132"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a7451-133">IID</span><span class="sxs-lookup"><span data-stu-id="a7451-133">IID</span></span><br/>                      | <span data-ttu-id="a7451-134">Diid \_ ivmvirtualpcevents ist als efed1ef1-3c09-41f7-a9c2-7e29fa286c9d definiert.</span><span class="sxs-lookup"><span data-stu-id="a7451-134">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="a7451-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7451-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7451-136">**Ivmvirtualpcevents**</span><span class="sxs-lookup"><span data-stu-id="a7451-136">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 


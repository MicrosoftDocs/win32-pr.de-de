---
description: Die OnStart-Methode ist eine optionale Methode, die vom Monitor implementiert werden kann. Die mcsvc ruft diese Methode auf, um anzufordern, dass der Monitor die Erfassung startet.
ms.assetid: 992ee27e-aaba-4e65-989b-e3f0fbd542ea
title: 'Imonitor:: OnStart-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStart
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: ca9e5e17de1d6baf2c79cc0077c5e2036a2a6246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128324"
---
# <a name="imonitoronstart-method"></a><span data-ttu-id="ffb58-104">Imonitor:: OnStart-Methode</span><span class="sxs-lookup"><span data-stu-id="ffb58-104">IMonitor::OnStart method</span></span>

<span data-ttu-id="ffb58-105">Die **OnStart** -Methode ist eine optionale Methode, die vom Monitor implementiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ffb58-105">The **OnStart** method is an optional method that can be implemented by the monitor.</span></span> <span data-ttu-id="ffb58-106">Die mcsvc ruft diese Methode auf, um anzufordern, dass der Monitor die Erfassung startet.</span><span class="sxs-lookup"><span data-stu-id="ffb58-106">The MCSVC calls this method to request that the monitor start the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffb58-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffb58-107">Syntax</span></span>


```C++
HRESULT OnStart(
  [in] IUnknown *pUnkNPP
);
```



## <a name="parameters"></a><span data-ttu-id="ffb58-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffb58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffb58-109">*punknpp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffb58-109">*pUnkNPP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb58-110">Ein [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger auf die [untc](irtc.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ffb58-110">An [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer to the [IRTC](irtc.md) interface.</span></span> <span data-ttu-id="ffb58-111">Der Monitor kann diese Schnittstelle verwenden, um Statistiken abzurufen, die verwendet werden können, um zu bestimmen, ob die Erfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ffb58-111">The monitor can use this interface to obtain statistics that can be used to determine if the capture should be started.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffb58-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffb58-112">Return value</span></span>

<span data-ttu-id="ffb58-113">Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK (entspricht noError).</span><span class="sxs-lookup"><span data-stu-id="ffb58-113">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span> <span data-ttu-id="ffb58-114">Wenn S \_ OK zurückgegeben wird, ruft der mcsvc die Methode " [untc:: Start](irtc-start.md) " auf.</span><span class="sxs-lookup"><span data-stu-id="ffb58-114">When S\_OK is returned, the MCSVC calls the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="ffb58-115">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ffb58-115">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="ffb58-116">Die mcsvc startet die Erfassung nicht, wenn ein Fehlercode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ffb58-116">The MCSVC will not start the capture if any error code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffb58-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffb58-117">Remarks</span></span>

<span data-ttu-id="ffb58-118">Die mcsvc ruft diese Methode auf, bevor die [untc:: Start](irtc-start.md) -Methode von NPP aufgerufen wird, um die Erfassung zu starten.</span><span class="sxs-lookup"><span data-stu-id="ffb58-118">The MCSVC calls this method before the NPP's [IRTC::Start](irtc-start.md) method is called to start the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffb58-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffb58-119">Requirements</span></span>



| <span data-ttu-id="ffb58-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffb58-120">Requirement</span></span> | <span data-ttu-id="ffb58-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ffb58-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb58-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ffb58-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ffb58-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffb58-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ffb58-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ffb58-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ffb58-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffb58-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ffb58-126">Header</span><span class="sxs-lookup"><span data-stu-id="ffb58-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffb58-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffb58-127"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffb58-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffb58-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffb58-129">Imonitor</span><span class="sxs-lookup"><span data-stu-id="ffb58-129">IMonitor</span></span>](imonitor.md)
</dt> <dt>

[<span data-ttu-id="ffb58-130">Netzwerk Paketanbieter</span><span class="sxs-lookup"><span data-stu-id="ffb58-130">Network Packet Providers</span></span>](network-packet-providers.md)
</dt> </dl>

 


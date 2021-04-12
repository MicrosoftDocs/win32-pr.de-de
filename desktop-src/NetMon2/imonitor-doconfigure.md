---
description: Die doconfigure-Methode muss vom Monitor implementiert werden. Die mcsvc ruft diese Methode auf, um Konfigurationsinformationen für die Erfassung zu erhalten.
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: Imonitor::D oconfigure-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoConfigure
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: e9a0ba2ade1095f291d5cb325a0902e6caeac3f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128916"
---
# <a name="imonitordoconfigure-method"></a><span data-ttu-id="63832-104">Imonitor::D oconfigure-Methode</span><span class="sxs-lookup"><span data-stu-id="63832-104">IMonitor::DoConfigure method</span></span>

<span data-ttu-id="63832-105">Die **doconfigure** -Methode muss vom Monitor implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="63832-105">The **DoConfigure** method must be implemented by the monitor.</span></span> <span data-ttu-id="63832-106">Die mcsvc ruft diese Methode auf, um Konfigurationsinformationen für die Erfassung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="63832-106">The MCSVC calls this method to obtain configuration information for the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="63832-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="63832-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE DoConfigure(
  [in]  char *pName,
  [in]  char *pConfiguration,
  [out] char **ppScriptInstance
);
```



## <a name="parameters"></a><span data-ttu-id="63832-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="63832-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63832-109">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63832-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63832-110">Der Name einer Instanz des Monitors.</span><span class="sxs-lookup"><span data-stu-id="63832-110">Name of an instance of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="63832-111">*pconfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63832-111">*pConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63832-112">Konfigurations Zeichenfolge, die von mcsvc bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="63832-112">Configuration string provided by the MCSVC.</span></span> <span data-ttu-id="63832-113">Der Monitor muss diese Zeichenfolge für Konfigurationsdaten analysieren.</span><span class="sxs-lookup"><span data-stu-id="63832-113">The monitor must parse this string for configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="63832-114">*ppscriptinstance* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="63832-114">*ppScriptInstance* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63832-115">Adresse der HTML-Zeichenfolge, die zum Konfigurieren des Monitors verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63832-115">Address of the HTML string used to configure the monitor.</span></span> <span data-ttu-id="63832-116">Wenn ein Standardskript für die Konfiguration verwendet wird, sollte dieser Wert auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="63832-116">If a default script is used for configuration, this value should be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63832-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63832-117">Return value</span></span>

<span data-ttu-id="63832-118">Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK (entspricht noError), und der mcsvc führt den Monitor aus.</span><span class="sxs-lookup"><span data-stu-id="63832-118">If the method is successful, the return value is S\_OK (which is the same as NOERROR), and the MCSVC will run the monitor.</span></span>

<span data-ttu-id="63832-119">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="63832-119">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="63832-120">Der Rückgabewert der nmerr- \_ Monitor \_ Konfiguration \_ ist fehlgeschlagen, aber wenn dieser Fehler zurückgegeben wird, kann der Monitor erst gestartet werden, wenn ein zukünftiger **doconfigure** -Rückruf erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="63832-120">A return value of NMERR\_MONITOR\_CONFIG\_FAILED is acceptable, but when this error is returned, the monitor cannot start until a future **DoConfigure** call succeeds.</span></span> <span data-ttu-id="63832-121">Jeder andere Fehler verhindert, dass die Instanz des Monitors aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="63832-121">Any other error prevents the instance of the monitor from being enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="63832-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63832-122">Remarks</span></span>

<span data-ttu-id="63832-123">Die mcsvc ruft diese Methode auf, nachdem Sie eine Verbindung mit dem Netzwerk hergestellt hat und bevor die Methode " [iritc:: Configure](irtc-configure.md) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="63832-123">The MCSVC calls this method after it has connected to the network and before the [IRTC::Configure](irtc-configure.md) method is called.</span></span>

<span data-ttu-id="63832-124">Der Monitor kann die von diesem-Befehl bereitgestellten Informationen speichern, das HTML-Skript oder die Konfigurations Zeichenfolge aktualisieren und den [Erfassungs Filter](capture-filters.md) im NPP-BLOB festlegen.</span><span class="sxs-lookup"><span data-stu-id="63832-124">The monitor can store information provided by this call, update the HTML script or configuration string, and set the [capture filter](capture-filters.md) in the NPP BLOB.</span></span>

<span data-ttu-id="63832-125">Die mcsvc kann diese Methode mehrmals aufrufen, aber Sie kann nicht aufgerufen werden, während der Monitor Daten erfasst.</span><span class="sxs-lookup"><span data-stu-id="63832-125">The MCSVC may call this method several times, but it cannot be not called while the monitor is capturing data.</span></span> <span data-ttu-id="63832-126">Beachten Sie, dass jedes Mal, wenn eine [NPP](network-packet-providers.md) eine Erfassung startet, die Verbindung mit dem Netzwerk konfiguriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="63832-126">Note that every time an [NPP](network-packet-providers.md) starts a capture, the connection to the network must be configured.</span></span> <span data-ttu-id="63832-127">Diese Einschränkung umfasst Situationen, in denen die NPP die gleiche Erfassung startet und beendet.</span><span class="sxs-lookup"><span data-stu-id="63832-127">This restriction includes situations in which the NPP starts and stops the same capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="63832-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63832-128">Requirements</span></span>



| <span data-ttu-id="63832-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63832-129">Requirement</span></span> | <span data-ttu-id="63832-130">Wert</span><span class="sxs-lookup"><span data-stu-id="63832-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="63832-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63832-131">Minimum supported client</span></span><br/> | <span data-ttu-id="63832-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63832-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="63832-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63832-133">Minimum supported server</span></span><br/> | <span data-ttu-id="63832-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63832-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="63832-135">Header</span><span class="sxs-lookup"><span data-stu-id="63832-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="63832-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="63832-136"><dt>Netmon.h</dt></span></span> </dl> |



 

 





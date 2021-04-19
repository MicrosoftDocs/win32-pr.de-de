---
description: Die Meldung "line \_ proxystatus" wird gesendet, wenn sich die verfügbaren Proxys in einer Zeile ändern, die derzeit von der Anwendung geöffnet wurde.
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: LINE_PROXYSTATUS Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb00c5df4f531309bdd1311fb7c34c3e9967a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359388"
---
# <a name="line_proxystatus-message"></a><span data-ttu-id="a5198-103">Zeile \_ proxystatus-Meldung</span><span class="sxs-lookup"><span data-stu-id="a5198-103">LINE\_PROXYSTATUS message</span></span>

<span data-ttu-id="a5198-104">Die Meldung " **line \_ proxystatus** " wird gesendet, wenn sich die verfügbaren Proxys in einer Zeile ändern, die derzeit von der Anwendung geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="a5198-104">The **LINE\_PROXYSTATUS** message is sent when the available proxies change on a line that the application currently has open.</span></span>

<span data-ttu-id="a5198-105">Tapisrv generiert diese Nachricht während einer [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) -Funktion mithilfe von lineproxystatus \_ Open und lineproxystatus \_ allopenforacd oder einer [**lineclose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) -Funktion mithilfe von lineproxystatus \_ Close (alle [**lineproxystatus- \_ Konstanten**](lineproxystatus--constants.md)).</span><span class="sxs-lookup"><span data-stu-id="a5198-105">TAPISRV generates this message during a [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) function using LINEPROXYSTATUS\_OPEN and LINEPROXYSTATUS\_ALLOPENFORACD or a [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) function using LINEPROXYSTATUS\_CLOSE (all [**LINEPROXYSTATUS\_ Constants**](lineproxystatus--constants.md)).</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="a5198-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5198-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5198-107">*dwdevice*</span><span class="sxs-lookup"><span data-stu-id="a5198-107">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a5198-108">Das Handle der Anwendung für das liniengerät.</span><span class="sxs-lookup"><span data-stu-id="a5198-108">The application's handle to the line device.</span></span> <span data-ttu-id="a5198-109">Dies bezieht sich auf den-Agent-Handler.</span><span class="sxs-lookup"><span data-stu-id="a5198-109">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="a5198-110">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="a5198-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="a5198-111">Die beim Öffnen der Zeile angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="a5198-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="a5198-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="a5198-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="a5198-113">Gibt den Status der Warteschlange an, der geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="a5198-113">Specifies the queue status that has changed.</span></span> <span data-ttu-id="a5198-114">Kann eine oder mehrere der [**lineproxystatus- \_ Konstanten**](lineproxystatus--constants.md)sein.</span><span class="sxs-lookup"><span data-stu-id="a5198-114">Can be one or more of the [**LINEPROXYSTATUS\_ constants**](lineproxystatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5198-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="a5198-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="a5198-116">Wenn *dwParam1* auf lineproxystatus \_ Open oder lineproxystatus close festgelegt ist \_ , gibt *dwParam2* den zugehörigen Proxy Anforderungstyp an. Dies ist einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="a5198-116">If *dwParam1* is set to LINEPROXYSTATUS\_OPEN or LINEPROXYSTATUS\_CLOSE, *dwParam2* indicates the related proxy request type, which is one of the following:</span></span>

-   <span data-ttu-id="a5198-117">lineproxyrequest \_ setagentgroup</span><span class="sxs-lookup"><span data-stu-id="a5198-117">LINEPROXYREQUEST\_SETAGENTGROUP</span></span>
-   <span data-ttu-id="a5198-118">lineproxyrequest \_ setagentstate</span><span class="sxs-lookup"><span data-stu-id="a5198-118">LINEPROXYREQUEST\_SETAGENTSTATE</span></span>
-   <span data-ttu-id="a5198-119">lineproxyrequest \_ setagentactivity</span><span class="sxs-lookup"><span data-stu-id="a5198-119">LINEPROXYREQUEST\_SETAGENTACTIVITY</span></span>
-   <span data-ttu-id="a5198-120">lineproxyrequest \_ getagentcaps</span><span class="sxs-lookup"><span data-stu-id="a5198-120">LINEPROXYREQUEST\_GETAGENTCAPS</span></span>
-   <span data-ttu-id="a5198-121">lineproxyrequest \_ getagentstatus</span><span class="sxs-lookup"><span data-stu-id="a5198-121">LINEPROXYREQUEST\_GETAGENTSTATUS</span></span>
-   <span data-ttu-id="a5198-122">lineproxyrequest- \_ agentspezifisch</span><span class="sxs-lookup"><span data-stu-id="a5198-122">LINEPROXYREQUEST\_AGENTSPECIFIC</span></span>
-   <span data-ttu-id="a5198-123">lineproxyrequest \_ getagentactivitylist</span><span class="sxs-lookup"><span data-stu-id="a5198-123">LINEPROXYREQUEST\_GETAGENTACTIVITYLIST</span></span>
-   <span data-ttu-id="a5198-124">lineproxyrequest \_ getagentgrouplist</span><span class="sxs-lookup"><span data-stu-id="a5198-124">LINEPROXYREQUEST\_GETAGENTGROUPLIST</span></span>
-   <span data-ttu-id="a5198-125">lineproxyrequest- \_ kreateagent</span><span class="sxs-lookup"><span data-stu-id="a5198-125">LINEPROXYREQUEST\_CREATEAGENT</span></span>
-   <span data-ttu-id="a5198-126">lineproxyrequest \_ setagentmessrementperiod</span><span class="sxs-lookup"><span data-stu-id="a5198-126">LINEPROXYREQUEST\_SETAGENTMEASUREMENTPERIOD</span></span>
-   <span data-ttu-id="a5198-127">lineproxyrequest \_ getagentinfo</span><span class="sxs-lookup"><span data-stu-id="a5198-127">LINEPROXYREQUEST\_GETAGENTINFO</span></span>
-   <span data-ttu-id="a5198-128">lineproxyrequest- \_ Sitzung</span><span class="sxs-lookup"><span data-stu-id="a5198-128">LINEPROXYREQUEST\_CREATEAGENTSESSION</span></span>
-   <span data-ttu-id="a5198-129">lineproxyrequest \_ getagentsessionlist</span><span class="sxs-lookup"><span data-stu-id="a5198-129">LINEPROXYREQUEST\_GETAGENTSESSIONLIST</span></span>
-   <span data-ttu-id="a5198-130">lineproxyrequest \_ setagentsessionstate</span><span class="sxs-lookup"><span data-stu-id="a5198-130">LINEPROXYREQUEST\_SETAGENTSESSIONSTATE</span></span>
-   <span data-ttu-id="a5198-131">lineproxyrequest \_ getagentsessioninfo</span><span class="sxs-lookup"><span data-stu-id="a5198-131">LINEPROXYREQUEST\_GETAGENTSESSIONINFO</span></span>
-   <span data-ttu-id="a5198-132">lineproxyrequest \_ getqueuelist</span><span class="sxs-lookup"><span data-stu-id="a5198-132">LINEPROXYREQUEST\_GETQUEUELIST</span></span>
-   <span data-ttu-id="a5198-133">lineproxyrequest \_ setqueuemessrementperiod</span><span class="sxs-lookup"><span data-stu-id="a5198-133">LINEPROXYREQUEST\_SETQUEUEMEASUREMENTPERIOD</span></span>
-   <span data-ttu-id="a5198-134">lineproxyrequest \_ getqueueinfo</span><span class="sxs-lookup"><span data-stu-id="a5198-134">LINEPROXYREQUEST\_GETQUEUEINFO</span></span>
-   <span data-ttu-id="a5198-135">"lineproxyrequest" \_ getgrouplist</span><span class="sxs-lookup"><span data-stu-id="a5198-135">LINEPROXYREQUEST\_GETGROUPLIST</span></span>
-   <span data-ttu-id="a5198-136">lineproxyrequest \_ setagentstateex</span><span class="sxs-lookup"><span data-stu-id="a5198-136">LINEPROXYREQUEST\_SETAGENTSTATEEX</span></span>

<span data-ttu-id="a5198-137">Andernfalls ist *dwParam2* auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a5198-137">Otherwise, *dwParam2* is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a5198-138">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="a5198-138">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="a5198-139">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a5198-139">Reserved.</span></span> <span data-ttu-id="a5198-140">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="a5198-140">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5198-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5198-141">Requirements</span></span>



| <span data-ttu-id="a5198-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5198-142">Requirement</span></span> | <span data-ttu-id="a5198-143">Wert</span><span class="sxs-lookup"><span data-stu-id="a5198-143">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a5198-144">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="a5198-144">TAPI version</span></span><br/> | <span data-ttu-id="a5198-145">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="a5198-145">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="a5198-146">Header</span><span class="sxs-lookup"><span data-stu-id="a5198-146">Header</span></span><br/>       | <dl> <span data-ttu-id="a5198-147"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5198-147"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5198-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5198-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5198-149">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="a5198-149">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="a5198-150">**lineclose**</span><span class="sxs-lookup"><span data-stu-id="a5198-150">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="a5198-151">**\_linienproxyrequest**</span><span class="sxs-lookup"><span data-stu-id="a5198-151">**LINE\_PROXYREQUEST**</span></span>](line-proxyrequest.md)
</dt> <dt>

[<span data-ttu-id="a5198-152">**Lineproxyrequest- \_ Konstanten**</span><span class="sxs-lookup"><span data-stu-id="a5198-152">**LINEPROXYREQUEST\_ Constants**</span></span>](lineproxyrequest--constants.md)
</dt> </dl>

 

 





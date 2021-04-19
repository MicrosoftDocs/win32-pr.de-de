---
description: Die \_ Meldung "agentstatusex" wird gesendet, wenn sich der Status eines ACD-Agents in einem Agent-Handler ändert, für den die Anwendung zurzeit über eine geöffnete Zeile verfügt. Diese Meldung wird mithilfe der lineproxymess-Funktion generiert.
ms.assetid: a0709367-9105-43af-9772-0161d94c098a
title: LINE_AGENTSTATUSEX Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c9ff1a39fd6aacf69922693a54198426d267720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366817"
---
# <a name="line_agentstatusex-message"></a><span data-ttu-id="ee594-104">Zeile \_ agentstatusex-Meldung</span><span class="sxs-lookup"><span data-stu-id="ee594-104">LINE\_AGENTSTATUSEX message</span></span>

<span data-ttu-id="ee594-105">Die Meldung " **\_ agentstatusex** " wird gesendet, wenn sich der Status eines ACD-Agents in einem Agent-Handler ändert, für den die Anwendung zurzeit über eine geöffnete Zeile verfügt.</span><span class="sxs-lookup"><span data-stu-id="ee594-105">The **LINE\_AGENTSTATUSEX** message is sent when the status of an ACD agent changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="ee594-106">Diese Meldung wird mithilfe der [**lineproxymess**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) -Funktion generiert.</span><span class="sxs-lookup"><span data-stu-id="ee594-106">This message is generated using [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="ee594-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee594-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee594-108">*dwdevice*</span><span class="sxs-lookup"><span data-stu-id="ee594-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="ee594-109">Das Handle der Anwendung für das liniengerät.</span><span class="sxs-lookup"><span data-stu-id="ee594-109">The application's handle to the line device.</span></span> <span data-ttu-id="ee594-110">Dies bezieht sich auf den-Agent-Handler.</span><span class="sxs-lookup"><span data-stu-id="ee594-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="ee594-111">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="ee594-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="ee594-112">Die beim Öffnen der Zeile angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="ee594-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="ee594-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="ee594-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="ee594-114">Das Handle des Agents, dessen Status geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ee594-114">The handle of the agent whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="ee594-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="ee594-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="ee594-116">Gibt den Status der Warteschlange an, der geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ee594-116">Specifies the queue status that has changed.</span></span> <span data-ttu-id="ee594-117">Kann eine oder mehrere der [**linequeuestatus- \_ Konstanten**](linequeuestatus--constants.md)sein.</span><span class="sxs-lookup"><span data-stu-id="ee594-117">Can be one or more of the [**LINEQUEUESTATUS\_ constants**](linequeuestatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee594-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="ee594-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="ee594-119">Wenn *dwParam2* das Status Bit lineagentstatusex enthält \_ , gibt *dwParam3* den neuen Wert des Agentstatus an, der eine der [**lineagentstateex- \_ Konstanten**](lineagentstateex--constants.md)ist.</span><span class="sxs-lookup"><span data-stu-id="ee594-119">If *dwParam2* includes the LINEAGENTSTATUSEX \_STATE bit, *dwParam3* indicates the new value of the agent state, which is one of the [**LINEAGENTSTATEEX\_ constants**](lineagentstateex--constants.md).</span></span>

<span data-ttu-id="ee594-120">Andernfalls ist *dwParam3* auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ee594-120">Otherwise, *dwParam3* is set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee594-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee594-121">Requirements</span></span>



| <span data-ttu-id="ee594-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee594-122">Requirement</span></span> | <span data-ttu-id="ee594-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ee594-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ee594-124">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="ee594-124">TAPI version</span></span><br/> | <span data-ttu-id="ee594-125">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="ee594-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="ee594-126">Header</span><span class="sxs-lookup"><span data-stu-id="ee594-126">Header</span></span><br/>       | <dl> <span data-ttu-id="ee594-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee594-127"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee594-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee594-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee594-129">**linegetagentinfo**</span><span class="sxs-lookup"><span data-stu-id="ee594-129">**lineGetAgentInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)
</dt> <dt>

[<span data-ttu-id="ee594-130">**lineproxymess**</span><span class="sxs-lookup"><span data-stu-id="ee594-130">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 





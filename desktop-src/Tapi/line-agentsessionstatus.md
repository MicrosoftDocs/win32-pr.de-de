---
description: Die \_ Meldung "agentsessionstatus" wird gesendet, wenn sich der Status einer ACD-Agent-Sitzung auf einem Agent-Handler ändert, für den die Anwendung zurzeit eine offene Zeile aufweist. Diese Meldung wird mithilfe der lineproxymess-Funktion generiert.
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: LINE_AGENTSESSIONSTATUS Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d53c14290dfb6bda3889e7d2b87d8d3ca5e651c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368674"
---
# <a name="line_agentsessionstatus-message"></a><span data-ttu-id="67c10-104">Zeile \_ agentsessionstatus-Meldung</span><span class="sxs-lookup"><span data-stu-id="67c10-104">LINE\_AGENTSESSIONSTATUS message</span></span>

<span data-ttu-id="67c10-105">Die Meldung " **\_ agentsessionstatus** " wird gesendet, wenn sich der Status einer ACD-Agent-Sitzung auf einem Agent-Handler ändert, für den die Anwendung zurzeit eine offene Zeile aufweist.</span><span class="sxs-lookup"><span data-stu-id="67c10-105">The **LINE\_AGENTSESSIONSTATUS** message is sent when the status of an ACD agent session changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="67c10-106">Diese Meldung wird mithilfe der [**lineproxymess**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) -Funktion generiert.</span><span class="sxs-lookup"><span data-stu-id="67c10-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="67c10-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="67c10-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67c10-108">*dwdevice*</span><span class="sxs-lookup"><span data-stu-id="67c10-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="67c10-109">Das Handle der Anwendung für das liniengerät, für das sich der agentsitzungsstatus geändert hat.</span><span class="sxs-lookup"><span data-stu-id="67c10-109">The application's handle to the line device on which the agent session status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="67c10-110">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="67c10-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="67c10-111">Die beim Öffnen der Zeile angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="67c10-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="67c10-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="67c10-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="67c10-113">Ein Handle der Agentsitzung, deren Status sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="67c10-113">A handle of the agent session whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="67c10-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="67c10-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="67c10-115">Gibt den Agent-Sitzungs Status an, der geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="67c10-115">Specifies the agent session status that has changed.</span></span> <span data-ttu-id="67c10-116">Kann eine oder mehrere der **Zeilen \_ agentsessionstatus** sein.</span><span class="sxs-lookup"><span data-stu-id="67c10-116">Can be one or more of the **LINE\_AGENTSESSIONSTATUS**.</span></span>

</dd> <dt>

<span data-ttu-id="67c10-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="67c10-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="67c10-118">Wenn *dwParam2* das Status Bit lineagentstatusex enthält \_ , gibt *dwParam3* den neuen Wert des Agentstatus an, der eine der [**lineagentstateex- \_ Konstanten**](lineagentstateex--constants.md)ist.</span><span class="sxs-lookup"><span data-stu-id="67c10-118">If *dwParam2* includes the LINEAGENTSTATUSEX\_STATE bit, *dwParam3* indicates the new value of the agent state, which is one of the [**LINEAGENTSTATEEX\_ constants**](lineagentstateex--constants.md).</span></span>

<span data-ttu-id="67c10-119">Andernfalls ist *dwParam3* auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="67c10-119">Otherwise, *dwParam3* is set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67c10-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67c10-120">Requirements</span></span>



| <span data-ttu-id="67c10-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67c10-121">Requirement</span></span> | <span data-ttu-id="67c10-122">Wert</span><span class="sxs-lookup"><span data-stu-id="67c10-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="67c10-123">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="67c10-123">TAPI version</span></span><br/> | <span data-ttu-id="67c10-124">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="67c10-124">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="67c10-125">Header</span><span class="sxs-lookup"><span data-stu-id="67c10-125">Header</span></span><br/>       | <dl> <span data-ttu-id="67c10-126"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="67c10-126"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67c10-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67c10-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c10-128">**linegetagentsessioninfo**</span><span class="sxs-lookup"><span data-stu-id="67c10-128">**lineGetAgentSessionInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[<span data-ttu-id="67c10-129">**lineproxymess**</span><span class="sxs-lookup"><span data-stu-id="67c10-129">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 





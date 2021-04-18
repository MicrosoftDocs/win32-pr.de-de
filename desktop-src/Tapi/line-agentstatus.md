---
description: Die TAPI-Line- \_ agentstatusmeldung wird gesendet, wenn sich der Status eines ACD-Agents in einer von der Anwendung geöffneten Zeile ändert. Die Anwendung kann linegetagentstatus aufrufen, um den aktuellen Status des Agents zu ermitteln.
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: LINE_AGENTSTATUS Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b98242745e2f025f95cfe06fbe22c8956a02b0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365717"
---
# <a name="line_agentstatus-message"></a><span data-ttu-id="19989-104">Zeile \_ Agentstatus-Meldung</span><span class="sxs-lookup"><span data-stu-id="19989-104">LINE\_AGENTSTATUS message</span></span>

<span data-ttu-id="19989-105">Die TAPI- **line- \_ agentstatusmeldung** wird gesendet, wenn sich der Status eines ACD-Agents in einer von der Anwendung geöffneten Zeile ändert.</span><span class="sxs-lookup"><span data-stu-id="19989-105">The TAPI **LINE\_AGENTSTATUS** message is sent when the status of an ACD agent changes on a line the application currently has open.</span></span> <span data-ttu-id="19989-106">Die Anwendung kann [**linegetagentstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) aufrufen, um den aktuellen Status des Agents zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="19989-106">The application can invoke [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) to determine the current status of the agent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="19989-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="19989-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19989-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="19989-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="19989-109">Das Handle der Anwendung für das liniengerät, auf dem sich der Agentstatus geändert hat.</span><span class="sxs-lookup"><span data-stu-id="19989-109">The application's handle to the line device on which the agent status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="19989-110">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="19989-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="19989-111">Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="19989-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="19989-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="19989-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="19989-113">Der Bezeichner der Adresse in der Zeile, in der sich der Agentstatus geändert hat.</span><span class="sxs-lookup"><span data-stu-id="19989-113">Identifier of the address on the line on which the agent status changed.</span></span> <span data-ttu-id="19989-114">Ein Adress Bezeichner ist dauerhaft einer Adresse zugeordnet. der Bezeichner bleibt bei Betriebssystem Upgrades konstant.</span><span class="sxs-lookup"><span data-stu-id="19989-114">An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.</span></span>

</dd> <dt>

<span data-ttu-id="19989-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="19989-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="19989-116">Gibt den Agent-Status an, der geändert wurde. kann eine Kombination aus [**lineagentstatus- \_ Konstanten**](lineagentstatus--constants.md)sein.</span><span class="sxs-lookup"><span data-stu-id="19989-116">Specifies the agent status that has changed; can be a combination of [**LINEAGENTSTATUS\_ constants**](lineagentstatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="19989-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="19989-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="19989-118">Wenn *dwParam2* das Status Bit lineagentstatus enthält \_ , gibt *dwParam3* den neuen Wert des Elements **dwstate** in [**lineagentstatus**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)an.</span><span class="sxs-lookup"><span data-stu-id="19989-118">If *dwParam2* includes the LINEAGENTSTATUS\_STATE bit, then *dwParam3* indicates the new value of the **dwState** member in [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus).</span></span> <span data-ttu-id="19989-119">Andernfalls wird dieser Parameter auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19989-119">Otherwise, this parameter is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19989-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19989-120">Return value</span></span>

<span data-ttu-id="19989-121">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="19989-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19989-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19989-122">Remarks</span></span>

<span data-ttu-id="19989-123">Die **Zeile \_ Agentstatus** -Nachricht wird nicht an Anwendungen gesendet, die ältere Versionen von TAPI unterstützen.</span><span class="sxs-lookup"><span data-stu-id="19989-123">The **LINE\_AGENTSTATUS** message is not sent to applications that support older versions of TAPI.</span></span>

## <a name="requirements"></a><span data-ttu-id="19989-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19989-124">Requirements</span></span>



| <span data-ttu-id="19989-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19989-125">Requirement</span></span> | <span data-ttu-id="19989-126">Wert</span><span class="sxs-lookup"><span data-stu-id="19989-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="19989-127">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="19989-127">TAPI version</span></span><br/> | <span data-ttu-id="19989-128">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="19989-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="19989-129">Header</span><span class="sxs-lookup"><span data-stu-id="19989-129">Header</span></span><br/>       | <dl> <span data-ttu-id="19989-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="19989-130"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19989-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19989-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19989-132">**Lineagentstatus**</span><span class="sxs-lookup"><span data-stu-id="19989-132">**LINEAGENTSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[<span data-ttu-id="19989-133">**linegetagentstatus**</span><span class="sxs-lookup"><span data-stu-id="19989-133">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 





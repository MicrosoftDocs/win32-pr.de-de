---
description: Die TAPI-Zeilen- \_ agentspezifische Nachricht wird gesendet, wenn sich der Status eines ACD-Agents in einer Zeile ändert, die die Anwendung zurzeit geöffnet hat. Die Anwendung kann linegetagentstatus aufrufen, um den aktuellen Status des Agents zu ermitteln.
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: LINE_AGENTSPECIFIC Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ca03138ce00f11520e2e0f1df8e810e21d1186
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367734"
---
# <a name="line_agentspecific-message"></a><span data-ttu-id="ca5eb-104">LINE- \_ agentspezifische Nachricht</span><span class="sxs-lookup"><span data-stu-id="ca5eb-104">LINE\_AGENTSPECIFIC message</span></span>

<span data-ttu-id="ca5eb-105">Die TAPI- **Zeilen- \_ agentspezifische** Nachricht wird gesendet, wenn sich der Status eines ACD-Agents in einer Zeile ändert, die die Anwendung zurzeit geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="ca5eb-105">The TAPI **LINE\_AGENTSPECIFIC** message is sent when the status of an ACD agent changes on a line the application currently has open.</span></span> <span data-ttu-id="ca5eb-106">Die Anwendung kann [**linegetagentstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) aufrufen, um den aktuellen Status des Agents zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="ca5eb-106">The application can invoke [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) to determine the current status of the agent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="ca5eb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca5eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca5eb-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="ca5eb-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="ca5eb-109">Das Handle der Anwendung für das liniengerät.</span><span class="sxs-lookup"><span data-stu-id="ca5eb-109">The application's handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="ca5eb-110">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="ca5eb-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="ca5eb-111">Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="ca5eb-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="ca5eb-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="ca5eb-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="ca5eb-113">Der Index im Array von handlererweiterungsbezeichnerwerten in der [**lineagentcaps**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) -Struktur der Handlererweiterung, der die Nachricht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ca5eb-113">The index into the array of handler extension identifiers in the [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) structure of the handler extension with which the message is associated.</span></span>

</dd> <dt>

<span data-ttu-id="ca5eb-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="ca5eb-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="ca5eb-115">Spezifisch für die Handlererweiterung.</span><span class="sxs-lookup"><span data-stu-id="ca5eb-115">Specific to the handler extension.</span></span> <span data-ttu-id="ca5eb-116">Im Allgemeinen wird dieser Wert verwendet, um die Anwendung dazu zu veranlassen, eine [**lineagentspecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) -Funktion aufzurufen, um weitere Details zur Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ca5eb-116">Generally, this value is used to cause the application to invoke a [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) function to fetch further details about the message.</span></span>

</dd> <dt>

<span data-ttu-id="ca5eb-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="ca5eb-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="ca5eb-118">Spezifisch für die Handlererweiterung.</span><span class="sxs-lookup"><span data-stu-id="ca5eb-118">Specific to the handler extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca5eb-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca5eb-119">Return value</span></span>

<span data-ttu-id="ca5eb-120">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="ca5eb-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca5eb-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca5eb-121">Remarks</span></span>

<span data-ttu-id="ca5eb-122">Die **Zeile \_ agentspecific** -Nachricht wird nicht an Anwendungen gesendet, die ältere Versionen von TAPI unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ca5eb-122">The **LINE\_AGENTSPECIFIC** message is not sent to applications that support older versions of TAPI.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca5eb-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca5eb-123">Requirements</span></span>



| <span data-ttu-id="ca5eb-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca5eb-124">Requirement</span></span> | <span data-ttu-id="ca5eb-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ca5eb-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ca5eb-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="ca5eb-126">TAPI version</span></span><br/> | <span data-ttu-id="ca5eb-127">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ca5eb-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ca5eb-128">Header</span><span class="sxs-lookup"><span data-stu-id="ca5eb-128">Header</span></span><br/>       | <dl> <span data-ttu-id="ca5eb-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca5eb-129"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca5eb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca5eb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca5eb-131">**Lineagentcaps**</span><span class="sxs-lookup"><span data-stu-id="ca5eb-131">**LINEAGENTCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[<span data-ttu-id="ca5eb-132">**lineagentspecific**</span><span class="sxs-lookup"><span data-stu-id="ca5eb-132">**lineAgentSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[<span data-ttu-id="ca5eb-133">**linegetagentstatus**</span><span class="sxs-lookup"><span data-stu-id="ca5eb-133">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 





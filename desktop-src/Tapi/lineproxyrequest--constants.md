---
description: Diese Konstanten werden in zwei Kontexten verwendet.
ms.assetid: 5c05a567-cc65-411e-b049-919a442c5c57
title: LINEPROXYREQUEST_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba34a3a7f7b1f41f0c32783c4132afcfafef1aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354717"
---
# <a name="lineproxyrequest_-constants"></a><span data-ttu-id="e11bd-103">Lineproxyrequest- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="e11bd-103">LINEPROXYREQUEST\_ Constants</span></span>

<span data-ttu-id="e11bd-104">Diese Konstanten werden in zwei Kontexten verwendet.</span><span class="sxs-lookup"><span data-stu-id="e11bd-104">These constants are used in two contexts.</span></span> <span data-ttu-id="e11bd-105">Zuerst können Sie in einem Array von **DWORD** -Werten in der [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) -Struktur verwendet werden, die mit [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) übergeben wird, wenn die Option "lineopenoption" \_ angegeben wird, um anzugeben, welche Funktionen die Anwendung verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="e11bd-105">First, they can be used in an array of **DWORD** values in the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure passed in with [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) when the LINEOPENOPTION\_PROXY option is specified, to indicate which functions the application is willing to handle.</span></span> <span data-ttu-id="e11bd-106">Zweitens werden Sie in der [**Zeile \_ proxyrequest**](line-proxyrequest.md) verwendet, die von einer **line \_ proxyrequest** -Nachricht an die Handleranwendung übermittelt wird, um den Typ der zu verarbeitenden Anforderung und das Format der Daten im Puffer anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e11bd-106">Second, they are used in the [**LINE\_PROXYREQUEST**](line-proxyrequest.md) passed to the handler application by a **LINE\_PROXYREQUEST** message to indicate the type of request that is to be processed and the format of the data in the buffer.</span></span>

<dl> <dt>

<span data-ttu-id="e11bd-107"><span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**lineproxyrequest- \_ agentspezifisch**</span><span class="sxs-lookup"><span data-stu-id="e11bd-107"><span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**LINEPROXYREQUEST\_AGENTSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-108">Ist [**lineagentspecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e11bd-108">Associated with [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-109"><span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**lineproxyrequest- \_ kreateagent**</span><span class="sxs-lookup"><span data-stu-id="e11bd-109"><span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**LINEPROXYREQUEST\_CREATEAGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-110">Verknüpft mit [**linecreateagent**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta).</span><span class="sxs-lookup"><span data-stu-id="e11bd-110">Associated with [**lineCreateAgent**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-111"><span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**lineproxyrequest- \_ Sitzung**</span><span class="sxs-lookup"><span data-stu-id="e11bd-111"><span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**LINEPROXYREQUEST\_CREATEAGENTSESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-112">Verknüpft mit [**linecreateagentsession**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona).</span><span class="sxs-lookup"><span data-stu-id="e11bd-112">Associated with [**lineCreateAgentSession**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-113"><span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**lineproxyrequest \_ getagentactivitylist**</span><span class="sxs-lookup"><span data-stu-id="e11bd-113"><span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**LINEPROXYREQUEST\_GETAGENTACTIVITYLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-114">Ist [**linegetagentactivitylist**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e11bd-114">Associated with [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-115"><span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**lineproxyrequest \_ getagentcaps**</span><span class="sxs-lookup"><span data-stu-id="e11bd-115"><span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**LINEPROXYREQUEST\_GETAGENTCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-116">Mit [**linegetagentcaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)verknüpft.</span><span class="sxs-lookup"><span data-stu-id="e11bd-116">Associated with [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-117"><span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**lineproxyrequest \_ getagentgrouplist**</span><span class="sxs-lookup"><span data-stu-id="e11bd-117"><span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**LINEPROXYREQUEST\_GETAGENTGROUPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-118">Ist [**linegetagentgrouplist**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e11bd-118">Associated with [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-119"><span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**lineproxyrequest \_ getagentinfo**</span><span class="sxs-lookup"><span data-stu-id="e11bd-119"><span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**LINEPROXYREQUEST\_GETAGENTINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-120">Ist [**linegetagentinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e11bd-120">Associated with [**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-121"><span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**lineproxyrequest \_ getagentsessioninfo**</span><span class="sxs-lookup"><span data-stu-id="e11bd-121"><span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**LINEPROXYREQUEST\_GETAGENTSESSIONINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-122">Ist [**linegetagentsessioninfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e11bd-122">Associated with [**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-123"><span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**lineproxyrequest \_ getagentsessionlist**</span><span class="sxs-lookup"><span data-stu-id="e11bd-123"><span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**LINEPROXYREQUEST\_GETAGENTSESSIONLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-124">Ist [**linegetagentsessionlist**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e11bd-124">Associated with [**lineGetAgentSessionList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-125"><span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**lineproxyrequest \_ getagentstatus**</span><span class="sxs-lookup"><span data-stu-id="e11bd-125"><span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**LINEPROXYREQUEST\_GETAGENTSTATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-126">Ist [**linegetagentstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e11bd-126">Associated with [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-127"><span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**"lineproxyrequest" \_ getgrouplist**</span><span class="sxs-lookup"><span data-stu-id="e11bd-127"><span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**LINEPROXYREQUEST\_GETGROUPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-128">Ist [**linegetgrouplist**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e11bd-128">Associated with [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-129"><span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**lineproxyrequest \_ getqueueinfo**</span><span class="sxs-lookup"><span data-stu-id="e11bd-129"><span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**LINEPROXYREQUEST\_GETQUEUEINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-130">Ist [**linegetqueueinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e11bd-130">Associated with [**lineGetQueueInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-131"><span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**lineproxyrequest \_ getqueuelist**</span><span class="sxs-lookup"><span data-stu-id="e11bd-131"><span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**LINEPROXYREQUEST\_GETQUEUELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-132">[**Ist linegetqueuelist**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e11bd-132">Associated with [**lineGetQueueList**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-133"><span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**lineproxyrequest \_ setagentactivity**</span><span class="sxs-lookup"><span data-stu-id="e11bd-133"><span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**LINEPROXYREQUEST\_SETAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-134">Verknüpft mit [**linesetagentactivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).</span><span class="sxs-lookup"><span data-stu-id="e11bd-134">Associated with [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-135"><span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**lineproxyrequest \_ setagentgroup**</span><span class="sxs-lookup"><span data-stu-id="e11bd-135"><span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**LINEPROXYREQUEST\_SETAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-136">Verknüpft mit [**linesetagentgroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup).</span><span class="sxs-lookup"><span data-stu-id="e11bd-136">Associated with [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-137"><span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**lineproxyrequest \_ setagentmessrementperiod**</span><span class="sxs-lookup"><span data-stu-id="e11bd-137"><span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**LINEPROXYREQUEST\_SETAGENTMEASUREMENTPERIOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-138">Zugeordnet mit [**linesetagentmessrementperiod**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod).</span><span class="sxs-lookup"><span data-stu-id="e11bd-138">Associated with [**lineSetAgentMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-139"><span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**lineproxyrequest \_ setagentsessionstate**</span><span class="sxs-lookup"><span data-stu-id="e11bd-139"><span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**LINEPROXYREQUEST\_SETAGENTSESSIONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-140">Verknüpft mit [**linesetagentsessionstate**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate).</span><span class="sxs-lookup"><span data-stu-id="e11bd-140">Associated with [**lineSetAgentSessionState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-141"><span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**lineproxyrequest \_ setagentstate**</span><span class="sxs-lookup"><span data-stu-id="e11bd-141"><span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**LINEPROXYREQUEST\_SETAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-142">Verknüpft mit [**linesetagentstate**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate).</span><span class="sxs-lookup"><span data-stu-id="e11bd-142">Associated with [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-143"><span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**lineproxyrequest \_ setagentstateex**</span><span class="sxs-lookup"><span data-stu-id="e11bd-143"><span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**LINEPROXYREQUEST\_SETAGENTSTATEEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-144">Verknüpft mit [**linesetagentstateex**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex).</span><span class="sxs-lookup"><span data-stu-id="e11bd-144">Associated with [**lineSetAgentStateEx**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e11bd-145"><span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**lineproxyrequest \_ setqueuemessrementperiod**</span><span class="sxs-lookup"><span data-stu-id="e11bd-145"><span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**LINEPROXYREQUEST\_SETQUEUEMEASUREMENTPERIOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e11bd-146">Zugeordnet mit [**linesetqueuemessrementperiod**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod).</span><span class="sxs-lookup"><span data-stu-id="e11bd-146">Associated with [**lineSetQueueMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e11bd-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e11bd-147">Requirements</span></span>



| <span data-ttu-id="e11bd-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e11bd-148">Requirement</span></span> | <span data-ttu-id="e11bd-149">Wert</span><span class="sxs-lookup"><span data-stu-id="e11bd-149">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e11bd-150">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="e11bd-150">TAPI version</span></span><br/> | <span data-ttu-id="e11bd-151">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e11bd-151">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e11bd-152">Header</span><span class="sxs-lookup"><span data-stu-id="e11bd-152">Header</span></span><br/>       | <dl> <span data-ttu-id="e11bd-153"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e11bd-153"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e11bd-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e11bd-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e11bd-155">Callcenterkonstanten</span><span class="sxs-lookup"><span data-stu-id="e11bd-155">Call Center Constants</span></span>](call-center-constants.md)
</dt> <dt>

[<span data-ttu-id="e11bd-156">Callcenter-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e11bd-156">Call Center Functions</span></span>](call-center-functions.md)
</dt> </dl>

 

 





---
description: Qualifizierer enthalten Implementierungs spezifische Kontextinformationen und Transporteigenschaften, die definieren, wie der SNMP-Anbieter auf einen SNMP-Agent zugreift. Im folgenden werden die für den SNMP-Anbieter eindeutigen Qualifizierer aufgelistet.
ms.assetid: f2ac107c-e201-4670-96d1-883419787377
ms.tgt_platform: multiple
title: Spezifische Qualifizierer für den SNMP-Anbieter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: a1405cb4d9609380fdf35d6ce05a0fc9e1255ba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753673"
---
# <a name="qualifiers-specific-to-the-snmp-provider"></a><span data-ttu-id="8327e-104">Spezifische Qualifizierer für den SNMP-Anbieter</span><span class="sxs-lookup"><span data-stu-id="8327e-104">Qualifiers Specific to the SNMP Provider</span></span>

<span data-ttu-id="8327e-105">Qualifizierer enthalten Implementierungs spezifische Kontextinformationen und Transporteigenschaften, die definieren, wie der SNMP-Anbieter auf einen SNMP-Agent zugreift.</span><span class="sxs-lookup"><span data-stu-id="8327e-105">Qualifiers contain implementation-specific context information and transport properties that define how the SNMP Provider accesses an SNMP agent.</span></span> <span data-ttu-id="8327e-106">Im folgenden werden die für den SNMP-Anbieter eindeutigen Qualifizierer aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8327e-106">The following lists the qualifiers unique to the SNMP Provider.</span></span>

<dt>

<span data-ttu-id="8327e-107"><span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="8327e-107"><span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress**</span></span> 
</dt> <dd>

<span data-ttu-id="8327e-108">Datentyp: **CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8327e-108">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="8327e-109">Die dem SNMP-Agent zugeordnete Transport Adresse, z. b. eine IP-Adresse oder ein DNS-Name.</span><span class="sxs-lookup"><span data-stu-id="8327e-109">Transport address associated with the SNMP agent, such as an IP address or DNS name.</span></span> <span data-ttu-id="8327e-110">Sie sollten **AgentAddress** auf eine gültige unicasthostadresse oder einen Domänen Hostnamen festlegen, die über den Domänen Namen des Betriebssystems aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="8327e-110">You should set **AgentAddress** to a valid unicast host address or a domain host name that can be resolved through the operating system's domain-name resolution process.</span></span> <span data-ttu-id="8327e-111">**AgentAddress** hat keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="8327e-111">**AgentAddress** has no default value.</span></span>

</dd> <dt>

<span data-ttu-id="8327e-112"><span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**Agentflowcontrolwindowsize**</span><span class="sxs-lookup"><span data-stu-id="8327e-112"><span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize**</span></span> 
</dt> <dd>

<span data-ttu-id="8327e-113">Datentyp: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="8327e-113">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="8327e-114">Maximale Anzahl gleichzeitig ausstehender SNMP-Anforderungen, die an diesen Agent gesendet werden können, während eine Antwort noch nicht empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="8327e-114">Maximum number of concurrently outstanding SNMP requests that can be sent to this agent while a response has not yet been received.</span></span> <span data-ttu-id="8327e-115">Eine SNMP-Anforderung wird als ausstehend betrachtet, bis eine PDU-Antwort empfangen wurde oder ein Timeout aufgetreten ist. Eine große Fenstergröße verbessert in der Regel die Leistung, aber einige Agents funktionieren bei hoher Auslastung möglicherweise nicht gut.</span><span class="sxs-lookup"><span data-stu-id="8327e-115">An SNMP request is considered outstanding until a PDU response has been received or it has timed out. A large window size generally improves performance, but some agents might not work well under a heavy load.</span></span> <span data-ttu-id="8327e-116">**Agentflowcontrolwindowsize** kann auf 0 festgelegt werden, um eine unbegrenzte Fenstergröße oder eine Ganzzahl zwischen 1 und 2 ^ 32-1 anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8327e-116">**AgentFlowControlWindowSize** can be set to 0 to indicate an infinite window size or to an integer between 1 and 2^32-1.</span></span> <span data-ttu-id="8327e-117">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="8327e-117">The default value is 10.</span></span> <span data-ttu-id="8327e-118">Dieser Qualifizierer ist optional.</span><span class="sxs-lookup"><span data-stu-id="8327e-118">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8327e-119"><span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**Agentlesercommunityname**</span><span class="sxs-lookup"><span data-stu-id="8327e-119"><span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName**</span></span> 
</dt> <dd>

<span data-ttu-id="8327e-120">Datentyp: **CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8327e-120">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="8327e-121">Oktett-Zeichenfolge mit variabler Länge, die vom SNMP-Agent zum Authentifizieren einer SNMP-Protokolldaten Einheit (PDU) während eines Lesevorgangs (SNMP Get/Get Next Requests) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8327e-121">Variable-length octet string that is used by the SNMP agent to authenticate an SNMP Protocol Data Unit (PDU) during a read operation (SNMP GET/GET NEXT requests).</span></span> <span data-ttu-id="8327e-122">Der Communityname muss einer Unicode-Zeichenfolge zugeordnet werden und ist auf alphanumerische Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="8327e-122">The community name must be mapped to a Unicode string and is limited to alphanumeric characters.</span></span> <span data-ttu-id="8327e-123">Der Standardwert ist Public.</span><span class="sxs-lookup"><span data-stu-id="8327e-123">The default value is public.</span></span> <span data-ttu-id="8327e-124">Dieser Qualifizierer ist optional.</span><span class="sxs-lookup"><span data-stu-id="8327e-124">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8327e-125"><span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**Agentretrycount**</span><span class="sxs-lookup"><span data-stu-id="8327e-125"><span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount**</span></span> 
</dt> <dd>

<span data-ttu-id="8327e-126">Datentyp: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="8327e-126">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="8327e-127">Gibt an, wie oft eine einzelne SNMP-Anforderung erneut versucht werden kann, wenn keine Antwort vom SNMP-Agent vorliegt, bevor die Anforderung als fehlgeschlagen eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="8327e-127">Number of times a single SNMP request can be retried when there is no response from the SNMP agent before the request is deemed to have failed.</span></span> <span data-ttu-id="8327e-128">**Agentretrycount** muss auf eine ganze Zahl zwischen 0 und 2 ^ 32-1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8327e-128">**AgentRetryCount** must be set to an integer between 0 and 2^32-1.</span></span> <span data-ttu-id="8327e-129">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="8327e-129">The default value is 1.</span></span> <span data-ttu-id="8327e-130">Dieser Qualifizierer ist optional.</span><span class="sxs-lookup"><span data-stu-id="8327e-130">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8327e-131"><span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**Agentretrytimeout**</span><span class="sxs-lookup"><span data-stu-id="8327e-131"><span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout**</span></span> 
</dt> <dd>

<span data-ttu-id="8327e-132">Datentyp: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="8327e-132">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="8327e-133">Die Zeit in Millisekunden, bevor die SNMP-Protokolldaten Einheit (PDU) gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="8327e-133">Time in milliseconds before the SNMP Protocol Data Unit (PDU) is considered to have been dropped.</span></span> <span data-ttu-id="8327e-134">Dies ist die Anzahl von Millisekunden, die auf eine Antwort auf eine SNMP-Anforderung gewartet werden soll, die an den SNMP-Agent gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8327e-134">This is the number of milliseconds to wait for a response to an SNMP request sent to the SNMP agent.</span></span> <span data-ttu-id="8327e-135">**Agentretrytimeout** muss auf eine ganze Zahl zwischen 0 und 2 ^ 32-1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8327e-135">**AgentRetryTimeout** must be set to an integer between 0 and 2^32-1.</span></span> <span data-ttu-id="8327e-136">Der Standardwert ist 500.</span><span class="sxs-lookup"><span data-stu-id="8327e-136">The default value is 500.</span></span> <span data-ttu-id="8327e-137">Dieser Qualifizierer ist optional.</span><span class="sxs-lookup"><span data-stu-id="8327e-137">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8327e-138"><span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**Agentsnmpversion**</span><span class="sxs-lookup"><span data-stu-id="8327e-138"><span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion**</span></span> 
</dt> <dd>

<span data-ttu-id="8327e-139">Datentyp: **CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8327e-139">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="8327e-140">Die Version des SNMP-Protokolls, das bei der Kommunikation mit dem SNMP-Agent verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8327e-140">Version of the SNMP protocol to be used when communicating with the SNMP agent.</span></span> <span data-ttu-id="8327e-141">Derzeit sind die einzigen gültigen Werte 1 (für SNMPv1) und 2C (für SNMPv2C).</span><span class="sxs-lookup"><span data-stu-id="8327e-141">Currently, the only valid values are 1 (for SNMPv1) and 2C (for SNMPv2C).</span></span> <span data-ttu-id="8327e-142">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="8327e-142">The default value is 1.</span></span> <span data-ttu-id="8327e-143">Dieser Qualifizierer ist optional.</span><span class="sxs-lookup"><span data-stu-id="8327e-143">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8327e-144"><span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**Agenttransport**</span><span class="sxs-lookup"><span data-stu-id="8327e-144"><span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport**</span></span> 
</dt> <dd>

<span data-ttu-id="8327e-145">Datentyp: **CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8327e-145">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="8327e-146">Transport Protokoll, das für die Kommunikation mit dem SNMP-Agent verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8327e-146">Transport protocol used to communicate with the SNMP agent.</span></span> <span data-ttu-id="8327e-147">Zurzeit sind die einzigen gültigen Werte Internet Protocol (IP) und Internet Packet Exchange (IPX).</span><span class="sxs-lookup"><span data-stu-id="8327e-147">Currently the only valid values are Internet Protocol (IP) and Internet Packet Exchange (IPX).</span></span> <span data-ttu-id="8327e-148">Der Standardwert ist IP.</span><span class="sxs-lookup"><span data-stu-id="8327e-148">The default value is IP.</span></span> <span data-ttu-id="8327e-149">Dieser Qualifizierer ist optional.</span><span class="sxs-lookup"><span data-stu-id="8327e-149">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8327e-150"><span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**Agentvarbindsperpdu**</span><span class="sxs-lookup"><span data-stu-id="8327e-150"><span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu**</span></span> 
</dt> <dd>

<span data-ttu-id="8327e-151">Datentyp: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="8327e-151">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="8327e-152">Maximale Anzahl von Variablen Bindungen, die in einem einzelnen SNMP-PDU enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="8327e-152">Maximum number of variable bindings contained within a single SNMP PDU.</span></span> <span data-ttu-id="8327e-153">Jede SNMP-Anforderung, die an den SNMP-Agent gesendet wird, enthält mindestens eine SNMP-Variable.</span><span class="sxs-lookup"><span data-stu-id="8327e-153">Every SNMP request sent to the SNMP agent contains one or more SNMP variables.</span></span> <span data-ttu-id="8327e-154">Dieser Parameter gibt die größte Anzahl von Variablen an, die in einer einzelnen Anforderung enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="8327e-154">This parameter specifies the largest number of variables that can be included in a single request.</span></span> <span data-ttu-id="8327e-155">**Agentvarbindsperpdu** kann auf 0 (null) festgelegt werden, um zu bewirken, dass die Implementierung die optimalen Variablen Bindungen oder eine Ganzzahl zwischen 1 und 2 ^ 32-1 bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8327e-155">**AgentVarBindsPerPdu** can be set to 0 (zero) to cause the implementation to determine the optimal variable bindings or to an integer between 1 and 2^32-1.</span></span> <span data-ttu-id="8327e-156">Beachten Sie, dass bei einer Erhöhung dieses Werts die Leistung verbessert werden kann, einige Agents und Netzwerke jedoch nicht mit der resultierenden Anforderung umgehen können.</span><span class="sxs-lookup"><span data-stu-id="8327e-156">Note that while increasing this value can improve performance, some agents and networks cannot deal with the resulting request.</span></span> <span data-ttu-id="8327e-157">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="8327e-157">The default value is 10.</span></span> <span data-ttu-id="8327e-158">Dieser Qualifizierer ist optional.</span><span class="sxs-lookup"><span data-stu-id="8327e-158">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8327e-159"><span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**Agentschreitecommunityname**</span><span class="sxs-lookup"><span data-stu-id="8327e-159"><span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName**</span></span> 
</dt> <dd>

<span data-ttu-id="8327e-160">Datentyp: **CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8327e-160">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="8327e-161">Oktett-Zeichenfolge mit variabler Länge, die vom SNMP-Agent zum Authentifizieren einer SNMP-Protokolldaten Einheit (PDU) während eines Schreibvorgangs (SNMP-SET-Anforderung) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8327e-161">Variable-length octet string that is used by the SNMP agent to authenticate an SNMP Protocol Data Unit (PDU) during a write operation (SNMP SET request).</span></span> <span data-ttu-id="8327e-162">Der Communityname muss einer Unicode-Zeichenfolge zugeordnet werden und ist auf alphanumerische Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="8327e-162">The community name must be mapped to a Unicode string and is limited to alphanumeric characters.</span></span> <span data-ttu-id="8327e-163">Der Standardwert ist Public.</span><span class="sxs-lookup"><span data-stu-id="8327e-163">The default value is public.</span></span> <span data-ttu-id="8327e-164">Dieser Qualifizierer ist optional.</span><span class="sxs-lookup"><span data-stu-id="8327e-164">This qualifier is optional.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8327e-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8327e-165">Requirements</span></span>



| <span data-ttu-id="8327e-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8327e-166">Requirement</span></span> | <span data-ttu-id="8327e-167">Wert</span><span class="sxs-lookup"><span data-stu-id="8327e-167">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8327e-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8327e-168">Minimum supported client</span></span><br/> | <span data-ttu-id="8327e-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8327e-169">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8327e-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8327e-170">Minimum supported server</span></span><br/> | <span data-ttu-id="8327e-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8327e-171">Windows Server 2008</span></span><br/> |



 

 





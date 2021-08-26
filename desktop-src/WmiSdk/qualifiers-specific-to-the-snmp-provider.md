---
description: Qualifizierer enthalten implementierungsspezifische Kontextinformationen und Transporteigenschaften, die definieren, wie der SNMP-Anbieter auf einen SNMP-Agent zutritt. Im Folgenden werden die für den SNMP-Anbieter eindeutigen Qualifizierer aufgeführt.
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
ms.openlocfilehash: 3b05e2d6994bd0bee1a1f0e30287169c23b69ef574ba47fab1f3d8b5db5abedf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996090"
---
# <a name="qualifiers-specific-to-the-snmp-provider"></a>Spezifische Qualifizierer für den SNMP-Anbieter

Qualifizierer enthalten implementierungsspezifische Kontextinformationen und Transporteigenschaften, die definieren, wie der SNMP-Anbieter auf einen SNMP-Agent zutritt. Im Folgenden werden die für den SNMP-Anbieter eindeutigen Qualifizierer aufgeführt.

<dt>

<span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress** 
</dt> <dd>

Datentyp: **CIM \_ STRING**

Transportadresse, die dem SNMP-Agent zugeordnet ist, z. B. eine IP-Adresse oder ein DNS-Name. Sie sollten **AgentAddress auf eine** gültige Unicasthostadresse oder einen Domänenhostnamen festlegen, der über den Domänennamenauflösungsprozess des Betriebssystems aufgelöst werden kann. **AgentAddress hat** keinen Standardwert.

</dd> <dt>

<span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize** 
</dt> <dd>

Datentyp: **CIM \_ SINT32**

Maximale Anzahl gleichzeitig ausstehender SNMP-Anforderungen, die an diesen Agent gesendet werden können, während noch keine Antwort empfangen wurde. Eine SNMP-Anforderung gilt als ausstechend, bis eine PDU-Antwort empfangen wurde oder ein Time out erreicht wurde. Eine große Fenstergröße verbessert in der Regel die Leistung, aber einige Agents funktionieren bei einer hohen Auslastung möglicherweise nicht gut. **AgentFlowControlWindowSize** kann auf 0 festgelegt werden, um eine unendliche Fenstergröße anzugeben, oder auf eine ganze Zahl zwischen 1 und 2^32-1. Der Standardwert ist 10. Dieser Qualifizierer ist optional.

</dd> <dt>

<span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName** 
</dt> <dd>

Datentyp: **CIM \_ STRING**

Oktettzeichenfolge variabler Länge, die vom SNMP-Agent verwendet wird, um eine SNMP-Protokolldateneinheit (PDU) während eines Lesevorgang zu authentifizieren (SNMP GET/GET NEXT-Anforderungen). Der Communityname muss einer Unicode-Zeichenfolge zugeordnet werden und ist auf alphanumerische Zeichen beschränkt. Der Standardwert ist öffentlich. Dieser Qualifizierer ist optional.

</dd> <dt>

<span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount** 
</dt> <dd>

Datentyp: **CIM \_ SINT32**

Gibt an, wie oft eine einzelne SNMP-Anforderung wiederholt werden kann, wenn keine Antwort vom SNMP-Agent vor der Anforderung als fehlgeschlagen gilt. **AgentRetryCount muss** auf eine ganze Zahl zwischen 0 und 2^32-1 festgelegt werden. Der Standardwert ist 1. Dieser Qualifizierer ist optional.

</dd> <dt>

<span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout** 
</dt> <dd>

Datentyp: **CIM \_ SINT32**

Zeit in Millisekunden, bevor die SNMP-Protokolldateneinheit (PDU) als gelöscht betrachtet wird. Dies ist die Anzahl von Millisekunden, die auf eine Antwort auf eine an den SNMP-Agent gesendete SNMP-Anforderung gewartet werden soll. **AgentRetryTimeout** muss auf eine ganze Zahl zwischen 0 und 2^32-1 festgelegt werden. Der Standardwert ist 500. Dieser Qualifizierer ist optional.

</dd> <dt>

<span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion** 
</dt> <dd>

Datentyp: **CIM \_ STRING**

Version des SNMP-Protokolls, das bei der Kommunikation mit dem SNMP-Agent verwendet werden soll. Derzeit sind die einzigen gültigen Werte 1 (für SNMPv1) und 2C (für SNMPv2C). Der Standardwert ist 1. Dieser Qualifizierer ist optional.

</dd> <dt>

<span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport** 
</dt> <dd>

Datentyp: **CIM \_ STRING**

Transportprotokoll, das für die Kommunikation mit dem SNMP-Agent verwendet wird. Derzeit sind die einzigen gültigen Werte Internetprotokoll (IP) und Internet Packet Exchange (IPX). Der Standardwert ist IP. Dieser Qualifizierer ist optional.

</dd> <dt>

<span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu** 
</dt> <dd>

Datentyp: **CIM \_ SINT32**

Maximale Anzahl von Variablenbindungen, die in einem einzelnen SNMP-PDU enthalten sind. Jede SNMP-Anforderung, die an den SNMP-Agent gesendet wird, enthält mindestens eine SNMP-Variable. Dieser Parameter gibt die größte Anzahl von Variablen an, die in einer einzelnen Anforderung enthalten sein können. **AgentVarBindsPerPdu** kann auf 0 (null) festgelegt werden, damit die Implementierung die optimalen Variablenbindungen bestimmt, oder auf eine ganze Zahl zwischen 1 und 2^32-1. Beachten Sie, dass die Erhöhung dieses Werts zwar die Leistung verbessern kann, aber einige Agents und Netzwerke die resultierende Anforderung nicht behandeln können. Der Standardwert ist 10. Dieser Qualifizierer ist optional.

</dd> <dt>

<span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName** 
</dt> <dd>

Datentyp: **CIM \_ STRING**

Oktettzeichenfolge variabler Länge, die vom SNMP-Agent zum Authentifizieren einer SNMP-Protokolldateneinheit (PDU) während eines Schreibvorgang (SNMP SET-Anforderung) verwendet wird. Der Communityname muss einer Unicode-Zeichenfolge zugeordnet werden und ist auf alphanumerische Zeichen beschränkt. Der Standardwert ist öffentlich. Dieser Qualifizierer ist optional.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



 

 





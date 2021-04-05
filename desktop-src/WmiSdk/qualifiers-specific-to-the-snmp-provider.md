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
# <a name="qualifiers-specific-to-the-snmp-provider"></a>Spezifische Qualifizierer für den SNMP-Anbieter

Qualifizierer enthalten Implementierungs spezifische Kontextinformationen und Transporteigenschaften, die definieren, wie der SNMP-Anbieter auf einen SNMP-Agent zugreift. Im folgenden werden die für den SNMP-Anbieter eindeutigen Qualifizierer aufgelistet.

<dt>

<span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress** 
</dt> <dd>

Datentyp: **CIM- \_ Zeichenfolge**

Die dem SNMP-Agent zugeordnete Transport Adresse, z. b. eine IP-Adresse oder ein DNS-Name. Sie sollten **AgentAddress** auf eine gültige unicasthostadresse oder einen Domänen Hostnamen festlegen, die über den Domänen Namen des Betriebssystems aufgelöst werden kann. **AgentAddress** hat keinen Standardwert.

</dd> <dt>

<span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**Agentflowcontrolwindowsize** 
</dt> <dd>

Datentyp: **CIM \_ SINT32**

Maximale Anzahl gleichzeitig ausstehender SNMP-Anforderungen, die an diesen Agent gesendet werden können, während eine Antwort noch nicht empfangen wurde. Eine SNMP-Anforderung wird als ausstehend betrachtet, bis eine PDU-Antwort empfangen wurde oder ein Timeout aufgetreten ist. Eine große Fenstergröße verbessert in der Regel die Leistung, aber einige Agents funktionieren bei hoher Auslastung möglicherweise nicht gut. **Agentflowcontrolwindowsize** kann auf 0 festgelegt werden, um eine unbegrenzte Fenstergröße oder eine Ganzzahl zwischen 1 und 2 ^ 32-1 anzugeben. Der Standardwert ist 10. Dieser Qualifizierer ist optional.

</dd> <dt>

<span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**Agentlesercommunityname** 
</dt> <dd>

Datentyp: **CIM- \_ Zeichenfolge**

Oktett-Zeichenfolge mit variabler Länge, die vom SNMP-Agent zum Authentifizieren einer SNMP-Protokolldaten Einheit (PDU) während eines Lesevorgangs (SNMP Get/Get Next Requests) verwendet wird. Der Communityname muss einer Unicode-Zeichenfolge zugeordnet werden und ist auf alphanumerische Zeichen beschränkt. Der Standardwert ist Public. Dieser Qualifizierer ist optional.

</dd> <dt>

<span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**Agentretrycount** 
</dt> <dd>

Datentyp: **CIM \_ SINT32**

Gibt an, wie oft eine einzelne SNMP-Anforderung erneut versucht werden kann, wenn keine Antwort vom SNMP-Agent vorliegt, bevor die Anforderung als fehlgeschlagen eingestuft wird. **Agentretrycount** muss auf eine ganze Zahl zwischen 0 und 2 ^ 32-1 festgelegt werden. Der Standardwert ist 1. Dieser Qualifizierer ist optional.

</dd> <dt>

<span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**Agentretrytimeout** 
</dt> <dd>

Datentyp: **CIM \_ SINT32**

Die Zeit in Millisekunden, bevor die SNMP-Protokolldaten Einheit (PDU) gelöscht wird. Dies ist die Anzahl von Millisekunden, die auf eine Antwort auf eine SNMP-Anforderung gewartet werden soll, die an den SNMP-Agent gesendet wurde. **Agentretrytimeout** muss auf eine ganze Zahl zwischen 0 und 2 ^ 32-1 festgelegt werden. Der Standardwert ist 500. Dieser Qualifizierer ist optional.

</dd> <dt>

<span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**Agentsnmpversion** 
</dt> <dd>

Datentyp: **CIM- \_ Zeichenfolge**

Die Version des SNMP-Protokolls, das bei der Kommunikation mit dem SNMP-Agent verwendet werden soll. Derzeit sind die einzigen gültigen Werte 1 (für SNMPv1) und 2C (für SNMPv2C). Der Standardwert ist 1. Dieser Qualifizierer ist optional.

</dd> <dt>

<span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**Agenttransport** 
</dt> <dd>

Datentyp: **CIM- \_ Zeichenfolge**

Transport Protokoll, das für die Kommunikation mit dem SNMP-Agent verwendet wird. Zurzeit sind die einzigen gültigen Werte Internet Protocol (IP) und Internet Packet Exchange (IPX). Der Standardwert ist IP. Dieser Qualifizierer ist optional.

</dd> <dt>

<span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**Agentvarbindsperpdu** 
</dt> <dd>

Datentyp: **CIM \_ SINT32**

Maximale Anzahl von Variablen Bindungen, die in einem einzelnen SNMP-PDU enthalten sind. Jede SNMP-Anforderung, die an den SNMP-Agent gesendet wird, enthält mindestens eine SNMP-Variable. Dieser Parameter gibt die größte Anzahl von Variablen an, die in einer einzelnen Anforderung enthalten sein können. **Agentvarbindsperpdu** kann auf 0 (null) festgelegt werden, um zu bewirken, dass die Implementierung die optimalen Variablen Bindungen oder eine Ganzzahl zwischen 1 und 2 ^ 32-1 bestimmt. Beachten Sie, dass bei einer Erhöhung dieses Werts die Leistung verbessert werden kann, einige Agents und Netzwerke jedoch nicht mit der resultierenden Anforderung umgehen können. Der Standardwert ist 10. Dieser Qualifizierer ist optional.

</dd> <dt>

<span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**Agentschreitecommunityname** 
</dt> <dd>

Datentyp: **CIM- \_ Zeichenfolge**

Oktett-Zeichenfolge mit variabler Länge, die vom SNMP-Agent zum Authentifizieren einer SNMP-Protokolldaten Einheit (PDU) während eines Schreibvorgangs (SNMP-SET-Anforderung) verwendet wird. Der Communityname muss einer Unicode-Zeichenfolge zugeordnet werden und ist auf alphanumerische Zeichen beschränkt. Der Standardwert ist Public. Dieser Qualifizierer ist optional.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



 

 





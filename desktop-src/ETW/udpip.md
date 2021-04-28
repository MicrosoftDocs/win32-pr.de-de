---
description: 'UdpIp-Klasse: Diese Klasse ist die übergeordnete Klasse für UDP/IP-Ereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: UdpIp-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: d76aeb00ece18b026d9e5515a74ce830eb14af32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105388"
---
# <a name="udpip-class"></a>UdpIp-Klasse

Diese Klasse ist die übergeordnete Klasse für UDP/IP-Ereignisse.

Die folgende Syntax wird durch MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **UdpIp-Klasse** definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um UDP/IP-Ereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **FLAG EVENT TRACE FLAG NETWORK \_ \_ \_ \_ TCPIP** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an.

Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für UDP/IP-Ereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**UdpIpGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Netzwerkereignis (UDP/IP) bei der Nutzung von Ereignissen zu identifizieren.



| Ereignistyp                                                         | BESCHREIBUNG                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ RECEIVE**(Ereignistypwert ist 11)<br/> | Empfangsereignis für das IPv4-Protokoll. Die [**MOF-Klasse UdpIp \_ TypeGroup1**](udpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis. |
| **EVENT \_ TRACE \_ TYPE \_ SEND**(Ereignistypwert ist 10)<br/>    | Senden des Ereignisses für das IPv4-Protokoll. Die [**MOF-Klasse UdpIp \_ TypeGroup1**](udpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.    |
| Ereignistypwert, 17                                               | Fehlerereignis. Die [**UdpIp \_ Fail**](udpip-fail.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                  |
| Ereignistypwert, 26                                               | Senden eines Ereignisses für das IPv6-Protokoll. Die [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.    |
| Ereignistypwert, 27                                               | Empfangen des Ereignisses für das IPv6-Protokoll. Die [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. |



 

Sie können Netzwerkereignisse mithilfe der **ProcessId-Eigenschaft** zu einem Quell- und Zielprozess nachverfolgen. Da einige Netzwerkereignisse von separaten Threads protokolliert werden, können Sie die **ProcessId-** und **ThreadId-Member** von [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht verwenden, um den Prozess oder Thread zu identifizieren, von dem bzw. dem die Netzwerkaktivitäten stammen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_UdpIp-Fehler**](udpip-fail.md)
</dt> <dt>

[**UdpIp \_ TypeGroup1**](udpip-typegroup1.md)
</dt> <dt>

[**UdpIp \_ TypeGroup2**](udpip-typegroup2.md)
</dt> <dt>

[**UdpIp \_ V0**](udpip-v0.md)
</dt> <dt>

[**UdpIp \_ V1**](udpip-v1.md)
</dt> </dl>

 

 

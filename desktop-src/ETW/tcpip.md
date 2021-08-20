---
description: 'TcpIp-Klasse: Diese Klasse ist die übergeordnete Klasse für TCP/IP-Ereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.'
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: TcpIp-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0782db83d5c92a0e39578bc4e0d46e2c1d41432feb418a08bceb2e3548a45b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069520"
---
# <a name="tcpip-class"></a>TcpIp-Klasse

Diese Klasse ist die übergeordnete Klasse für TCP/IP-Ereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **TcpIp-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Um TCP/IP-Ereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie das **EVENT TRACE FLAG NETWORK \_ \_ \_ \_ TCPIP-Flag** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an, wenn Sie die [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) aufrufen.

Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für TCP/IP-Ereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**TcpIpGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Netzwerkereignis (TCP/IP) beim Nutzen von Ereignissen zu identifizieren.



| Ereignistyp                                                            | Beschreibung                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ ACCEPT**(Ereignistypwert ist 15)<br/>     | Accept-Ereignis für das IPv4-Protokoll. Die [**TCPIp \_ TypeGroup2**](tcpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                            |
| **EVENT \_ TRACE \_ TYPE \_ CONNECT**(Ereignistypwert ist 12)<br/>    | Verbinden Ereignis für das IPv4-Protokoll. Die [**TCPIp \_ TypeGroup2**](tcpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                           |
| **EVENT \_ TRACE \_ TYPE \_ DISCONNECT**(Ereignistypwert ist 13)<br/> | Ereignis "Trennen" für IPv4-Protokoll. Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                        |
| **EVENT \_ TRACE \_ TYPE \_ RECEIVE**(Ereignistypwert ist 11)<br/>    | Empfangen des Ereignisses für das IPv4-Protokoll. Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                           |
| **EVENT \_ TRACE \_ TYPE \_ RECONNECT**(Ereignistypwert ist 16)<br/>  | Ereignis zum Wiederherstellen der Verbindung für das IPv4-Protokoll. (Ein Verbindungsversuch ist fehlgeschlagen, und es wird ein weiterer Versuch unternommen.) Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis. |
| **EVENT \_ TRACE \_ TYPE \_ RETRANSMIT**(Ereignistypwert ist 14)<br/> | Ereignis für erneutes Übertragen für das IPv4-Protokoll. Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                        |
| **EVENT \_ TRACE \_ TYPE \_ SEND**(Ereignistypwert ist 10)<br/>       | Senden eines Ereignisses für das IPv4-Protokoll. Die [**TCPIP \_ SendIPV4**](tcpip-sendipv4.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                  |
| Ereignistypwert, 17                                                  | Fehlerereignis. Die [**MOF-Klasse TcpIp \_ Fail**](tcpip-fail.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                            |
| Ereignistypwert, 18                                                  | TCP-Kopierereignis für IPv4-Protokoll. Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                          |
| Ereignistypwert, 26                                                  | Senden eines Ereignisses für das IPv6-Protokoll. Die [**\_ TCPIP SendIPV6**](tcpip-sendipv6.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                  |
| Ereignistypwert, 27                                                  | Empfangen des Ereignisses für das IPv6-Protokoll. Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                           |
| Ereignistypwert, 28                                                  | Verbinden Ereignis für das IPv6-Protokoll. Die [**TCPIp \_ TypeGroup4**](tcpip-typegroup4.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                           |
| Ereignistypwert, 29                                                  | Disconnect-Ereignis für IPv6-Protokoll. Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                        |
| Ereignistypwert, 30                                                  | Ereignis für erneutes Übertragen für das IPv6-Protokoll. Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                        |
| Ereignistypwert, 31                                                  | Accept-Ereignis für IPv6-Protokoll. Die [**TCPIp \_ TypeGroup4**](tcpip-typegroup4.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                            |
| Ereignistypwert, 32                                                  | Ereignis zum Wiederherstellen der Verbindung für das IPv6-Protokoll. (Ein Verbindungsversuch ist fehlgeschlagen, und es wird ein weiterer Versuch unternommen.) Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. |
| Ereignistypwert, 34                                                  | TCP-Kopierereignis für das IPv6-Protokoll. Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                          |



 

Sie können Netzwerkereignisse mithilfe der **ProcessId-Eigenschaft** zu einem Quell- und Zielprozess nachverfolgen. Da einige Netzwerkereignisse von separaten Threads protokolliert werden, können Sie die **ProcessId-** und **ThreadId-Member** von [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht verwenden, um den Prozess oder Thread zu identifizieren, von dem bzw. dem die Netzwerkaktivitäten stammen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_TcpIp-Fehler**](tcpip-fail.md)
</dt> <dt>

[**TcpIp \_ SendIPV4**](tcpip-sendipv4.md)
</dt> <dt>

[**TcpIp \_ SendIPV6**](tcpip-sendipv6.md)
</dt> <dt>

[**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md)
</dt> <dt>

[**TcpIp \_ TypeGroup2**](tcpip-typegroup2.md)
</dt> <dt>

[**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md)
</dt> <dt>

[**TcpIp \_ TypeGroup4**](tcpip-typegroup4.md)
</dt> <dt>

[**TcpIp \_ V0**](tcpip-v0.md)
</dt> <dt>

[**TcpIp \_ V1**](tcpip-v1.md)
</dt> </dl>

 

 

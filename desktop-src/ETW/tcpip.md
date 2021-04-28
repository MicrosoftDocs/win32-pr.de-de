---
description: 'TcpIp-Klasse: Diese Klasse ist die übergeordnete Klasse für TCP/IP-Ereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
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
ms.openlocfilehash: abcd805b417451adf2122e7baf3310be101a35ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105728"
---
# <a name="tcpip-class"></a>TcpIp-Klasse

Diese Klasse ist die übergeordnete Klasse für TCP/IP-Ereignisse.

Die folgende Syntax wird aus MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **TcpIp-Klasse** definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um TCP/IP-Ereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie das **EVENT TRACE FLAG NETWORK \_ \_ \_ \_ TCPIP-Flag** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an, wenn Sie die [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) aufrufen.

Consumer der Ereignisablaufverfolgung können eine spezielle Verarbeitung für TCP/IP-Ereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**TcpIpGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Netzwerkereignis (TCP/IP) beim Nutzen von Ereignissen zu identifizieren.



| Ereignistyp                                                            | BESCHREIBUNG                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ ACCEPT**(Ereignistypwert ist 15)<br/>     | Accept-Ereignis für IPv4-Protokoll. Die [**TCPIp \_ TypeGroup2**](tcpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                            |
| **EVENT \_ TRACE \_ TYPE \_ CONNECT**(Ereignistypwert ist 12)<br/>    | Connect-Ereignis für IPv4-Protokoll. Die [**TCPIp \_ TypeGroup2**](tcpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                           |
| **EVENT \_ TRACE \_ TYPE \_ DISCONNECT**(Ereignistypwert ist 13)<br/> | Disconnect-Ereignis für IPv4-Protokoll. Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                        |
| **EVENT \_ TRACE \_ TYPE \_ RECEIVE**(Ereignistypwert ist 11)<br/>    | Empfangsereignis für das IPv4-Protokoll. Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                           |
| **EVENT \_ TRACE \_ TYPE \_ RECONNECT**(Ereignistypwert ist 16)<br/>  | Verbindungsereignis für das IPv4-Protokoll wiederherstellen. (Ein Verbindungsversuch ist fehlgeschlagen, und es wird ein weiterer Versuch unternommen.) Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis. |
| **EVENT \_ TRACE \_ TYPE \_ RETRANSMIT**(Ereignistypwert ist 14)<br/> | Retransmit-Ereignis für das IPv4-Protokoll. Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                        |
| **EVENT \_ TRACE \_ TYPE \_ SEND**(Ereignistypwert ist 10)<br/>       | Senden des Ereignisses für das IPv4-Protokoll. Die [**MOF-Klasse TcpIp \_ SendIPV4**](tcpip-sendipv4.md) definiert die Ereignisdaten für dieses Ereignis.                                                                  |
| Ereignistypwert, 17                                                  | Fehlerereignis. Die [**TCPIp \_ Fail**](tcpip-fail.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                            |
| Ereignistypwert, 18                                                  | TCP-Kopierereignis für das IPv4-Protokoll. Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                          |
| Ereignistypwert, 26                                                  | Senden eines Ereignisses für das IPv6-Protokoll. Die [**MOF-Klasse TcpIp \_ SendIPV6**](tcpip-sendipv6.md) definiert die Ereignisdaten für dieses Ereignis.                                                                  |
| Ereignistypwert, 27                                                  | Empfangen des Ereignisses für das IPv6-Protokoll. Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                           |
| Ereignistypwert, 28                                                  | Connect-Ereignis für IPv6-Protokoll. Die [**TCPIp \_ TypeGroup4**](tcpip-typegroup4.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                           |
| Ereignistypwert, 29                                                  | Disconnect-Ereignis für IPv6-Protokoll. Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                        |
| Ereignistypwert, 30                                                  | Ereignis für erneutes Übertragen für das IPv6-Protokoll. Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                        |
| Ereignistypwert, 31                                                  | Accept-Ereignis für das IPv6-Protokoll. Die [**TCPIp \_ TypeGroup4**](tcpip-typegroup4.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                            |
| Ereignistypwert, 32                                                  | Ereignis zum Wiederherstellen der Verbindung für das IPv6-Protokoll. (Ein Verbindungsversuch ist fehlgeschlagen, und es wird ein weiterer Versuch unternommen.) Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. |
| Ereignistypwert, 34                                                  | TCP-Kopierereignis für das IPv6-Protokoll. Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                          |



 

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

 

 

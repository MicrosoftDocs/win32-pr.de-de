---
description: Diese Klasse ist die übergeordnete Klasse für TCP/IP-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: Tcpip-Klasse
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
ms.openlocfilehash: 6488ece2fd8df0670455ceea25560835c352b83e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978225"
---
# <a name="tcpip-class"></a>Tcpip-Klasse

Diese Klasse ist die übergeordnete Klasse für TCP/IP-Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **tcpip** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um TCP/IP-Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das **ereignisablaufverfolgungsflag \_ \_ \_ Network \_ tcpip** in dem **enableflags** -Member einer [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) -Struktur beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion an.

Ereignis Ablauf Verfolgungs Consumer können eine spezielle Verarbeitung für TCP/IP-Ereignisse implementieren, indem Sie die Funktion [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**tcpipguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben. Verwenden Sie die folgenden Ereignis Typen, um beim Verarbeiten von Ereignissen das tatsächliche Netzwerk (TCP/IP)-Ereignis zu identifizieren.



| Ereignistyp                                                            | BESCHREIBUNG                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ Annahme**(Ereignistyp Wert ist 15)<br/>     | Akzeptieren Sie das Ereignis für das IPv4-Protokoll. Die [**tcpip \_ TypeGroup2**](tcpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                            |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ Connect**(Ereignistyp Wert ist 12)<br/>    | Connect-Ereignis für IPv4-Protokoll. Die [**tcpip \_ TypeGroup2**](tcpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                           |
| **Ereignis \_ Ablauf Verfolgungs \_ Typen \_ Trennung**(Ereignistyp Wert ist 13)<br/> | Disconnect-Ereignis für IPv4-Protokoll. Die [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                        |
| **Ereignis \_ \_ \_ Empfang von Ablauf Verfolgungs Typen**(Ereignistyp Wert ist 11)<br/>    | Receive-Ereignis für IPv4-Protokoll. Die [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                           |
| **Ereignis \_ \_ \_ Reconnect** für Ablaufverfolgungstyp (Ereignistyp Wert ist 16)<br/>  | Reconnect-Ereignis für IPv4-Protokoll. (Ein Verbindungsversuch ist fehlgeschlagen, und es wird ein weiterer Versuch unternommen.) Die [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. |
| **Ereignis \_ \_Erneute über \_ Tragung von Ablauf Verfolgungs Typen**(Ereignistyp Wert ist 14)<br/> | Das Ereignis für das IPv4-Protokoll wird erneut übertragen. Die [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                        |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ senden**(Ereignistyp Wert ist 10)<br/>       | Sende Ereignis für IPv4-Protokoll. Die [**tcpip \_ SendIPV4**](tcpip-sendipv4.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                  |
| Ereignistyp Wert, 17                                                  | Fehler Ereignis. Die [**tcpip \_ Fail**](tcpip-fail.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                            |
| Ereignistyp Wert, 18                                                  | TCP-Kopier Ereignis für IPv4-Protokoll. Die [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                          |
| Ereignistyp Wert, 26                                                  | Sende Ereignis für IPv6-Protokoll. Die [**tcpip \_ SendIPV6**](tcpip-sendipv6.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                  |
| Ereignistyp Wert, 27                                                  | Receive-Ereignis für IPv6-Protokoll. Die [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                           |
| Ereignistyp Wert, 28                                                  | Connect-Ereignis für IPv6-Protokoll. Die [**tcpip \_ TypeGroup4**](tcpip-typegroup4.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                           |
| Ereignistyp Wert, 29                                                  | Disconnect-Ereignis für IPv6-Protokoll. Die [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                        |
| Ereignistyp Wert, 30                                                  | Das Ereignis für das IPv6-Protokoll wird erneut übertragen. Die [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                        |
| Ereignistyp Wert, 31                                                  | Akzeptieren Sie das Ereignis für das IPv6-Protokoll. Die [**tcpip \_ TypeGroup4**](tcpip-typegroup4.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                            |
| Ereignistyp Wert, 32                                                  | Reconnect-Ereignis für IPv6-Protokoll. (Ein Verbindungsversuch ist fehlgeschlagen, und es wird ein weiterer Versuch unternommen.) Die [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. |
| Ereignistyp Wert, 34                                                  | TCP-Kopier Ereignis für IPv6-Protokoll. Die [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                          |



 

Sie können Netzwerkereignisse mithilfe der **ProcessID-** Eigenschaft an einen Quell-und Ziel Prozess überführen. Da einige Netzwerkereignisse von separaten Threads protokolliert werden, können Sie die **ProcessID** -und **ThreadId** -Member des [**Ereignis Ablauf \_ Verfolgungs \_ Headers**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) nicht verwenden, um den Prozess oder den Thread zu identifizieren, der die Netzwerkaktivitäten ausgelöst hat.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ systemtrace**](msnt-systemtrace.md)
</dt> <dt>

[**Tcpip \_ schlägt fehl**](tcpip-fail.md)
</dt> <dt>

[**Tcpip \_ SendIPV4**](tcpip-sendipv4.md)
</dt> <dt>

[**Tcpip \_ SendIPV6**](tcpip-sendipv6.md)
</dt> <dt>

[**Tcpip \_ TypeGroup1**](tcpip-typegroup1.md)
</dt> <dt>

[**Tcpip \_ TypeGroup2**](tcpip-typegroup2.md)
</dt> <dt>

[**Tcpip \_ TypeGroup3**](tcpip-typegroup3.md)
</dt> <dt>

[**Tcpip \_ TypeGroup4**](tcpip-typegroup4.md)
</dt> <dt>

[**Tcpip \_ v0**](tcpip-v0.md)
</dt> <dt>

[**Tcpip \_ v1**](tcpip-v1.md)
</dt> </dl>

 

 

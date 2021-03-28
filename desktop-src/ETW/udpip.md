---
description: Diese Klasse ist die übergeordnete Klasse für UDP/IP-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: Udpip-Klasse
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
ms.openlocfilehash: 5116b5f97a4aa7e3bafa9da1c1208ce7ee9d5794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527287"
---
# <a name="udpip-class"></a>Udpip-Klasse

Diese Klasse ist die übergeordnete Klasse für UDP/IP-Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **udpip** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um UDP/IP-Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das Flag für das **ereignisablaufverfolgungsflag \_ \_ \_ Network \_ tcpip** im **enableflags** -Member einer [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) -Struktur beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion

Ereignisablaufverfolgungsconsumer können eine spezielle Verarbeitung für UDP/IP-Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**udpipguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben. Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Netzwerk Ereignis (UDP/IP) beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp                                                         | BESCHREIBUNG                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **Ereignis \_ \_ \_ Empfang von Ablauf Verfolgungs Typen**(Ereignistyp Wert ist 11)<br/> | Receive-Ereignis für IPv4-Protokoll. Die [**udpip \_ TypeGroup1**](udpip-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ senden**(Ereignistyp Wert ist 10)<br/>    | Sende Ereignis für IPv4-Protokoll. Die [**udpip \_ TypeGroup1**](udpip-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.    |
| Ereignistyp Wert, 17                                               | Fehler Ereignis. Die [**udpip \_**](udpip-fail.md) -MOF-Klasse "Fail" definiert die Ereignisdaten für dieses Ereignis.                                  |
| Ereignistyp Wert, 26                                               | Sende Ereignis für IPv6-Protokoll. Die [**udpip \_ TypeGroup2**](udpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.    |
| Ereignistyp Wert, 27                                               | Receive-Ereignis für IPv6-Protokoll. Die [**udpip \_ TypeGroup2**](udpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. |



 

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

[**Udpip \_ schlägt fehl**](udpip-fail.md)
</dt> <dt>

[**Udpip \_ TypeGroup1**](udpip-typegroup1.md)
</dt> <dt>

[**Udpip \_ TypeGroup2**](udpip-typegroup2.md)
</dt> <dt>

[**Udpip \_ v0**](udpip-v0.md)
</dt> <dt>

[**Udpip \_ v1**](udpip-v1.md)
</dt> </dl>

 

 

---
description: 'Process_V2-Klasse: Diese Klasse ist die übergeordnete Klasse für Prozessereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.'
ms.assetid: 75596278-43cc-4040-a43d-6958d0935b68
title: Process_V2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8b5ac8c1e8dd09b8f3a1078abde39523487afbe901d1e3013eade82170e4af11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069940"
---
# <a name="process_v2-class"></a>Process \_ V2-Klasse

Diese Klasse ist die übergeordnete Klasse für Prozessereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Process_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **Process-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Um Prozessereignisse in einer NT Kernel-Protokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **EVENT TRACE FLAG \_ \_ \_ PROCESS-Flag** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an. Sie können auch das folgende Flag angeben:

-   **\_ \_ \_ \_ EREIGNISABLAUFVERFOLGUNGSFLAG-PROZESSINDIKATOREN**

Consumer der Ereignisablaufverfolgung können eine spezielle Verarbeitung für Prozessereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**ProcessGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Prozessereignis beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp                                                      | Beschreibung                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ END**(Ereignistypwert ist 2)<br/>   | Endprozessereignis. Die [**Process \_ TypeGroup1**](process-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                          |
| **EVENT \_ TRACE \_ TYPE \_ START**(Ereignistypwert ist 1)<br/> | Startprozessereignis. Die [**Process \_ TypeGroup1**](process-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                        |
| Ereignistypwert, 3                                             | Ereignis zum Starten des Datensammlungsprozesses. Listet Prozesse auf, die derzeit zum Start der Kernelsitzung ausgeführt werden. Die [**Process \_ TypeGroup1**](process-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. |
| Ereignistypwert, 4                                             | Ereignis zum Beenden des Datensammlungsprozesses. Listet Prozesse auf, die derzeit zum Zeitpunkt des Beendens der Kernelsitzung ausgeführt werden. Die [**Process \_ TypeGroup1**](process-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.     |
| Ereignistypwert, 32                                            | Leistungsindikatorereignis. Die [**Process \_ V2 \_ TypeGroup2**](process-v2-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                          |
| Ereignistypwert, 33                                            | Rundown der Leistungsindikatoren zu Beginn der Sitzung. Die [**Process \_ V2 \_ TypeGroup2**](process-v2-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                     |
| Ereignistypwert, 39                                            | Das Ereignis für den außer Kraftsetzen des Prozesses. Die [**Process \_ TypeGroup1**](process-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                      |



 

Prozess- und Threadstartereignisse können im Kontext des übergeordneten Prozesses oder Threads protokolliert werden. Daher entsprechen die **ProcessId-** und **ThreadId-Member** von [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht dem Prozess und Thread, der erstellt wird. Aus diesem Grund enthalten diese Ereignisse die Prozess- und Threadbezeichner in den Ereignisdaten (zusätzlich zu denen im Ereignisheader).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Prozess**](process.md)
</dt> <dt>

[**Process \_ TypeGroup1**](process-typegroup1.md)
</dt> <dt>

[**Verarbeiten \_ von V0**](process-v0.md)
</dt> <dt>

[**Verarbeiten \_ von V1**](process-v1.md)
</dt> </dl>

 

 

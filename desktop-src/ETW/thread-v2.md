---
description: 'Thread_V2 Klasse: Diese Klasse ist die übergeordnete Klasse für Threadereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.'
ms.assetid: 63e52cba-42a5-44f0-8eb6-e1bac8414a83
title: Thread_V2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: d057f80d5cf29f6660ee3a2ebd651c468496529a56a11147225ebd504451184c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069390"
---
# <a name="thread_v2-class"></a>Thread \_ V2-Klasse

Diese Klasse ist die übergeordnete Klasse für Threadereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Thread_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **Thread \_ V2-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Um Threadereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **FLAG EVENT TRACE FLAG \_ \_ \_ THREAD** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an. Sie können auch die folgenden Flags angeben:

-   **\_ \_ EREIGNIS-ABLAUFVERFOLGUNGSFLAG \_ CSWITCH**
-   **\_ \_ EREIGNISVERFOLGUNGSFLAG \_ DISPATCHER**

Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für Threadereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**ThreadGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Threadereignis beim Verwenden von Ereignissen zu identifizieren.



| Ereignistyp                                                      | Beschreibung                                                                                                                                                                                                                          |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ END**(Ereignistypwert ist 2)<br/>   | Endthreadereignis. Die [**\_ MOF-Klasse Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                        |
| **EVENT \_ TRACE \_ TYPE \_ START**(Ereignistypwert ist 1)<br/> | Threadereignis starten. Die [**\_ MOF-Klasse Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                      |
| Ereignistypwert, 3                                             | Starten des Datensammlungsthread-Ereignisses. Aufzählen von Threads, die derzeit zum Zeitpunkt des Starts der Kernelsitzung ausgeführt werden. Die [**\_ MOF-Klasse Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis. |
| Ereignistypwert, 4                                             | Enddatensammlungsthreadereignis. Aufzählen von Threads, die derzeit zum Zeitpunkt des Beendens der Kernelsitzung ausgeführt werden. Die [**\_ MOF-Klasse Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.     |
| Ereignistypwert, 36                                            | Kontextwechselereignis. Die [**MOF-Klasse CSwitch**](cswitch.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                |
| Ereignistypwert, 50                                            | Ready-Threadereignis. Die [](readythread.md) ReadyThread-MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                          |



 

Prozess- und Threadstartereignisse können im Kontext des übergeordneten Prozesses oder Threads protokolliert werden. Daher entsprechen die **ProcessId-** und **ThreadId-Member** von [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht dem Prozess und Thread, der erstellt wird. Aus diesem Grund enthalten diese Ereignisse die Prozess- und Threadbezeichner in den Ereignisdaten (zusätzlich zu den im Ereignisheader).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**CSwitch**](cswitch.md)
</dt> <dt>

[**Thread**](thread.md)
</dt> <dt>

[**Thread \_ TypeGroup1**](thread-typegroup1.md)
</dt> <dt>

[**Thread \_ V0**](thread-v0.md)
</dt> <dt>

[**Thread \_ V1**](thread-v1.md)
</dt> </dl>

 

 

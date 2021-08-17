---
description: 'Prozessklasse: Diese Klasse ist die übergeordnete Klasse für Prozessereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.'
ms.assetid: a505c693-2169-499b-bd32-42fa9bd69d2f
title: Process-Klasse
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
ms.openlocfilehash: 25c21e5f301d88f3790900c70873d9485161f5041d28bb1a30f3bb85082a9bd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069900"
---
# <a name="process-class"></a>Process-Klasse

Diese Klasse ist die übergeordnete Klasse für Prozessereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Process : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **Process-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Um Prozessereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **FLAG EVENT TRACE FLAG \_ \_ \_ PROCESS** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an. Sie können auch das folgende Flag angeben:

-   **PROZESSINDIKATOREN \_ FÜR \_ EREIGNIS-ABLAUFVERFOLGUNGSFLAGS \_ \_**

Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für Prozessereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**ProcessGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Prozessereignis beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp                                                      | Beschreibung                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ END**(Ereignistypwert ist 2)<br/>   | Endprozessereignis. Die [**\_ MOF-Klasse Process TypeGroup1**](process-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                          |
| **EVENT \_ TRACE \_ TYPE \_ START**(Ereignistypwert ist 1)<br/> | Startprozessereignis. Die [**\_ MOF-Klasse Process TypeGroup1**](process-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                        |
| Ereignistypwert, 3                                             | Ereignis zum Starten des Datensammlungsprozesses. Aufzählen von Prozessen, die derzeit zum Zeitpunkt des Starts der Kernelsitzung ausgeführt werden. Die [**\_ MOF-Klasse Process TypeGroup1**](process-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis. |
| Ereignistypwert, 4                                             | Beenden des Datensammlungsprozess-Ereignisses. Aufzählen von Prozessen, die derzeit zum Zeitpunkt des Beendens der Kernelsitzung ausgeführt werden. Die [**\_ MOF-Klasse Process TypeGroup1**](process-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.     |



 

Prozess- und Threadstartereignisse können im Kontext des übergeordneten Prozesses oder Threads protokolliert werden. Daher entsprechen die **ProcessId-** und **ThreadId-Member** von [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht dem Prozess und Thread, der erstellt wird. Aus diesem Grund enthalten diese Ereignisse die Prozess- und Threadbezeichner in den Ereignisdaten (zusätzlich zu den im Ereignisheader).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Process \_ TypeGroup1**](process-typegroup1.md)
</dt> <dt>

[**Verarbeiten \_ von V0**](process-v0.md)
</dt> <dt>

[**Prozess \_ V1**](process-v1.md)
</dt> <dt>

[**Prozess \_ V2**](process-v2.md)
</dt> </dl>

 

 

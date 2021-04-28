---
description: 'Threadklasse: Diese Klasse ist die übergeordnete Klasse für Threadereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: 0bf14240-3b8d-4eb5-b751-7b2e23b55762
title: Thread-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread
api_type:
- NA
api_location: ''
ms.openlocfilehash: 121a8d4aa04017011648d80329ee02396582987a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105528"
---
# <a name="thread-class"></a>Thread-Klasse

Diese Klasse ist die übergeordnete Klasse für Threadereignisse.

Die folgende Syntax wird durch MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **Thread-Klasse** definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um Threadereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **FLAG EVENT TRACE FLAG \_ \_ \_ THREAD** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an.

Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für Threadereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**ThreadGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Threadereignis beim Verwenden von Ereignissen zu identifizieren.



| Ereignistyp                                                      | BESCHREIBUNG                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ END**(Ereignistypwert ist 2)<br/>   | Endthreadereignis. Die [**\_ MOF-Klasse Thread TypeGroup1**](thread-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                        |
| **EVENT \_ TRACE \_ TYPE \_ START**(Ereignistypwert ist 1)<br/> | Threadereignis starten. Die [**\_ MOF-Klasse Thread TypeGroup1**](thread-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                      |
| Ereignistypwert, 3                                             | Starten des Datensammlungsthread-Ereignisses. Aufzählen von Threads, die derzeit zum Zeitpunkt des Starts der Kernelsitzung ausgeführt werden. Die [**\_ MOF-Klasse Thread TypeGroup1**](thread-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis. |
| Ereignistypwert, 4                                             | Enddatensammlungsthreadereignis. Listet Threads auf, die derzeit zum Zeitpunkt des Beendens der Kernelsitzung ausgeführt werden. Die [**MOF-Klasse Thread \_ TypeGroup1**](thread-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.     |



 

Prozess- und Threadstartereignisse können im Kontext des übergeordneten Prozesses oder Threads protokolliert werden. Daher entsprechen die **ProcessId-** und **ThreadId-Member** von [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht dem Prozess und Thread, der erstellt wird. Aus diesem Grund enthalten diese Ereignisse die Prozess- und Threadbezeichner in den Ereignisdaten (zusätzlich zu denen im Ereignisheader).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_ThreadtypGruppe1**](thread-typegroup1.md)
</dt> <dt>

[**Thread \_ V0**](thread-v0.md)
</dt> <dt>

[**Thread \_ V1**](thread-v1.md)
</dt> <dt>

[**Thread \_ V2**](thread-v2.md)
</dt> </dl>

 

 

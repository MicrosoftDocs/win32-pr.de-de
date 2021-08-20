---
description: Diese Klasse ist die übergeordnete Klasse für Leistungsindikatorereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: PerfInfo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PerfInfo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 641ebb361d14fa8abb0c8199cf113cfd85a2e6700e262447c1302f3f1b66231a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151406"
---
# <a name="perfinfo-class"></a>PerfInfo-Klasse

Diese Klasse ist die übergeordnete Klasse für Leistungsindikatorereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **PerfInfo-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Um DPC-Ereignisse (Deferred Procedure Call) in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **\_ \_ \_ DPC-Flag EVENT TRACE FLAG** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an. Sie können auch eines oder mehrere der folgenden Flags angeben:

-   **\_ \_ \_ EREIGNISABLAUFVERFOLGUNGSFLAG-INTERRUPT**
-   **\_ \_ EREIGNISABLAUFVERFOLGUNGSFLAGPROFIL \_**
-   **\_EREIGNISABLAUFVERFOLGUNGSFLAG \_ \_ SYSTEMCALL**

Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für DPC-Ereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**PerfInfoGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Ereignis beim Nutzen von Ereignissen zu identifizieren.



| Ereignistyp           | Beschreibung                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| Ereignistypwert, 46 | Beispielprofilereignis. Die [**MOF-Klasse SampledProfile**](sampledprofile.md) definiert die Ereignisdaten für dieses Ereignis. |
| Ereignistypwert, 51 | Ereignis "Systemaufruf eingeben". Die [**SysCallEnter**](syscallenter.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.   |
| Ereignistypwert, 52 | Beendigungsereignis des Systemaufrufs. Die [**MOF-Klasse SysCallExit**](syscallexit.md) definiert die Ereignisdaten für dieses Ereignis.      |
| Ereignistypwert, 66 | Threaded DPC-Ereignis. Die [**DPC**](dpc.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                          |
| Ereignistypwert, 67 | Interruptdienstroutine (ISR)-Ereignis. Die [**ISR**](isr.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.       |
| Ereignistypwert, 68 | DPC-Ereignis. Die [**DPC**](dpc.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                   |
| Ereignistypwert, 69 | DPC-Timerereignis. Die [**DPC**](dpc.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 

---
description: Diese Klasse ist die übergeordnete Klasse für Seitenfehlerereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: PageFault_V2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd8adfa698975f7661abdbd849136d04049b5539ff3fed3b52b61660791add0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900750"
---
# <a name="pagefault_v2-class"></a>PageFault \_ V2-Klasse

Diese Klasse ist die übergeordnete Klasse für Seitenfehlerereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class PageFault_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **PageFault \_ V2-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Um alle Seitenfehlerereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **FLAG EVENT TRACE FLAG MEMORY PAGE \_ \_ \_ \_ \_ FAULTS** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an. Sie können auch die folgenden Flags angeben:

-   **\_ \_ EREIGNIS-ABLAUFVERFOLGUNGSFLAG– \_ ARBEITSSPEICHER – \_ HARTE \_ FEHLER**
-   **EVENT \_ TRACE \_ FLAG \_ VIRTUAL \_ ALLOC**

Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für alle Seitenfehlerereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**PageFaultGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Speicherereignis beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EVENT \_ TRACE TYPE MM MM \_ \_ \_ MM(Ereignistypwert ist 12)<br/> | Copy-on-Write-Ereignis. Die [**MOF-Klasse \_ PageFault TypeGroup1**](pagefault-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis. Vor der Windows Vista definiert die [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF-Klasse das Ereignis.     |
| EVENT \_ TRACE TYPE MM \_ \_ \_ TIPPF(Ereignistypwert ist 11)<br/> | Anforderungsfehlerereignis 0 (null). Die [**MOF-Klasse \_ PageFault TypeGroup1**](pagefault-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis. Vor der Windows Vista definiert die [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF-Klasse das Ereignis. |
| EVENT \_ TRACE TYPE MM \_ \_ \_ GPF(Ereignistypwert ist 13)<br/> | Fehlerereignis der Schutzseite. Die [**MOF-Klasse \_ PageFault TypeGroup1**](pagefault-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis. Vor der Windows Vista definiert die [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF-Klasse das Ereignis.  |
| EVENT \_ TRACE TYPE MM \_ \_ \_ HPF(Ereignistypwert ist 14)<br/> | Fehlerereignis für harte Seiten. Die [**MOF-Klasse \_ PageFault TypeGroup1**](pagefault-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis. Vor der Windows Vista definiert die [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF-Klasse das Ereignis.   |
| EVENT \_ TRACE TYPE MM TF \_ \_ \_ (Ereignistypwert ist 10)<br/>  | Übergangsfehlerereignis. Die [**MOF-Klasse \_ PageFault TypeGroup1**](pagefault-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis. Vor der Windows Vista definiert die [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF-Klasse das Ereignis.  |
| EVENT \_ TRACE TYPE MM \_ \_ \_ AV(Ereignistypwert ist 15)<br/>  | Zugriffsverletzungsereignis. Die [**MOF-Klasse \_ PageFault TypeGroup1**](pagefault-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                           |
| Ereignistypwert, 32                                           | Fehlerereignis für harte Seiten. Die [**PageFault \_ HardFault**](pagefault-hardfault.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                               |
| Ereignistypwert, 105                                          | Bildladeereignis in Seitendatei. Die [**MOF-Klasse \_ PageFault ImageLoadBacked**](pagefault-imageloadbacked.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                          |
| Ereignistypwert, 98                                           | Virtuelles Zuordnungsereignis. Die [**MOF-Klasse VirtualAlloc**](pagefault-virtualalloc.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                |
| Ereignistypwert, 99                                           | Virtuelles kostenloses Ereignis. Die [**MOF-Klasse VirtualAlloc**](pagefault-virtualalloc.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                      |



 

Sie können die **ProcessId- und** **ThreadId-Member** von [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) verwenden, um den fehlerhaften Prozess oder Thread zu identifizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



 

 

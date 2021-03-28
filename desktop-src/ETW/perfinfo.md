---
description: Diese Klasse ist die übergeordnete Klasse für Leistungs Ereignis Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: Perfinfo-Klasse
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
ms.openlocfilehash: 93f12242fef86e5eab81bb702b783eb1f4c1915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977705"
---
# <a name="perfinfo-class"></a>Perfinfo-Klasse

Diese Klasse ist die übergeordnete Klasse für Leistungs Ereignis Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **perfinfo** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um DPC-Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das **ereignisablaufverfolgungsflag \_ \_ \_ DPC** -Flag im **enableflags** -Member einer [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) -Struktur beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion an. Sie können auch eines oder mehrere der folgenden Flags angeben:

-   **Flag für Ereignis Ablauf \_ Verfolgung \_ \_**
-   **Ereignis Ablauf \_ Verfolgungs \_ Flag- \_ Profil**
-   **Ereignis \_ Ablaufverfolgungsflag \_ \_ systemrückruf**

Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für DPC-Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**perfinfoguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben. Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Ereignis beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp           | BESCHREIBUNG                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| Ereignistyp Wert, 46 | Samplingprofilereignis. Die [**sampledprofile**](sampledprofile.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. |
| Ereignistyp Wert, 51 | System Rückruf: Ereignis eingeben. Die " [**syscallenter**](syscallenter.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.   |
| Ereignistyp Wert, 52 | Exit-Ereignis für System Aufrufe. Die " [**syscallexit**](syscallexit.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.      |
| Ereignistyp Wert, 66 | Thread-DPC-Ereignis. Die [**DPC**](dpc.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                          |
| Ereignistyp Wert, 67 | ISR-Ereignis (Interrupt Service Routine). Die [**ISR**](isr.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.       |
| Ereignistyp Wert, 68 | DPC-Ereignis. Die [**DPC**](dpc.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                   |
| Ereignistyp Wert, 69 | DPC-Zeit Geber Ereignis. Die [**DPC**](dpc.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                             |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 

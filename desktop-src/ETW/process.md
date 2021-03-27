---
description: Diese Klasse ist die übergeordnete Klasse für Prozess Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: b014262044db9e227bec5af2b351d1392c243c23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980392"
---
# <a name="process-class"></a>Process-Klasse

Diese Klasse ist die übergeordnete Klasse für Prozess Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Process : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **Process** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um Prozess Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das Ablaufverfolgungsflag für die **Ereignis \_ \_ \_ Ablauf Verfolgung** im **enableflags** -Member einer Eigenschaften Struktur der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion an. Sie können auch das folgende Flag angeben:

-   **Prozessindikatoren für die Ereignis \_ \_ \_ Ablauf Verfolgung \_**

Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für Prozess Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**ProcessGuid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben. Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Prozess Ereignis beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp                                                      | BESCHREIBUNG                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ Ende**(Ereignistyp Wert ist 2)<br/>   | Prozess Ereignis beenden. Die " [**Process \_ TypeGroup1**](process-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                          |
| **Ereignis \_ \_ \_ Start** Ablaufverfolgungstyp (Ereignistyp Wert ist 1)<br/> | Prozess Ereignis starten. Die " [**Process \_ TypeGroup1**](process-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                        |
| Ereignistyp Wert, 3                                             | Ereignis zum Starten der Daten Sammlungs Verarbeitung. Listet die Prozesse auf, die derzeit zum Zeitpunkt des Starts der Kernel Sitzung ausgeführt werden. Die " [**Process \_ TypeGroup1**](process-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis. |
| Wert für Ereignistyp, 4                                             | Ereignis für Daten Sammlungs Prozess beenden. Listet Prozesse auf, die zurzeit ausgeführt werden, wenn die Kernel Sitzung beendet wird. Die " [**Process \_ TypeGroup1**](process-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.     |



 

Prozess-und Thread Start Ereignisse können im Kontext des übergeordneten Prozesses oder Threads protokolliert werden. Folglich entsprechen die **ProcessID** -und **ThreadId** -Member des [**Ereignis Ablauf \_ Verfolgungs \_ Headers**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht dem Prozess und dem Thread, der erstellt wird. Aus diesem Grund enthalten diese Ereignisse die Prozess-und Thread Bezeichner in den Ereignisdaten (zusätzlich zu den in der Ereignis Kopfzeile).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ systemtrace**](msnt-systemtrace.md)
</dt> <dt>

[**Prozess \_ TypeGroup1**](process-typegroup1.md)
</dt> <dt>

[**Prozess \_ v0**](process-v0.md)
</dt> <dt>

[**Prozess \_ v1**](process-v1.md)
</dt> <dt>

[**Prozess \_ v2**](process-v2.md)
</dt> </dl>

 

 

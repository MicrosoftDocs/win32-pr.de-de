---
description: Diese Klasse ist die übergeordnete Klasse für Thread Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: c4af87462607b675e46b3459a811925fbefe3ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218861"
---
# <a name="thread-class"></a>Thread-Klasse

Diese Klasse ist die übergeordnete Klasse für Thread Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **Thread** Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um Thread Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das **ereignisablaufverfolgungsflag \_ \_ \_ Thread** -Flag im **enableflags** -Member einer [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) -Struktur beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion an.

Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für Thread Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**threadguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben. Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Thread Ereignis zu identifizieren, wenn Ereignisse verwendet werden.



| Ereignistyp                                                      | BESCHREIBUNG                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ Ende**(Ereignistyp Wert ist 2)<br/>   | End Thread Ereignis. Die [**Thread \_ TypeGroup1**](thread-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                        |
| **Ereignis \_ \_ \_ Start** Ablaufverfolgungstyp (Ereignistyp Wert ist 1)<br/> | Starten Sie das Thread Ereignis. Die [**Thread \_ TypeGroup1**](thread-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                      |
| Ereignistyp Wert, 3                                             | Ereignis für Daten Sammlungs Thread starten. Listet Threads auf, die derzeit zum Zeitpunkt des Starts der Kernel Sitzung ausgeführt werden. Die [**Thread \_ TypeGroup1**](thread-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. |
| Wert für Ereignistyp, 4                                             | Ereignis zum Beenden der Daten Sammlungs Thread. Listet Threads auf, die zurzeit ausgeführt werden, wenn die Kernel Sitzung beendet wird. Die [**Thread \_ TypeGroup1**](thread-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.     |



 

Prozess-und Thread Start Ereignisse können im Kontext des übergeordneten Prozesses oder Threads protokolliert werden. Folglich entsprechen die **ProcessID** -und **ThreadId** -Member des [**Ereignis Ablauf \_ Verfolgungs \_ Headers**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht dem Prozess und dem Thread, der erstellt wird. Aus diesem Grund enthalten diese Ereignisse die Prozess-und Thread Bezeichner in den Ereignisdaten (zusätzlich zu den in der Ereignis Kopfzeile).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ systemtrace**](msnt-systemtrace.md)
</dt> <dt>

[**Thread \_ TypeGroup1**](thread-typegroup1.md)
</dt> <dt>

[**Thread \_ v0**](thread-v0.md)
</dt> <dt>

[**Thread \_ v1**](thread-v1.md)
</dt> <dt>

[**Thread \_ v2**](thread-v2.md)
</dt> </dl>

 

 

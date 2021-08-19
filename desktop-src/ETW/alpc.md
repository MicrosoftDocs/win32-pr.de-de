---
description: Diese Klasse ist die übergeordnete Klasse für erweiterte Lokale Prozeduraufrufereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 5380fada-50e7-4eb2-8549-6d738a56d2cd
title: ALPC-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC
api_type:
- NA
api_location: ''
ms.openlocfilehash: 435b55c44f06b6be062653a45e14a1a890e026371d8bd8e649c87ce3542118c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070290"
---
# <a name="alpc-class"></a>ALPC-Klasse

Diese Klasse ist die übergeordnete Klasse für erweiterte Lokale Prozeduraufrufereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **ALPC-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Um erweiterte Aufrufereignisse für lokale Prozeduren in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **FLAG EVENT TRACE FLAG \_ \_ \_ ALPC** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an.

Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für ALPC-Ereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**ALPCGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche ALPC-Ereignis bei der Nutzung von Ereignissen zu identifizieren.



| Ereignistyp           | Beschreibung                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Ereignistypwert, 33 | Nachrichtenereignis senden. Die [**ALPC \_ Send \_ Message**](alpc-send-message.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                           |
| Ereignistypwert, 34 | Nachrichtenereignis empfangen. Die [**MOF-Klasse für ALPC \_ \_ Receive Message**](alpc-receive-message.md) definiert die Ereignisdaten für dieses Ereignis.                  |
| Ereignistypwert, 35 | Warten Sie auf das Antwortereignis. Die [**MOF-Klasse ALPC \_ Wait For \_ \_ Reply**](alpc-wait-for-reply.md) definiert die Ereignisdaten für dieses Ereignis.                    |
| Ereignistypwert, 36 | Warten Sie auf ein neues Nachrichtenereignis. Die [**MOF-Klasse ALPC \_ Wait For New \_ \_ \_ Message**](alpc-wait-for-new-message.md) definiert die Ereignisdaten für dieses Ereignis. |
| Ereignistypwert, 37 | Warteereignis beenden. Die [**MOF-Klasse ALPC \_ Unwait**](alpc-unwait.md) definiert die Ereignisdaten für dieses Ereignis.                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 


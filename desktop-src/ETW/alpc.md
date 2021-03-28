---
description: Diese Klasse ist die übergeordnete Klasse für erweiterte Ereignisse des lokalen Prozedur Aufrufes. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 2a4b09a8bab9280de8fb4c91368f5d6d93f7944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977728"
---
# <a name="alpc-class"></a>ALPC-Klasse

Diese Klasse ist die übergeordnete Klasse für erweiterte Ereignisse des lokalen Prozedur Aufrufes.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **ALPC** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um erweiterte Aufruf Ereignisse für lokale Prozeduren in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das **ereignisablaufverfolgungsflag \_ \_ \_ ALPC** in dem **enableflags** -Member einer [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) -Struktur beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion an

Consumer der Ereignis Ablauf Verfolgung können eine spezielle Verarbeitung für ALPC-Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**alpcguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben. Verwenden Sie die folgenden Ereignis Typen, um beim Verarbeiten von Ereignissen das tatsächliche ALPC-Ereignis zu identifizieren.



| Ereignistyp           | BESCHREIBUNG                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Ereignistyp Wert, 33 | Sende Nachrichten Ereignis. Die " [**ALPC \_ Send \_ Message**](alpc-send-message.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                           |
| Ereignistyp Wert, 34 | Nachrichten Ereignis empfangen. Die " [**ALPC \_ Receive \_ Message**](alpc-receive-message.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                  |
| Ereignistyp Wert, 35 | Warten auf Antwort Ereignis. Die [**ALPC \_ Wait \_ for \_ Reply**](alpc-wait-for-reply.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                    |
| Ereignistyp Wert, 36 | Warten Sie auf das neue Message-Ereignis. Die [**ALPC- \_ Wartezeit \_ für die \_ neue \_**](alpc-wait-for-new-message.md) MOF-Nachrichten Klasse definiert die Ereignisdaten für dieses Ereignis. |
| Ereignistyp Wert, 37 | Warten Sie das wartende Ereignis. Die " [**ALPC \_ Unwait**](alpc-unwait.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                        |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 


---
description: Diese Klasse ist die übergeordnete Klasse für Split IO-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: Splitio-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: f2efc14ce8804852f983ebe9dcb852c8c0669899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978841"
---
# <a name="splitio-class"></a>Splitio-Klasse

Diese Klasse ist die übergeordnete Klasse für Split IO-Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **splitio** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um geteilte e/a-Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das Flag für die Ablaufverfolgungsflag **\_ \_ \_ Split \_ IO** im **enableflags** -Member einer Eigenschaften Struktur der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion

Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für Split IO-Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**splitioguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben. Verwenden Sie den folgenden Ereignistyp, um das tatsächliche Ereignis beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp           | BESCHREIBUNG                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| Ereignistyp Wert, 32 | IO-Ereignis aufteilen. Die " [**splitio \_ Info**](splitio-info.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis. |



 

Split IO-Ereignisse zeigen an, dass die e/a-Anforderungen aufgrund der zugrunde liegenden Spiegelung der Datenträger Hardware in mehrere e/a-Anforderungen aufgeteilt wurden

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 

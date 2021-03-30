---
description: Diese Klasse ist die übergeordnete Klasse für Stapel Ablauf Verfolgungs Ereignisse.
ms.assetid: 3c0ff01b-fb37-4931-9484-ff8048abca66
title: Stackwalk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ad873815cb5cea40c1a9d2f694eca8d0e90d11b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977624"
---
# <a name="stackwalk-class"></a>Stackwalk-Klasse

Diese Klasse ist die übergeordnete Klasse für Stapel Ablauf Verfolgungs Ereignisse.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{def2fe46-7bd6-4b80-bd94-f57fe20d0ce3}")]
class StackWalk : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **Stackwalk** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um die Stapel Überwachung von Kernel Ereignissen zu aktivieren, müssen Sie die [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) -Funktion und die Kernel Ereignisse und-Typen angeben, für die Sie die Stapel Überwachung aufzeichnen möchten. Um die Stapel Überwachung für andere Ereignisse zu aktivieren, legen Sie den **enableproperty** -Member von Ablauf Verfolgungs [**\_ \_ Parametern aktivieren**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) auf **Ereignis \_ Aktivierung \_ Eigenschaften \_ Stapel \_** Überwachung fest.

Verwenden Sie den folgenden Ereignistyp, um das tatsächliche Ereignis beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp           | BESCHREIBUNG                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------|
| Ereignistyp Wert, 32 | Stapel Ablauf Verfolgungs Ereignis. Die MOF-Klasse des [**Stackwalk- \_ Ereignisses**](stackwalk-event.md) definiert die Ereignisdaten für dieses Ereignis. |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

 

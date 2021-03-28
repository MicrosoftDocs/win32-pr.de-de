---
description: Stellt die übergeordnete Klasse dar, von der alle Objekt-Manager-Ereignis Ablauf Verfolgungs Klassen abgeleitet werden.
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: Obtrace-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTrace
api_type:
- NA
api_location: ''
ms.openlocfilehash: ca89f58df9f5dd741da5b1fb8572b153c956cd43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757662"
---
# <a name="obtrace-class"></a>Obtrace-Klasse

Stellt die übergeordnete Klasse dar, von der alle Objekt-Manager-Ereignis Ablauf Verfolgungs Klassen abgeleitet werden.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **obtrace** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um die Objekt-Manager-Ereignis Ablauf Verfolgung zu aktivieren, müssen Sie die [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) -Funktion mit dem *informationclass* -Parameter aufrufen, der gleich dem Enumerationswert der [**Trace \_ Info- \_ Klasse**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) , **tracesystemtraceenableflagsinfo** , und dem **enableflags** -Member der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) gleich dem **perf-ob- \_ \_ handle** (0x

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |



 

 

---
description: Stellt die übergeordnete Klasse dar, von der alle Objekt-Manager-Ereignisablaufverfolgungsklassen abgeleitet werden.
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: ObTrace-Klasse
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
ms.openlocfilehash: 8cf30fe0c7b028c819477bcf0c66c2b674fc588286916be1cd1fd1a6b207770d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328750"
---
# <a name="obtrace-class"></a>ObTrace-Klasse

Stellt die übergeordnete Klasse dar, von der alle Objekt-Manager-Ereignisablaufverfolgungsklassen abgeleitet werden.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **ObTrace-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Um die Ereignisablaufverfolgung des Objekt-Managers zu aktivieren, rufen Sie die [**TraceSetInformation-Funktion**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) mit dem *InformationClass-Parameter* auf, der dem [**TRACE INFO \_ \_ CLASS-Enumerationswert**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) **TraceSystemTraceEnableFlagsInfo** und dem **EnableFlags-Member** der [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) gleich **PERF OB \_ \_ HANDLE** (0x80000040) entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |



 

 

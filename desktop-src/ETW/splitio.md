---
description: Diese Klasse ist die übergeordnete Klasse für geteilte E/A-Ereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: SplitIo-Klasse
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
ms.openlocfilehash: 0268c3dfa778eb8694a81f57b9212b68bd6674e6c7de6324cdc297550745b2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069720"
---
# <a name="splitio-class"></a>SplitIo-Klasse

Diese Klasse ist die übergeordnete Klasse für geteilte E/A-Ereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **SplitIo-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Um split IO-Ereignisse in einer NT Kernel-Protokollierungssitzung zu aktivieren, geben Sie das **EVENT TRACE FLAG SPLIT \_ \_ \_ \_ IO-Flag** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an, wenn Sie die [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) aufrufen.

Consumer der Ereignisablaufverfolgung können eine spezielle Verarbeitung für split-E/A-Ereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**SplitIoGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie den folgenden Ereignistyp, um das tatsächliche Ereignis beim Nutzen von Ereignissen zu identifizieren.



| Ereignistyp           | Beschreibung                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| Ereignistypwert, 32 | Split E/A-Ereignis. Die [**SPLITIo \_ Info**](splitio-info.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis. |



 

Split E/A-Ereignisse geben an, dass die E/A-Anforderungen aufgrund der zugrunde liegenden Datenträgerhardware für die Spiegelung in mehrere Datenträger-E/A-Anforderungen aufgeteilt wurden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 

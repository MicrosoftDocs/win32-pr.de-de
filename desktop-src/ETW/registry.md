---
description: 'Registrierungsklasse: Diese Klasse ist die übergeordnete Klasse für Registrierungsereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: 362d7653-1ba0-45b7-80f3-0fccca0badf1
title: Registrierungsklasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry
api_type:
- NA
api_location: ''
ms.openlocfilehash: 23cd59e8d6afeb7578bd65625741caaae8156066
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106128"
---
# <a name="registry-class"></a>Registrierungsklasse

Diese Klasse ist die übergeordnete Klasse für Registrierungsereignisse.

Die folgende Syntax wird durch MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(2)]
class Registry : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **Registry-Klasse** definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um Registrierungsereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie die **EVENT \_ TRACE FLAG \_ \_ REGISTRY** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an, wenn Sie die [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) aufrufen.

Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für Registrierungsereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**RegistryGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Registrierungsereignis beim Nutzen von Ereignissen zu identifizieren.



| Ereignistyp                                                                       | BESCHREIBUNG                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ REGCREATE**(Ereignistypwert ist 10)<br/>             | Erstellen sie ein Schlüsselereignis. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                            |
| **EVENT \_ TRACE \_ TYPE \_ REGDELETE**(Ereignistypwert ist 12)<br/>             | Löschen sie das Schlüsselereignis. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                            |
| **EVENT \_ TRACE \_ TYPE \_ REGDELETEVALUE**(Ereignistypwert ist 15)<br/>        | Löschen eines Wertereignis. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                          |
| **EVENT \_ TRACE \_ TYPE \_ REGENUMERATEKEY**(Ereignistypwert ist 17)<br/>       | Enumerate key event (Schlüsselereignis aufzählen). Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                         |
| **EVENT \_ TRACE \_ TYPE \_ REGENUMERATEVALUEKEY**(Ereignistypwert ist 18)<br/>  | Aufzählen des Schlüsselereigniswerts. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                   |
| **EVENT \_ TRACE \_ TYPE \_ REGFLUSH**(Ereignistypwert ist 21)<br/>              | Ereignis zum Leeren des Schlüssels. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                             |
| **EVENT \_ TRACE \_ TYPE \_ REGKCBDMP**(Ereignistypwert ist 22)<br/>             | Erstellen sie ein Schlüsselereignis. Wird generiert, wenn ein Registrierungsvorgang Handles anstelle von Zeichenfolgen verwendet, um auf Unterschlüssel zu verweisen. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis. |
| **EVENT \_ TRACE \_ TYPE \_ REGOPEN**(Ereignistypwert ist 11)<br/>               | Open Key-Ereignis. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                              |
| **EVENT \_ TRACE \_ TYPE \_ REGQUERY**(Ereignistypwert ist 13)<br/>              | Abfrageschlüsselereignis. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                             |
| **EVENT \_ TRACE \_ TYPE \_ REGQUERYMULTIPLEVALUE**(Ereignistypwert ist 19)<br/> | Abfragen eines Ereignisses mit mehreren Werts. Die [**MOF-Klasse Registry \_ TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                  |
| **EVENT \_ TRACE \_ TYPE \_ REGQUERYVALUE**(Ereignistypwert ist 16)<br/>         | Abfragewertereignis. Die [**MOF-Klasse Registry \_ TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                           |
| **EVENT \_ TRACE \_ TYPE \_ REGSETINFORMATION**(Ereignistypwert ist 20)<br/>     | Ereignis zum Festlegen von Informationen. Die [**MOF-Klasse Registry \_ TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                       |
| **EVENT \_ TRACE \_ TYPE \_ REGSETVALUE**(Ereignistypwert ist 14)<br/>           | Festlegen des Wertereignisses. Die [**MOF-Klasse Registry \_ TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                             |
| Ereignistypwert, 23                                                             | Delete Key-Ereignis. Wird generiert, wenn ein Registrierungsvorgang Handles anstelle von Zeichenfolgen verwendet, um auf Unterschlüssel zu verweisen. Die [**MOF-Klasse Registry \_ TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis. |
| Ereignistypwert, 24                                                             | Listet die Registrierungsschlüssel auf, die am Anfang der Sitzung geöffnet sind. Die [**MOF-Klasse Registry \_ TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                           |
| Ereignistypwert, 25                                                             | Listet die Registrierungsschlüssel auf, die am Ende der Sitzung geöffnet sind. Die [**MOF-Klasse Registry \_ TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                  |
| Ereignistypwert, 26                                                             | Die [**MOF-Klasse Registry \_ TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                              |
| Ereignistypwert, 27                                                             | Open Key-Ereignis. Die [**MOF-Klasse Registry \_ TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_RegistrierungstypGruppe1**](registry-typegroup1.md)
</dt> <dt>

[**Registrierung \_ V0**](registry-v0.md)
</dt> <dt>

[**Registrierung \_ V1**](registry-v1.md)
</dt> </dl>

 

 

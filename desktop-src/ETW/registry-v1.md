---
description: 'Registry_V1 Klasse: Diese Klasse ist die übergeordnete Klasse für Registrierungsereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.'
ms.assetid: 7ad92377-3fd7-47e0-b96e-bab530ea9d99
title: Registry_V1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V1
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7c74a52793873a725c4b84e451818e07a49baf5c2839ddd38891a879cee6cb76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394178"
---
# <a name="registry_v1-class"></a>Registry \_ V1-Klasse

Diese Klasse ist die übergeordnete Klasse für Registrierungsereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(1)]
class Registry_V1 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **Registry \_ V1-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Um Registrierungsereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) die **EVENT TRACE FLAG \_ \_ \_ REGISTRY** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an.

Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für Registrierungsereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und **RegistryGuid** als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Registrierungsereignis beim Nutzen von Ereignissen zu identifizieren.



| Ereignistyp                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ REGCREATE**(Ereignistypwert ist 10)<br/>             | Erstellen sie ein Schlüsselereignis. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                     |
| **EVENT \_ TRACE \_ TYPE \_ REGDELETE**(Ereignistypwert ist 12)<br/>             | Löschen sie das Schlüsselereignis. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                     |
| **EVENT \_ TRACE \_ TYPE \_ REGDELETEVALUE**(Ereignistypwert ist 15)<br/>        | Löschen eines Wertereignis. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                   |
| **EVENT \_ TRACE \_ TYPE \_ REGENUMERATEKEY**(Ereignistypwert ist 17)<br/>       | Enumerate key event (Schlüsselereignis aufzählen). Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                  |
| **EVENT \_ TRACE \_ TYPE \_ REGENUMERATEVALUEKEY**(Ereignistypwert ist 18)<br/>  | Aufzählen des Schlüsselereigniswerts. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                            |
| **EVENT \_ TRACE \_ TYPE \_ REGFLUSH**(Ereignistypwert ist 21)<br/>              | Ereignis zum Leeren des Schlüssels. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                      |
| **EVENT \_ TRACE \_ TYPE \_ REGKCBDMP**(Ereignistypwert ist 22)<br/>             | Wird generiert, wenn ein Registrierungsvorgang Handles anstelle von Zeichenfolgen verwendet, um auf Unterschlüssel zu verweisen. Diese Ereignisse werden einmal für jedes Handle aufgezeichnet– beim ersten Verweis auf das Handle. Wiederholte Verweise auf das Handle generieren nicht mehrere Ereignisse.<br/> Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.<br/> **Windows 2000:** Dieser Wert wird nicht unterstützt.<br/> |
| **EVENT \_ TRACE \_ TYPE \_ REGOPEN**(Ereignistypwert ist 11)<br/>               | Öffnen Sie das Schlüsselereignis. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                       |
| **EVENT \_ TRACE \_ TYPE \_ REGQUERY**(Ereignistypwert ist 13)<br/>              | Abfrageschlüsselereignis. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                      |
| **EVENT \_ TRACE \_ TYPE \_ REGQUERYMULTIPLEVALUE**(Ereignistypwert ist 19)<br/> | Abfragen eines Ereignisses mit mehreren Werts. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                           |
| **EVENT \_ TRACE \_ TYPE \_ REGQUERYVALUE**(Ereignistypwert ist 16)<br/>         | Abfragewertereignis. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                    |
| **EVENT \_ TRACE \_ TYPE \_ REGSETINFORMATION**(Ereignistypwert ist 20)<br/>     | Festlegen des Informationsereignis. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                |
| **EVENT \_ TRACE \_ TYPE \_ REGSETVALUE**(Ereignistypwert ist 14)<br/>           | Legen Sie das Wertereignis fest. Die [**\_ MOF-Klasse Registry TypeGroup1**](registry-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Registrierung**](registry.md)
</dt> <dt>

[**Registrierung \_ V0**](registry-v0.md)
</dt> <dt>

[**Registry \_ V1 \_ TypeGroup1**](registry-v1-typegroup1.md)
</dt> </dl>

 

 

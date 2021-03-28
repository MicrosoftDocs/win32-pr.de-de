---
description: Diese Klasse ist die übergeordnete Klasse für Registrierungs Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 362d7653-1ba0-45b7-80f3-0fccca0badf1
title: Registrierungs Klasse
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
ms.openlocfilehash: 6799756ebfe573fad6a32a191e79c3c2b745f563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129696"
---
# <a name="registry-class"></a>Registrierungs Klasse

Diese Klasse ist die übergeordnete Klasse für Registrierungs Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(2)]
class Registry : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **Registry** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um Registrierungs Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie die **ereignisablaufverfolgungsflag- \_ \_ \_ Registrierung** im **enableflags** -Member einer [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) -Struktur beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion an

Consumer der Ereignis Ablauf Verfolgung können eine spezielle Verarbeitung für Registrierungs Ereignisse implementieren, indem Sie die Funktion [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**registryguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben. Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Registrierungs Ereignis beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp                                                                       | BESCHREIBUNG                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regcreate**(Ereignistyp Wert ist 10)<br/>             | Schlüsselereignis erstellen. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                            |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ RegDelete**(Ereignistyp Wert ist 12)<br/>             | Schlüsselereignis löschen. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                            |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ RegDeleteValue**(Ereignistyp Wert ist 15)<br/>        | Ereignis zum Löschen von Werten. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                          |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regenenumeratekey**(Ereignistyp Wert ist 17)<br/>       | Listet das Schlüsselereignis auf. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                         |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regenenumeratevaluekey**(Ereignistyp Wert ist 18)<br/>  | Enumerate Value Key-Ereignis. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                   |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regleerung**(Ereignistyp Wert ist 21)<br/>              | Schlüsselereignis leeren. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                             |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regkcbdmp**(Ereignistyp Wert ist 22)<br/>             | Schlüsselereignis erstellen. Wird generiert, wenn ein Registrierungsvorgang Handles anstelle von Zeichen folgen verwendet, um auf Unterschlüssel zu verweisen. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis. |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regopen**(Ereignistyp Wert ist 11)<br/>               | Öffnen Sie das Schlüsselereignis. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                              |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regquery**(Ereignistyp Wert ist 13)<br/>              | Abfrage Schlüsselereignis. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                             |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regquerymultiplevalue**(Ereignistyp Wert ist 19)<br/> | Ereignisse mit mehreren Werten Abfragen. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                  |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ RegQueryValue**(Ereignistyp Wert ist 16)<br/>         | Abfrage Wert Ereignis. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                           |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regsetinformation**(Ereignistyp Wert ist 20)<br/>     | Legen Sie das Informations Ereignis fest. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                       |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ RegSetValue**(Ereignistyp Wert ist 14)<br/>           | Legen Sie ein Wert Ereignis fest. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                             |
| Ereignistyp Wert, 23                                                             | Schlüsselereignis löschen. Wird generiert, wenn ein Registrierungsvorgang Handles anstelle von Zeichen folgen verwendet, um auf Unterschlüssel zu verweisen. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis. |
| Ereignistyp Wert, 24                                                             | Listet die Registrierungsschlüssel auf, die am Anfang der Sitzung geöffnet sind. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                           |
| Ereignistyp Wert, 25                                                             | Listet die Registrierungsschlüssel auf, die am Ende der Sitzung geöffnet sind. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                  |
| Ereignistyp Wert, 26                                                             | Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                              |
| Ereignistyp Wert, 27                                                             | Öffnen Sie das Schlüsselereignis. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                              |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ systemtrace**](msnt-systemtrace.md)
</dt> <dt>

[**Registrierungs \_ TypeGroup1**](registry-typegroup1.md)
</dt> <dt>

[**Registrierung \_ v0**](registry-v0.md)
</dt> <dt>

[**Registrierung \_ v1**](registry-v1.md)
</dt> </dl>

 

 

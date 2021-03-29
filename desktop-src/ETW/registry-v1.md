---
description: Diese Klasse ist die übergeordnete Klasse für Registrierungs Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 320a2bce9213228be4ff5c1880d884ee9622b68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977809"
---
# <a name="registry_v1-class"></a>Registry \_ v1-Klasse

Diese Klasse ist die übergeordnete Klasse für Registrierungs Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(1)]
class Registry_V1 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **Registrierung \_ v1** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um Registrierungs Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie die **ereignisablaufverfolgungsflag- \_ \_ \_ Registrierung** im **enableflags** -Member einer [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) -Struktur beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion an

Consumer der Ereignis Ablauf Verfolgung können eine spezielle Verarbeitung für Registrierungs Ereignisse implementieren, indem Sie die Funktion [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und **registryguid** als *pguid* -Parameter angeben. Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Registrierungs Ereignis beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regcreate**(Ereignistyp Wert ist 10)<br/>             | Schlüsselereignis erstellen. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                     |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ RegDelete**(Ereignistyp Wert ist 12)<br/>             | Schlüsselereignis löschen. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                     |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ RegDeleteValue**(Ereignistyp Wert ist 15)<br/>        | Ereignis zum Löschen von Werten. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                   |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regenenumeratekey**(Ereignistyp Wert ist 17)<br/>       | Listet das Schlüsselereignis auf. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                  |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regenenumeratevaluekey**(Ereignistyp Wert ist 18)<br/>  | Enumerate Value Key-Ereignis. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                            |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regleerung**(Ereignistyp Wert ist 21)<br/>              | Schlüsselereignis leeren. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                      |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regkcbdmp**(Ereignistyp Wert ist 22)<br/>             | Wird generiert, wenn ein Registrierungsvorgang Handles anstelle von Zeichen folgen verwendet, um auf Unterschlüssel zu verweisen. Diese Ereignisse werden für jedes handle einmal aufgezeichnet – beim ersten Verweis auf das handle. Durch wiederholte Verweise auf das Handle werden nicht mehrere Ereignisse generiert.<br/> Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.<br/> **Windows 2000:** Dieser Wert wird nicht unterstützt.<br/> |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regopen**(Ereignistyp Wert ist 11)<br/>               | Öffnen Sie das Schlüsselereignis. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                       |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regquery**(Ereignistyp Wert ist 13)<br/>              | Abfrage Schlüsselereignis. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                      |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regquerymultiplevalue**(Ereignistyp Wert ist 19)<br/> | Ereignisse mit mehreren Werten Abfragen. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                           |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ RegQueryValue**(Ereignistyp Wert ist 16)<br/>         | Abfrage Wert Ereignis. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                    |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ regsetinformation**(Ereignistyp Wert ist 20)<br/>     | Legen Sie das Informations Ereignis fest. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ RegSetValue**(Ereignistyp Wert ist 14)<br/>           | Legen Sie ein Wert Ereignis fest. Die " [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ systemtrace**](msnt-systemtrace.md)
</dt> <dt>

[**Registrierung**](registry.md)
</dt> <dt>

[**Registrierung \_ v0**](registry-v0.md)
</dt> <dt>

[**Registrierung \_ v1 \_ TypeGroup1**](registry-v1-typegroup1.md)
</dt> </dl>

 

 

---
title: Randomdelay (timetriggertype)-Element
description: Enthält die Verzögerungszeit, die der Startzeit des Auslösers zufällig hinzugefügt wird. | Randomdelay (timetriggertype)-Element
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
keywords:
- Randomdelay-Element Taskplaner
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a28613cb236b6dc8a3ae77dce9452423a992a866
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354324"
---
# <a name="randomdelay-timetriggertype-element"></a>Randomdelay (timetriggertype)-Element

Enthält die Verzögerungszeit, die der Startzeit des Auslösers zufällig hinzugefügt wird. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

Das-Element wird durch den komplexen Typ " [**timetriggertype**](taskschedulerschema-timetriggertype-complextype.md) " definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                    | Abgeleitet von                                                               | BESCHREIBUNG                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**Timetrigger (triggergroup)**](taskschedulerschema-timetrigger-triggergroup-element.md) | [**timetriggertype**](taskschedulerschema-timetriggertype-complextype.md) | Gibt einen-Auslösers an, der einen Task startet, wenn der--ausgelöst wird<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**randomdelay-Eigenschaft von Itime-**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay)Auslösung.

Informationen zur Skript Entwicklung finden Sie unter [**timeauslöst. randomdelay**](timetrigger-randomdelay.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 






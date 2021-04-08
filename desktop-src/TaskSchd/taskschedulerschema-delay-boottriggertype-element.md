---
title: Delay (boottriggertype)-Element
description: Gibt den Zeitraum zwischen dem Start des Systems und dem Start der Aufgabe an.
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
keywords:
- Verzögertes Element Taskplaner
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1ab28da8e9c739d3deff52572fe6a5d37f862119
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957205"
---
# <a name="delay-boottriggertype-element"></a>Delay (boottriggertype)-Element

Gibt den Zeitraum zwischen dem Start des Systems und dem Start der Aufgabe an. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

Das **Delay** -Element wird durch den komplexen [**boottriggertype**](taskschedulerschema-boottriggertype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                     | Abgeleitet von                                                               | BESCHREIBUNG                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Boottrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) | [**boottriggertype**](taskschedulerschema-boottriggertype-complextype.md) | Gibt einen-Fehler an, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skript Entwicklung wird die Verzögerung des Ereignis Auslösers durch die [**boottrigger. Delay**](boottrigger-delay.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird die Verzögerung des Ereignis Auslösers durch die [**iboottrigger::D Elay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) -Eigenschaft angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 






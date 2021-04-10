---
title: Delay (sessionstatechangetriggertype)-Element
description: Enthält einen Wert, der die Länge der Verzögerung für einen Task Startzeitpunkt angibt, wenn eine Terminal Server-Sitzungs Zustandsänderung erkannt wird.
ms.assetid: 7fb87c4c-0b69-4c5b-b038-d61fb7c4ab9a
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
ms.openlocfilehash: 03f230465f2e2b49ce83f1af358dfa1f84f21433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106377"
---
# <a name="delay-sessionstatechangetriggertype-element"></a>Delay (sessionstatechangetriggertype)-Element

Enthält einen Wert, der die Länge der Verzögerung für einen Task Startzeitpunkt angibt, wenn eine Terminal Server-Sitzungs Zustandsänderung erkannt wird. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

Das **Delay** -Element wird durch den komplexen Typ [**sessionstatechangetriggertype**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                       | Abgeleitet von                                                                                           | BESCHREIBUNG                                                                                      |
|-------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| **Sessionstatechange-Auslösers** | [**sessionstatechangetriggertype**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Gibt einen-Endpunkt an, der einen Task startet, wenn sich der Status einer Terminal Server Sitzung ändert. <br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird die Verzögerungs Verzögerung für den Sitzungs Statusänderung mithilfe der [**sessionstatechangeghost. Delay**](sessionstatechangetrigger-delay.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird die Verzögerungs Verzögerung der Sitzungs Statusänderung mithilfe der [**Delay-Eigenschaft von isessionstatechangelöst**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay)angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 






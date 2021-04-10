---
title: einfacher multipleinstancespolicytype-Typ
description: Definiert die instanzrichtlinienkonstanten für das multipleinstancespolicy (settingstype)-Element.
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- multipleinstancespolicytype-Typ "Simple" Taskplaner
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29a3523ef16224836ada474fb32265084453479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956683"
---
# <a name="multipleinstancespolicytype-simple-type"></a>einfacher multipleinstancespolicytype-Typ

Definiert die instanzrichtlinienkonstanten für das [**multipleinstancespolicy (settingstype)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) -Element.

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Enumerationswerte

Der einfache Typ " **multipleinstancespolicytype** " definiert die folgenden Werte.



| Wert        | BESCHREIBUNG                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| Parallel     | Startet eine neue Instanz, während eine vorhandene-Instanz ausgeführt wird.<br/>                           |
| Warteschlange        | Startet eine neue Instanz der Aufgabe, nachdem alle anderen Instanzen der Aufgabe vollständig sind.<br/>      |
| Ignorumew    | Standard. Startet keine neue Instanz, wenn eine vorhandene Instanz der Aufgabe ausgeführt wird.<br/> |
| Stopp vorhanden | Beendet eine vorhandene Instanz der Aufgabe vor dem Starten der neuen Instanz.<br/>                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Einfache Typen von Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 






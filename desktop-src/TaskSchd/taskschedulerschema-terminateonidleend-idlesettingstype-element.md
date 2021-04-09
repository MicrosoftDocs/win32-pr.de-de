---
title: Stoponidleend (idlesettingstype)-Element
description: Gibt an, dass der Taskplaner den Task beendet, wenn die Leerlauf Bedingung vor dem Abschluss der Aufgabe endet.
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- Stoponidleend-Element Taskplaner
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a47a01d7d77f3dd20f055bce8e4bb12fad82c771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957069"
---
# <a name="stoponidleend-idlesettingstype-element"></a>Stoponidleend (idlesettingstype)-Element

Gibt an, dass der Taskplaner den Task beendet, wenn die Leerlauf Bedingung vor dem Abschluss der Aufgabe endet.

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

Das **stoponidleend** -Element wird durch den komplexen [**idlesettingstype**](taskschedulerschema-idlesettingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | BESCHREIBUNG                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**Idlesettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idlesettingstype**](taskschedulerschema-idlesettingstype-complextype.md) | Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**stoponidleend-Eigenschaft von iidlesettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).

Informationen zur Skript Entwicklung finden Sie unter [**idlesettings. stoponidleend**](idlesettings-stoponidleend.md).

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert eine Leerlauf Einstellung, die angibt, dass die Aufgabe nicht ausgeführt werden soll, wenn die Leerlauf Bedingung endet.


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
</IdleSettings>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






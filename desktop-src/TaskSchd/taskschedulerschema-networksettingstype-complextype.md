---
title: komplexer networksettingstype-Typ
description: Definiert die Elemente, die die Einstellungen bereitstellen, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- komplexer networksettingstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2a8389b1e1f368bedf03fa38dce9c8e262a401
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956682"
---
# <a name="networksettingstype-complex-type"></a>komplexer networksettingstype-Typ

Definiert die Elemente, die die Einstellungen bereitstellen, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden.

``` syntax
<xs:complexType name="networkSettingsType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="Id"
            type="guidType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                              | type                                                        | BESCHREIBUNG                                                                                 |
|----------------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**Name**](taskschedulerschema-id-networksettingstype-element.md)     | [**guidtype**](taskschedulerschema-guidtype-simpletype.md) | Gibt einen GUID-Wert an, der ein Netzwerk Profil identifiziert. <br/>                       |
| [**Name**](taskschedulerschema-name-networksettingstype-element.md) | nonEmptyString                                              | Gibt den Namen eines Netzwerk Profils an. Der Name wird zu Anzeige Zwecken verwendet. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 






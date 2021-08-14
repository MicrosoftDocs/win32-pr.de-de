---
title: komplexer networkSettingsType-Typ
description: Definiert die Elemente, die die Einstellungen bereitstellen, die der Taskplaner verwendet, um ein Netzwerkprofil zu erhalten.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- komplexes networkSettingsType-Taskplaner
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9969e4e3827d926d8c295d4e1a3ce7b77550804eb4995a267a920a16871837f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758470"
---
# <a name="networksettingstype-complex-type"></a>komplexer networkSettingsType-Typ

Definiert die Elemente, die die Einstellungen bereitstellen, die der Taskplaner verwendet, um ein Netzwerkprofil zu erhalten.

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
| [**Id**](taskschedulerschema-id-networksettingstype-element.md)     | [**guidType**](taskschedulerschema-guidtype-simpletype.md) | Gibt einen GUID-Wert an, der ein Netzwerkprofil identifiziert. <br/>                       |
| [**Name**](taskschedulerschema-name-networksettingstype-element.md) | nonEmptyString                                              | Gibt den Namen eines Netzwerkprofils an. Der Name wird zu Anzeigezwecken verwendet. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 






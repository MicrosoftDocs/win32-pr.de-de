---
title: Baseeapparameters Complex Type-Verbindungs Eigenschaften
description: Definiert das Platzhalter Element für den Methodentyp und die Methoden spezifische Konfiguration.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- Baseeapparameters komplexer Typ EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3bfb9f6c833900967525467202421cf94166405
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106353408"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a>Baseeapparameters Complex Type-Verbindungs Eigenschaften

Der komplexe Typ **baseeapparameters** definiert das Platzhalter Element für den Methodentyp und die Methoden spezifische Konfiguration.

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                            | type    | BESCHREIBUNG                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [**type**](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | integer | Eine beliebige Schema Instanz ist hier zulässig.<br/> |



## <a name="remarks"></a>Bemerkungen

In **baseeapparameters** kann die-Methode die konstituierenden Elemente definieren. Die-Methode führt auch eine Schema Validierung für die Elemente in **baseeapparameters** aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[baseeapconnectionpropertiesv1-Schema](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 






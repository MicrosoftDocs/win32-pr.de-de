---
title: EapType-Element (mspeapuserpropertiesv1schema)
description: Dieses Element ist ein abgeleiteter Typ des EapType-Elements aus dem Baseeapuserpropertiesv1-Schema. Für mspeapuserpropertiesv1schema.
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
keywords:
- EapType-Element EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e27923d77a36b917b3356b7c5c79d408bc0a99d49d70967677b56a9047ed0b63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067180"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a>EapType-Element (mspeapuserpropertiesv1schema)

Das **EapType-Element** ist ein abgeleiteter Typ des [**EapType-Elements**](baseeapuserpropertiesv1schema-eaptype-element.md) aus dem [Baseeapuserpropertiesv1-Schema.](baseeapuserpropertiesv1schema-schema.md)

``` syntax
<xs:element name="EapType
        "
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                               | type                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | Das [**Eap-Element**](baseeapuserpropertiesv1schema-eap-element.md) identifiziert die innere Methode und die Anmeldeinformationen, die mit dieser Methode verwendet werden sollen. Wenn die PEAP-Konfiguration für den PEAP-Gastzugriff konfiguriert ist, fehlt dieses Element.<br/>                                  |
| [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [**PeapExtensionsType**](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | Das [**PeapExtensions-Element**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) ermöglicht zukünftige Erweiterungen des Schemas. <br/> Das [**PeapExtensions-Element**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) ist optional.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[mspeapuserpropertiesv1-Schema](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 






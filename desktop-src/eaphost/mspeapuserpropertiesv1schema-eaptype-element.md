---
title: Eaptype-Element (mspeapuserpropertiesv1schema)
description: Dieses Element ist ein abgeleiteter Typ des eaptype-Elements aus dem baseeapuserpropertiesv1-Schema. Für mspeapuserpropertiesv1schema.
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
keywords:
- Eaptype-Element EAPHost
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
ms.openlocfilehash: ccedc72baf3a677acc3a318895defbc97bb26287
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106368280"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a>Eaptype-Element (mspeapuserpropertiesv1schema)

Das **eaptype** -Element ist ein abgeleiteter Typ des [**eaptype**](baseeapuserpropertiesv1schema-eaptype-element.md) -Elements aus dem [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) -Schema.

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
| [**EAP**](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | Das [**EAP**](baseeapuserpropertiesv1schema-eap-element.md) -Element identifiziert die innere Methode und die Anmelde Informationen, die mit dieser Methode verwendet werden sollen. Wenn die Peer-Konfiguration für den Zugriff auf den Peer-Gast Zugriff konfiguriert ist, ist dieses Element nicht vorhanden.<br/>                                  |
| [**"Peer Erweiterungen"**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [**Peer-extensionstype**](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | Das Element " [**Peer-Erweiterungen**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) " ermöglicht zukünftige Erweiterungen des Schemas. <br/> Das Element " [**Peer-Extensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) " ist optional.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapuserpropertiesv1-Schema](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 






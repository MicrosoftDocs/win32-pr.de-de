---
title: EapType-Element (mschapv2connectionpropertiesv1schema)
description: Ein abgeleiteter Typ des EapType-Elements aus dem baseeapconnectionpropertiesv1-Schema. Dies ist das oberste Element, das im Config-Element des EapHostConfig-Schemas angezeigt wird.
ms.assetid: dbd63387-f8ed-4308-903f-7a555f3410f7
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
ms.openlocfilehash: 18d3296dfab4a28ba818199d0b9329888c692f55831bced2af5abedfd1f205e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984060"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a>EapType-Element (mschapv2connectionpropertiesv1schema)

Das **EapType-Element** ist ein abgeleiteter Typ des [EapType-Elements](baseeapconnectionpropertiesv1schema-eaptype-element.md) aus dem [baseeapconnectionpropertiesv1-Schema.](baseeapconnectionpropertiesv1schema-schema.md) Dies ist das oberste Element, das im Config-Element des [EapHostConfig-Schemas](eaphostconfigschema-elements.md) angezeigt wird.

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="UseWinLogonCredentials"
                        type="boolean"
                        default="true"
                        minOccurs="0"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                       | type    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UseWinLogonCredentials**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | boolean | Steuert die Verwendung der Winlogin-Anmeldeinformationen. True gibt an, dass EAP MS-CHAPv2 Anmeldeinformationen von winlogon erhält. False gibt an, dass EAP MS-CHAPv2 Anmeldeinformationen vom Benutzer erhält. <br/> Das [**UseWinLogonCredentials -Element (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) ist optional.<br/> |



## <a name="remarks"></a>Hinweise

Das **processContents-Element** ermöglicht zukünftige Erweiterungen des Schemas. Das **processContents-Element** ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[mschapv2connectionpropertiesv1-Schema](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 






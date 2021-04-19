---
title: Eaptype-Element (mschapv2connectionpropertiesv1schema)
description: Ist ein abgeleiteter Typ des eaptype-Elements aus dem baseeapconnectionpropertiesv1-Schema. Dies ist das oberste Element, das im config-Element des eaphostconfig-Schemas angezeigt wird.
ms.assetid: dbd63387-f8ed-4308-903f-7a555f3410f7
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
ms.openlocfilehash: 3e9b7db3d3e3ab1ba90427a65a5544b87939ca88
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106367176"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a>Eaptype-Element (mschapv2connectionpropertiesv1schema)

Das **eaptype** -Element ist ein abgeleiteter Typ des [eaptype](baseeapconnectionpropertiesv1schema-eaptype-element.md) -Elements aus dem [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) -Schema. Dies ist das oberste Element, das im config-Element des [eaphostconfig](eaphostconfigschema-elements.md) -Schemas angezeigt wird.

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
| [**UseWinLogonCredentials**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | boolean | Steuert die Verwendung der winlogin-Anmelde Informationen. Wenn der Wert true ist, erhält der EAP-MS-CHAPv2 Anmelde Informationen von Winlogon. Wenn der Wert false ist, erhält EAP MS-CHAPv2 Anmelde Informationen vom Benutzer. <br/> Das [**usewinlogon-Anmelde Informationen-Element (eaptype)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) ist optional.<br/> |



## <a name="remarks"></a>Bemerkungen

Das Element **processContents** ermöglicht zukünftige Erweiterungen des Schemas. Das **processContents** -Element ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mschapv2connectionpropertiesv1-Schema](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 






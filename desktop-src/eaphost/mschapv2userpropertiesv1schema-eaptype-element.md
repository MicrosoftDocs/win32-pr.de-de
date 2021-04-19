---
title: Eaptype-Element (mschapv2userpropertiesv1schema)
description: Dieses Element ist ein abgeleiteter Typ des eaptype-Elements aus dem baseeapuserpropertiesv1-Schema. Für mschapv2userpropertiesv1schema.
ms.assetid: 7bd8fb5b-ceff-4d82-a979-b01229f8863a
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
ms.openlocfilehash: d5985123a4679fe9b2524f9338b9181daa11282d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106355074"
---
# <a name="eaptype-element-mschapv2userpropertiesv1schema"></a>Eaptype-Element (mschapv2userpropertiesv1schema)

Das **eaptype** -Element ist ein abgeleiteter Typ des [**eaptype**](baseeapuserpropertiesv1schema-eaptype-element.md) -Elements aus dem [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) -Schema.

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
                    <xs:element
                        minOccurs="0"
                        ref="Username"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:element name="LogonDomain"
                        type="string"
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



| Element                                                                           | type   | BESCHREIBUNG                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Benutzername**](mschapv2userpropertiesv1schema-username-element.md)               |        | Identifiziert den Benutzer, der authentifiziert wird. Wenn dieses Element nicht vorhanden ist, wird der Benutzername aus Winlogon abgerufen. Das [**username**](mschapv2userpropertiesv1schema-username-element.md) -Element ist optional.<br/>                                        |
| [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) | Zeichenfolge | Identifiziert die Domäne des Benutzers oder Computers, der authentifiziert wird. Wenn dieses Element nicht vorhanden ist, wird die Domäne von Winlogon verwendet. Das [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) -Element ist optional.<br/>        |
| [**Anmelden**](mschapv2userpropertiesv1schema-password-eaptype-element.md)       | Zeichenfolge | Identifiziert das Kennwort des Benutzers oder Computers, der authentifiziert wird. Wenn dieses Element nicht vorhanden ist, wird der Kenn Wort Hash von Winlogon abgerufen. Das [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) -Element ist optional.<br/> |



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

[mschapv2userpropertiesv1-Schema](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 






---
title: Eaptype-Element (eaptlsuserpropertiesv1schema)
description: Dieses Element ist ein abgeleiteter Typ des eaptype-Elements aus dem baseeapuserpropertiesv1-Schema. Für eaptlsuserpropertiesv1schema.
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
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
ms.openlocfilehash: 53e5c1404c70542f3604b94aa6cae9c8fc39fd21
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106362112"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a>Eaptype-Element (eaptlsuserpropertiesv1schema)

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
                        ref="Username"
                     />
                    <xs:element name="UserCert"
                        type="hexBinary"
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



| Element                                                                   | type      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Benutzername**](eaptlsuserpropertiesv1schema-username-element.md)         |           | Erfasst den Benutzernamen, der in der EAP-Identity-Antwort gesendet werden soll. Wenn das [**username**](eaptlsuserpropertiesv1schema-username-element.md) -Element nicht vorhanden ist, verwendet EAP-TLS den Namen in dem Zertifikat, auf das im [**userCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) -Element verwiesen wird.<br/> |
| [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | hexBinary | Bezieht sich auf den SHA-1-Hash des Zertifikats, das für die Authentifizierung verwendet werden soll.<br/>                                                                                                                                                                                                                             |



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

[eaptlsuserpropertiesv1-Schema](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 






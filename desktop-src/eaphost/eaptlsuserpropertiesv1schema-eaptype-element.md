---
title: EapType-Element (eaptlsuserpropertiesv1schema)
description: Dieses Element ist ein abgeleiteter Typ des EapType-Elements aus dem Baseeapuserpropertiesv1-Schema. Für eaptlsuserpropertiesv1schema.
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
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
ms.openlocfilehash: fbc58ab640b7993d274abdb134de4648d51c495c07f70a4468460de1d920bd76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021630"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a>EapType-Element (eaptlsuserpropertiesv1schema)

Das **EapType-Element** ist ein abgeleiteter Typ des [**EapType-Elements**](baseeapuserpropertiesv1schema-eaptype-element.md) aus dem [Baseeapuserpropertiesv1-Schema.](baseeapuserpropertiesv1schema-schema.md)

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
| [**Benutzername**](eaptlsuserpropertiesv1schema-username-element.md)         |           | Erfasst den Benutzernamen, der in der Antwort EAP-Identity werden soll. Wenn das [**Username-Element**](eaptlsuserpropertiesv1schema-username-element.md) nicht vorhanden ist, verwendet EAP-TLS den Namen im Zertifikat, auf das im [**UserCert-Element verwiesen**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) wird.<br/> |
| [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | hexBinary | Bezieht sich auf den SHA-1-Hash des Zertifikats, das für die Authentifizierung verwendet werden soll.<br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a>Hinweise

Das **processContents-Element** ermöglicht zukünftige Erweiterungen des Schemas. Das **processContents-Element** ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eaptlsuserpropertiesv1-Schema](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 






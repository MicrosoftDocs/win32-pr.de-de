---
title: Komplexer eapmethodtype-Typ
description: Definiert die Elemente, die einen einzelnen EAP-Methodentyp, VendorID, vendortype und AutorID eindeutig identifizieren.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- Komplexer EAP-Typ eapmethodtype EAPHost
topic_type:
- apiref
api_name:
- EapMethodType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cea2448111266696398d1581aaecdbec2fb5859e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741841"
---
# <a name="eapmethodtype-complex-type"></a>Komplexer eapmethodtype-Typ

Der komplexe Typ **eapmethodtype** definiert die Elemente, die eine einzelne EAP-Methode eindeutig identifizieren: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md), [**vendortype**](eapcommonschema-vendortype-eapmethodtype-element.md)und [**AutorID**](eapcommonschema-authorid-eapmethodtype-element.md).

[**Typ**](eapcommonschema-type-eapmethodtype-element.md) und [**Autorität**](eapcommonschema-authorid-eapmethodtype-element.md) sind obligatorische Elemente, während [**vendortype**](eapcommonschema-vendortype-eapmethodtype-element.md) und [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) nur erforderlich sind, wenn das **Type** -Element 254 (eine erweiterte EAP-Methode) ist.

``` syntax
<xs:complexType name="EapMethodType">
    <xs:sequence>
        <xs:element name="Type"
            type="unsignedByte"
         />
        <xs:element name="VendorId"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="VendorType"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="AuthorId"
            type="unsignedInt"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                | type         | BESCHREIBUNG                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutorID**](eapcommonschema-authorid-eapmethodtype-element.md)     | unsignedInt  | Verweist auf den Autor der Methode. <br/>                                                                                                                                                                                                                 |
| [**type**](eapcommonschema-type-eapmethodtype-element.md)             | unsignedByte | Bezieht sich auf den Typ der EAP-Methode. <br/>                                                                                                                                                                                                               |
| [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md)     | unsignedInt  | Verweist auf den Hersteller, der die-Methode definiert hat,, wenn das [**Type**](eapcommonschema-type-eapmethodtype-element.md) -Element 254 (eine erweiterte EAP-Methode) ist. [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) ist optional. <br/> |
| [**Vendortype**](eapcommonschema-vendortype-eapmethodtype-element.md) | unsignedInt  | Ist der Hersteller definierte Typ für die Methode. Der [**vendortype**](eapcommonschema-vendortype-eapmethodtype-element.md) ist optional. <br/>                                                                                                           |



## <a name="remarks"></a>Bemerkungen

Die Elemente " [**AutorID**](eapcommonschema-authorid-eapmethodtype-element.md) " und " [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) " müssen für eine bestimmte Methode nicht identisch sein.

Die Elemente " [**AutorID**](eapcommonschema-authorid-eapmethodtype-element.md)", " [**Type**](eapcommonschema-type-eapmethodtype-element.md)", " [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) " und " [**vendortype**](eapcommonschema-vendortype-eapmethodtype-element.md) " sind jeweils eine eindeutige Zahl, die von der Internet Assigned Numbers Authority (IANA) ausgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eapcommon-Schema](eapcommonschema-schema.md)
</dt> </dl>

 

 






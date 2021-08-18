---
title: Komplexer EapMethodType-Typ
description: Definiert die Elemente, die einen einzelnen EAP-Methodentyp, VendorId, VendorType und AuthorId eindeutig identifizieren.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- 'EapMethodType: komplexer EAPHost-Typ'
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
ms.openlocfilehash: 059ea8162241c61d88fc93f565fa0aa4ba8aee223212e6fab254ed9d5dec4eea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739170"
---
# <a name="eapmethodtype-complex-type"></a>Komplexer EapMethodType-Typ

Der komplexe **EapMethodType-Typ** definiert die Elemente, die eine einzelne EAP-Methode eindeutig identifizieren: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)und [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md).

[**Type**](eapcommonschema-type-eapmethodtype-element.md) und [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) sind obligatorische Elemente, wohingegen [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) und [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) nur erforderlich sind, wenn das **Type-Element** 254 ist (eine erweiterte EAP-Methode).

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



| Element                                                                | type         | Beschreibung                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md)     | unsignedInt  | Verweist auf den Methodenautor. <br/>                                                                                                                                                                                                                 |
| [**type**](eapcommonschema-type-eapmethodtype-element.md)             | unsignedByte | Bezieht sich auf den EAP-Methodentyp. <br/>                                                                                                                                                                                                               |
| [**Vendorid**](eapcommonschema-vendorid-eapmethodtype-element.md)     | unsignedInt  | Bezieht sich auf den Anbieter, der die Methode definiert hat, wenn das [**Type-Element**](eapcommonschema-type-eapmethodtype-element.md) 254 ist (eine erweiterte EAP-Methode). Die [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) ist optional. <br/> |
| [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) | unsignedInt  | Der vom Anbieter definierte Typ für die Methode. [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) ist optional. <br/>                                                                                                           |



## <a name="remarks"></a>Hinweise

Die [**Elemente AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) und [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) müssen für eine bestimmte Methode nicht identisch sein.

Die Elemente [**AuthorId,**](eapcommonschema-authorid-eapmethodtype-element.md) [**Type,**](eapcommonschema-type-eapmethodtype-element.md) [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) und [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) sind jeweils eine eindeutige Zahl, die von der Internet Assigned Numbers Authority (IANA) ausgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eapcommon-Schema](eapcommonschema-schema.md)
</dt> </dl>

 

 






---
title: Komplexer CertSelection-Typ
description: Erfahren Sie mehr über den komplexen CertSelection-Typ. Dieser Typ bestimmt, wie der Benutzer ein Zertifikat auswählt.
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- Komplexer CertSelection-Typ EAPHost
topic_type:
- apiref
api_name:
- CertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 375ea26fddf07f8d775617c0a2167ed02aa8160de8cc5dde49a92f37f57a335e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984130"
---
# <a name="certselection-complex-type"></a>Komplexer CertSelection-Typ

Der **komplexe Typ CertSelection** bestimmt, wie der Benutzer ein Zertifikat auswählt.

``` syntax
<xs:complexType name="CertSelection">
    <xs:sequence>
        <xs:element name="SimpleCertSelection"
            type="boolean"
            minOccurs="0"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                     | type    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | boolean | Ist standardmäßig TRUE. Wenn [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) auf TRUE festgelegt ist, führt EAP-TLS eine einfache Zertifikatssuche ohne Dropdownlisten für die Auswahl von Zertifikaten durch. Wenn **SimpleCertSelection** false ist, veranschaulicht EAP-TLS dem Benutzer das geeignete Zertifikat, das ausgewählt werden soll.<br/> |



## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 Schema Complex Types](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 






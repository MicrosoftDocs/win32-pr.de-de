---
title: Komplexer certselection-Typ
description: Erfahren Sie mehr über den komplexen certselection-Typ. Dieser Typ bestimmt, wie der Benutzer ein Zertifikat auswählt.
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- Komplexer certselection-Typ EAPHost
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
ms.openlocfilehash: ba22df8dca61696f214e495542319168183dd2bf
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316473"
---
# <a name="certselection-complex-type"></a>Komplexer certselection-Typ

Der komplexe Typ " **certselection** " legt fest, wie der Benutzer ein Zertifikat auswählt.

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
| [**Simplecertselection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | boolean | Ist standardmäßig "true". Wenn [**simplecertselection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) auf true festgelegt ist, führt EAP-TLS eine einfache Zertifikat Suche ohne Dropdown Listen für die Auswahl der Zertifikate durch. Wenn **simplecertselection** den Wert false hat, veranschaulicht EAP-TLS dem Benutzer das geeignete Zertifikat, das ausgewählt werden soll.<br/> |



## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[komplexe eaptlsconnectionpropertiesv1-Schema Typen](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 






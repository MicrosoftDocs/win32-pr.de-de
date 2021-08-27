---
title: Komplexer BaseEapMethodUserCredentials-Typ
description: Erfahren Sie mehr über den komplexen BaseEapMethodUserCredentials-Typ. Dieser Typ ist ein Platzhalterelement für Methoden-Anmeldeinformationsdaten.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- Komplexer BaseEapMethodUserCredentials-Typ EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8102f095ca7d4b1ada6db3c21fbe55e73a98ed6d06d2d6b99032f1a21a344527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094420"
---
# <a name="baseeapmethodusercredentials-complex-type"></a>Komplexer BaseEapMethodUserCredentials-Typ

Der **komplexe BaseEapMethodUserCredentials-Typ** ist ein Platzhalterelement für Methodenanmerkungsdaten.

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>Hinweise

Die EAP-Methode führt eine Schemaüberprüfung für den Inhalt von **BaseEapMethodUserCredentials durch.**

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[baseeapmethodusercredentials-Schema](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 






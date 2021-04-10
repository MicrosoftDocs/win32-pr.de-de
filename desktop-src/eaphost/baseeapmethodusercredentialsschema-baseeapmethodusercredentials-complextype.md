---
title: Komplexer baseeapmethoduseranmeldeinyp
description: Erfahren Sie mehr über den komplexen Basistyp baseeapmethoduseranmeldeinformationen. Dieser Typ ist ein Platzhalter Element für Methoden Anmelde Informationsdaten.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- Der komplexe Typ "baseeapmethoduseranmeldeinformationen" EAPHost
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
ms.openlocfilehash: 37bc7a91a5d90cde6cba1af12bb0a4784ee21c7f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730177"
---
# <a name="baseeapmethodusercredentials-complex-type"></a>Komplexer baseeapmethoduseranmeldeinyp

Der komplexe **Basistyp baseeapmethodusercredenist** ein Platzhalter Element für Anmelde Informationsdaten der Methode.

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

## <a name="remarks"></a>Bemerkungen

Die EAP-Methode führt eine Schema Validierung für den Inhalt von **baseeapmethoduseranmelde** Informationen durch.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[baseeapmethoduseranmeldeinformationen-Schema](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 






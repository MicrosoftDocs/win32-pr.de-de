---
title: Komplexer baseeapmethodconfig-Typ
description: Erfahren Sie mehr über den komplexen Basistyp baseeapmethodconfig. Dieser Typ ist ein Platzhalter Element für die Methoden Konfiguration.
ms.assetid: 9aafd6ad-2342-4882-99d3-2f2e6c3d67b5
keywords:
- Komplexer baseeapmethodconfig-Typ EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac7d628b554696fffd254a45b9b1021d68e2a55e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391032"
---
# <a name="baseeapmethodconfig-complex-type"></a>Komplexer baseeapmethodconfig-Typ

Der komplexe **Basistyp baseeapmethodconfig** ist ein Platzhalter Element für die Methoden Konfiguration.

``` syntax
<xs:complexType name="BaseEapMethodConfig">
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

Die EAP-Methode führt eine Schema Validierung für den Inhalt des **baseeapmethodconfig** -Elements aus.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[baseeapmethodconfig-Schema](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 






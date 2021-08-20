---
title: Komplexer BaseEapMethodConfig-Typ
description: Erfahren Sie mehr über den komplexen BaseEapMethodConfig-Typ. Dieser Typ ist ein Platzhalterelement für die Methodenkonfiguration.
ms.assetid: 9aafd6ad-2342-4882-99d3-2f2e6c3d67b5
keywords:
- Komplexer BaseEapMethodConfig-Typ EAPHost
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
ms.openlocfilehash: 8decb1746391c1337440eb475a8a8face3f8b7466b73015db48e3991841a3c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086775"
---
# <a name="baseeapmethodconfig-complex-type"></a>Komplexer BaseEapMethodConfig-Typ

Der **komplexe BaseEapMethodConfig-Typ** ist ein Platzhalterelement für die Methodenkonfiguration.

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

## <a name="remarks"></a>Hinweise

Die EAP-Methode führt eine Schemaüberprüfung für den Inhalt des **BaseEapMethodConfig-Elements** durch.

## <a name="requirements"></a>Anforderungen



| Rolle | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[baseeapmethodconfig-Schema](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 






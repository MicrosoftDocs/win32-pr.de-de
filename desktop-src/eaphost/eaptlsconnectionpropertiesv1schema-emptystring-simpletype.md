---
title: einfacher emptystring-Typ
description: Erfahren Sie mehr über den einfachen emptystring-Typ, der nicht verwendet wird. Informationen finden Sie unter Anforderungen und Anzeigen zusätzlicher verfügbarer Ressourcen.
ms.assetid: e561b8d5-8683-41a1-bd72-73b1a767b6cf
keywords:
- emptystring Simple Type EAPHost
topic_type:
- apiref
api_name:
- emptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 756c8976c8b989cf77be921491770fcff9ea62d5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039629"
---
# <a name="emptystring-simple-type"></a>einfacher emptystring-Typ

Der einfache **emptystring** -Typ wird nicht verwendet.

``` syntax
<xs:simpleType name="emptyString">
    <xs:restriction
        base="string"
    >
        <xs:maxLength
            value="0"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|-------------------------------------|------------------------------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[einfache eaptlsconnectionpropertiesv1 Schema Typen](eaptlsconnectionpropertiesv1schema-simple-types.md)
</dt> </dl>

 

 






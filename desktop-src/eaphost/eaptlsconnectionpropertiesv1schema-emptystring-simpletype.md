---
title: emptyString Simple Type
description: Erfahren Sie mehr über den einfachen Typ emptyString, der nicht verwendet wird. Sehen Sie sich die Anforderungen an, und zeigen Sie zusätzliche verfügbare Ressourcen an.
ms.assetid: e561b8d5-8683-41a1-bd72-73b1a767b6cf
keywords:
- 'emptyString: einfacher EAPHost-Typ'
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
ms.openlocfilehash: 4f210fadeb0097ffd7a11d80dd47b252dbbfdc614950af0ac07d612b44edd0aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948210"
---
# <a name="emptystring-simple-type"></a>emptyString Simple Type

Der **simple-Typ emptyString** wird nicht verwendet.

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



| Role | Unterstützte Mindestversion des Betriebssystems |
|-------------------------------------|------------------------------------------------------|
| Client<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 Schema Simple Types](eaptlsconnectionpropertiesv1schema-simple-types.md)
</dt> </dl>

 

 






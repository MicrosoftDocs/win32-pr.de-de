---
title: AuthorId (EapMethodType)-Element
description: Erfahren Sie mehr über das AuthorId-Element (EapMethodType). Das AuthorID-Element (EapMethodType) verweist auf den Methodenautor.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- AuthorId-Element EAPHost
topic_type:
- apiref
api_name:
- AuthorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f15c5fc981592bb82f9ad52d590f12ac0b1f4b20af3537a511d01dd0a8cc15e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021750"
---
# <a name="authorid-eapmethodtype-element"></a>AuthorId (EapMethodType)-Element

Das **AuthorId-Element (EapMethodType)** verweist auf den Methodenautor.

Die AuthorId ist eine eindeutige Zahl, die von der Internet Assigned Numbers Authority (IANA) ausgegeben wird.

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

Das **AuthorId-Element** wird durch den komplexen [**EapMethodType-Typ**](eapcommonschema-eapmethodtype-complextype.md) definiert.

## <a name="remarks"></a>Hinweise

Die **Elemente AuthorId** [**und VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) müssen für eine bestimmte Methode nicht identisch sein.

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eapcommon-Schema](eapcommonschema-schema.md)
</dt> </dl>

 

 






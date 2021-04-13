---
title: Type (eapmethodtype)-Element
description: Erfahren Sie mehr über das Type (eapmethodtype)-Element, das auf den EAP-Methodentyp verweist. Informationen finden Sie unter Anforderungen und Anzeigen zusätzlicher verfügbarer Ressourcen.
ms.assetid: 7911e97c-9436-4d60-8497-bee45cdb8db4
keywords:
- Type-Element EAPHost
topic_type:
- apiref
api_name:
- Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d45defd098f560d4deb8698e0fd569492668e0b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391017"
---
# <a name="type-eapmethodtype-element"></a>Type (eapmethodtype)-Element

Das **Type (eapmethodtype)** -Element verweist auf den EAP-Methodentyp.

Der Typ ist eine eindeutige Zahl, die von der Internet Assigned Numbers Authority (IANA) ausgegeben wird.

``` syntax
<xs:element name="Type"
    type="unsignedByte"
 />
```

Das **Type** -Element wird durch den komplexen [**eapmethodtype**](eapcommonschema-eapmethodtype-complextype.md) -Typ definiert.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Eapmethodtype**](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eapcommon-Schema](eapcommonschema-schema.md)
</dt> </dl>

 

 






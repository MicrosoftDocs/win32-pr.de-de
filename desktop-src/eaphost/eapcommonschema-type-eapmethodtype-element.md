---
title: Type (EapMethodType)-Element
description: Erfahren Sie mehr über das Type -Element (EapMethodType), das auf den EAP-Methodentyp verweist. Sehen Sie sich die Anforderungen an, und zeigen Sie zusätzliche verfügbare Ressourcen an.
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
ms.openlocfilehash: 471cb15afc00593d90bec2c0525d8e7aeddc79db13779b7b93ce99d23ccab020
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498414"
---
# <a name="type-eapmethodtype-element"></a>Type (EapMethodType)-Element

Das **Type -Element (EapMethodType)** verweist auf den EAP-Methodentyp.

Der Typ ist eine eindeutige Zahl, die von der Internet Assigned Numbers Authority (IANA) ausgegeben wird.

``` syntax
<xs:element name="Type"
    type="unsignedByte"
 />
```

Das **Type-Element** wird vom komplexen [**EapMethodType-Typ**](eapcommonschema-eapmethodtype-complextype.md) definiert.

## <a name="requirements"></a>Anforderungen



| Rolle | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
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

 

 






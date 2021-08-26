---
title: VendorId (EapMethodType)-Element
description: Bezieht sich auf den Anbieter, der die Methode definiert hat, wenn das Type-Element (EapMethodType) 254 (eine erweiterte EAP-Methode) ist.
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- VendorId-Element EAPHost
topic_type:
- apiref
api_name:
- VendorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29508121a9724a52df19038b82d97576a924c3c8bab49ac6801c1de51ec71919
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067300"
---
# <a name="vendorid-eapmethodtype-element"></a>VendorId (EapMethodType)-Element

Das **VendorId-Element (EapMethodType)** bezieht sich auf den Anbieter, der die Methode definiert hat, wenn das [**Type-Element (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) 254 (eine erweiterte EAP-Methode) ist.

Die **VendorId** ist optional. Bei Verwendung ist **vendorId eine** eindeutige Nummer, die von der Internet Assigned Numbers Authority (IANA) ausgegeben wird.

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

Das **VendorId-Element** wird durch den komplexen [**EapMethodType-Typ**](eapcommonschema-eapmethodtype-complextype.md) definiert.

## <a name="remarks"></a>Hinweise

Die [**Elemente AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) **und VendorId** müssen für eine bestimmte Methode nicht identisch sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



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

 

 






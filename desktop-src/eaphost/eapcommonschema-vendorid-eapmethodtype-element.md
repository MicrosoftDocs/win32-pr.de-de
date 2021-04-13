---
title: VendorID (eapmethodtype)-Element
description: Bezieht sich auf den Hersteller, der die-Methode definiert hat, wenn das Type (eapmethodtype)-Element 254 (eine erweiterte EAP-Methode) ist.
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- VendorID-Element EAPHost
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
ms.openlocfilehash: 9091cdbd7620baf6ec5dc893bd2100b2f04585ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517891"
---
# <a name="vendorid-eapmethodtype-element"></a>VendorID (eapmethodtype)-Element

Das **VendorID (eapmethodtype)-** Element verweist auf den Hersteller, der die Methode definiert hat, wenn das [**Type (eapmethodtype)**](eapcommonschema-type-eapmethodtype-element.md) -Element 254 (eine erweiterte EAP-Methode) ist.

**VendorID** ist optional. Bei Verwendung ist **VendorID** eine eindeutige Zahl, die von der Internet Assigned Numbers Authority (IANA) ausgegeben wird.

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

Das **VendorID-** Element wird durch den komplexen [**eapmethodtype**](eapcommonschema-eapmethodtype-complextype.md) -Typ definiert.

## <a name="remarks"></a>Bemerkungen

Die Elemente " [**AutorID**](eapcommonschema-authorid-eapmethodtype-element.md) " und " **VendorID** " müssen für eine bestimmte Methode nicht identisch sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



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

 

 






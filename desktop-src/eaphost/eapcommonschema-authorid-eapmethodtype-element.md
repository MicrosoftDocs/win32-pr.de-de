---
title: Autorisiert (eapmethodtype)-Element
description: Erfahren Sie mehr über das Autorität-Element (eapmethodtype). Das Element "AutorID" (eapmethodtype) verweist auf den Autor der Methode.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- AutorID-Element EAPHost
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
ms.openlocfilehash: 1c9a756d8ad1fc88154d3d99d4304de6dd50166b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949124"
---
# <a name="authorid-eapmethodtype-element"></a>Autorisiert (eapmethodtype)-Element

Das Element " **AutorID" (eapmethodtype)** verweist auf den Autor der Methode.

Die Autorisierungs-ID ist eine eindeutige Zahl, die von der Internet Assigned Numbers Authority (IANA) ausgestellt wird.

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

Das **Autorität-** Element wird durch den komplexen [**eapmethodtype**](eapcommonschema-eapmethodtype-complextype.md) -Typ definiert.

## <a name="remarks"></a>Bemerkungen

Die Elemente " **AutorID** " und " [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) " müssen für eine bestimmte Methode nicht identisch sein.

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

 

 






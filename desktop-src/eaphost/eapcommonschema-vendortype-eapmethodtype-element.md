---
title: Vendortype (eapmethodtype)-Element
description: Erfahren Sie mehr über das vendortype (eapmethodtype)-Element. Dieses Element ist der Hersteller definierte Typ für die-Methode.
ms.assetid: baa43e60-05e2-43f9-bb38-896725be76b4
keywords:
- Vendortype-Element EAPHost
topic_type:
- apiref
api_name:
- VendorType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29030672cea0deff59f7f3026dcac98d6ff1c178
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474220"
---
# <a name="vendortype-eapmethodtype-element"></a>Vendortype (eapmethodtype)-Element

Das **vendortype (eapmethodtype)** -Element ist der Hersteller definierte Typ für die-Methode.

Das **vendortype** -Element ist optional. Bei Verwendung ist **vendortype** eine eindeutige Zahl, die von der Internet Assigned Numbers Authority (IANA) ausgegeben wird.

``` syntax
<xs:element name="VendorType"
    type="unsignedInt"
 />
```

Das **vendortype** -Element wird durch den komplexen [**eapmethodtype**](eapcommonschema-eapmethodtype-complextype.md) -Typ definiert.

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

 

 






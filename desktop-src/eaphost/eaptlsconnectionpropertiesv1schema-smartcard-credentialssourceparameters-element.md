---
title: Smartcard-Element ("kredentialssourceparameters")
description: Gibt an, dass EAP-TLS das Zertifikat von der Smartcard lesen soll.
ms.assetid: 0755b0bf-520a-4ae6-a8fc-2f69ae12b066
keywords:
- Smartcard-Element EAPHost
topic_type:
- apiref
api_name:
- SmartCard
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14581a06064a242a0f66e763e0b848d7d74bce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342842"
---
# <a name="smartcard-credentialssourceparameters-element"></a>Smartcard-Element ("kredentialssourceparameters")

Das **Smartcard-Element ("kredentialssourceparameters")** gibt an, dass EAP-TLS das Zertifikat von der Smartcard lesen soll.

``` syntax
<xs:element name="SmartCard"
    type="emptyString"
 />
```

Das **Smartcard** -Element wird durch den komplexen Typ " [**dedentialssourceparameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) " definiert.

## <a name="remarks"></a>Bemerkungen

Die [**certifikatestore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) -und **Smartcard** -Elemente können nicht gleichzeitig verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**"Kredentialssourceparameters"**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**"Kredentialssource" (eaptype)**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema Elemente](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 






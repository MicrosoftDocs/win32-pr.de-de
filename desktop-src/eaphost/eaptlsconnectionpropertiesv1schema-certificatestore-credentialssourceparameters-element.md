---
title: Certifikatestore ("kredentialssourceparameters")-Element
description: Gibt an, dass EAP-TLS das Zertifikat aus dem eigenen Speicher des Benutzers oder dem Computer lesen soll, der authentifiziert wird.
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- Certifikatestore-Element EAPHost
topic_type:
- apiref
api_name:
- CertificateStore
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc7c8841fe275d19752f8b774de5766b95824339
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518332"
---
# <a name="certificatestore-credentialssourceparameters-element"></a>Certifikatestore ("kredentialssourceparameters")-Element

Das **CertificateStore ("kredentialssourceparameters")** -Element gibt an, dass EAP-TLS das Zertifikat aus dem eigenen Speicher des Benutzers oder dem Computer lesen soll, der authentifiziert wird.

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

Das **certifikatestore** -Element wird durch den komplexen Typ " [**fordentialssourceparameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) " definiert.

## <a name="remarks"></a>Bemerkungen

Die **certifikatestore** -und [**Smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) -Elemente können nicht gleichzeitig verwendet werden.

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

 

 






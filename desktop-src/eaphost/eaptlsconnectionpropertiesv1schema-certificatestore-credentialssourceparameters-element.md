---
title: CertificateStore-Element (CredentialsSourceParameters)
description: Gibt an, dass EAP-TLS das Zertifikat aus dem My Store des Benutzers lesen soll, oder dass der computer authentifiziert wird.
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- CertificateStore-Element EAPHost
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
ms.openlocfilehash: 8fb3d2b5c9d50ea8b63c513e4fd9e7297afe236c5ccd16711d9bf4371e76a8d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274292"
---
# <a name="certificatestore-credentialssourceparameters-element"></a>CertificateStore-Element (CredentialsSourceParameters)

Das **CertificateStore-Element (CredentialsSourceParameters)** gibt an, dass EAP-TLS das Zertifikat aus my Store des Benutzers oder dem authentifizierten Computer lesen soll.

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

Das **CertificateStore-Element** wird durch den komplexen [**CredentialsSourceParameters-Typ**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) definiert.

## <a name="remarks"></a>Hinweise

Die **Elemente CertificateStore** [**und SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) können nicht gleichzeitig verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**CredentialsSource (EapType)**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schemaelemente](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 






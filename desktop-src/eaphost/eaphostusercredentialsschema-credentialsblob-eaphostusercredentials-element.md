---
title: CredentialsBlob(EapHostUserCredentials)-Element
description: Wird verwendet, wenn die Methodenkonfiguration ein binäres BLOB und nicht im XML-Textformat ist.
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- CredentialsBlob-Element EAPHost
topic_type:
- apiref
api_name:
- CredentialsBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e56fe90677d0988420a97510da75ea24bf9d50610f9b0b06555a127ef5f731c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274474"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a>CredentialsBlob(EapHostUserCredentials)-Element

Das **CredentialsBlob-Element (EapHostUserCredentials)** wird verwendet, wenn die Methodenkonfiguration ein binäres BLOB und nicht im XML-Textformat ist.

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

Das **CredentialsBlob-Element** wird durch das [**EapHostUserCredentials-Element**](eaphostusercredentialsschema-eaphostusercredentials-element.md) definiert.

## <a name="remarks"></a>Hinweise

Die [**Elemente Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) und **CredentialsBlob** können nicht gleichzeitig verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eaphostusercredentials-Schema](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 






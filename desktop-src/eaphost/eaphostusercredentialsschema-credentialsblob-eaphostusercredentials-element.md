---
title: Das Element "kredentialsblob" (eaphustuseranmeldeinformationen)
description: Wird verwendet, wenn die Methoden Konfiguration ein binäres Blob anstelle von im XML-Textformat ist.
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- Kredentialsblob-Element EAPHost
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
ms.openlocfilehash: 1fe7514c3aff50a7ecddadb3d8073a37b6c770eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103238"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a>Das Element "kredentialsblob" (eaphustuseranmeldeinformationen)

Das Element " **kredentialsblob" (eaptustuseranmeldeinformationen)** wird verwendet, wenn die Methoden Konfiguration ein binäres Blob anstelle von XML-Textformat ist.

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

Das Element " **kredentialsblob** " wird durch das [**eaphustuseranmelde**](eaphostusercredentialsschema-eaphostusercredentials-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Die Elemente "- [**Anmelde**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) Informationen" und " **kredentialsblob** " können nicht gleichzeitig verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Eaphustuseranmeldeinformationen**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Eaphustuseranmeldeinformationen**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eaphustuseranmelde-Schema](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 






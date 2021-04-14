---
description: Attribute sind in einer PKCS \# 10-Zertifikat Anforderung enthalten, indem Sie zur certificationrequestinfo-Struktur hinzugefügt werden, die im folgenden ASN. 1-Syntax Beispiel gezeigt wird.
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: PKCS \# 10-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c69260fa09b99c4d91fa1f8bcdafeb4b0da285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350188"
---
# <a name="pkcs-10-attributes"></a>PKCS \# 10-Attribute

Attribute sind in einer PKCS \# 10-Zertifikat Anforderung enthalten, indem Sie zur **certificationrequestinfo** -Struktur hinzugefügt werden, die im folgenden ASN. 1-Syntax Beispiel gezeigt wird. Weitere Informationen zum Hinzufügen von Attributen zu einer Anforderung finden Sie im Thema [Attribut Architektur](attribute-architecture.md) .

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

Das Attribut, das am häufigsten einer PKCS \# 10-Anforderung hinzugefügt wird, ist eine Sammlung von Erweiterungen der Version 3, die durch ein [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) -Objekt definiert werden Da eine PKCS \# 10-Anforderung kein Feld enthält, dem die Erweiterungen direkt hinzugefügt werden können, müssen Sie als Attribut hinzugefügt werden. Die Attribute " **ClientID**", " **cspprovider**", " **OSVersion**" und " **renewalcertificate** " können auch einem PKCS-Thema hinzugefügt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützte Attribute](supported-attributes.md)
</dt> </dl>

 

 




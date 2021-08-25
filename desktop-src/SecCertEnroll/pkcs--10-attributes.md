---
description: Attribute sind in einer PKCS \# 10-Zertifikatanforderung enthalten, indem sie der CertificationRequestInfo-Struktur hinzugefügt werden, die im folgenden ASN.1-Syntaxbeispiel gezeigt wird.
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: PKCS \# 10-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7922f7d308c6956af4c0098ea278a859113af45861ef3d21a20548081e7eee3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993290"
---
# <a name="pkcs-10-attributes"></a>PKCS \# 10-Attribute

Attribute sind in einer PKCS \# 10-Zertifikatanforderung enthalten, indem sie der **CertificationRequestInfo-Struktur** hinzugefügt werden, die im folgenden ASN.1-Syntaxbeispiel gezeigt wird. Weitere Informationen zum Hinzufügen von Attributen zu einer Anforderung finden Sie im Thema [Attributarchitektur.](attribute-architecture.md)

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

Das Attribut, das einer PKCS 10-Anforderung am häufigsten hinzugefügt \# wird, ist eine Auflistung von Erweiterungen der Version 3, die durch ein [**IX509AttributeExtensions-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) definiert werden. Da eine PKCS \# 10-Anforderung kein Feld enthält, dem die Erweiterungen direkt hinzugefügt werden können, müssen sie als Attribut hinzugefügt werden. Die Attribute **ClientId,** **CspProvider,** **OSVersion** und **RenewalCertificate** können auch einem PKCS -Thema hinzugefügt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützte Attribute](supported-attributes.md)
</dt> </dl>

 

 




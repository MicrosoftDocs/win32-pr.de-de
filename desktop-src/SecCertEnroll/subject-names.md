---
description: Das Feld Betreff einer PKCS \# 10-Zertifikat Anforderung enthält den Distinguished Name der Entität, die das Zertifikat anfordert.
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Antragstellernamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 226c294e75477a3960cd0ad824a98b3556c34322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351762"
---
# <a name="subject-names"></a>Antragstellernamen

Das Feld **Betreff** einer PKCS \# 10-Zertifikat Anforderung enthält den Distinguished Name der Entität, die das Zertifikat anfordert.

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

Der Distinguished Name besteht aus einer Sequenz von relativen Distinguished Names (rDNS). Jeder RDN besteht aus einem Satz von Attributen, und jedes Attribut besteht aus einem Objekt Bezeichner und einem Wert. Der Datentyp des Werts wird durch die **directerystring** -Struktur identifiziert.

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       EncodedObjectID,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Erstellen eines Antragsteller namens](creating-a-subject-name.md)
-   [Codieren eines Antragsteller namens](encoding-a-subject-name.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anforderungen](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 

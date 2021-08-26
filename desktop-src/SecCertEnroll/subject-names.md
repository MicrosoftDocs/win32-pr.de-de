---
description: Das Betrefffeld einer PKCS \# 10-Zertifikatanforderung enthält den Distinguished Name der Entität, die das Zertifikat anfordert.
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Antragstellernamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be70af23c524e71c1a9b22f43e391e4f5c8302fba70f24fba1f8268ebfda6e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101100"
---
# <a name="subject-names"></a>Antragstellernamen

Das **Betrefffeld** einer PKCS \# 10-Zertifikatanforderung enthält den Distinguished Name der Entität, die das Zertifikat anfordert.

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

Der Distinguished Name besteht aus einer Sequenz relativer Distinguished Names (RDNs). Jeder RDN besteht aus einem Satz von Attributen, und jedes Attribut besteht aus einem Objektbezeichner und einem Wert. Der Datentyp des Werts wird durch die **DirectoryString-Struktur** identifiziert.

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

Weitere Informationen finden Sie in den folgenden Themen:

-   [Erstellen eines Antragstellernamens](creating-a-subject-name.md)
-   [Codieren eines Antragstellernamens](encoding-a-subject-name.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anforderungen](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 

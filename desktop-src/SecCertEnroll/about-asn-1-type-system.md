---
description: Das Konzept eines Datentyps ist für den ASN.1-Standard (Abstract Syntax Notation One) von grundlegender Bedeutung.
ms.assetid: 85e88e0b-057b-42c7-a3c8-017a30195d1e
title: ASN.1-Typsystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0b5b9780057229d301bbabcdf2484c66bf06b4313587b0e70a68070885a179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905075"
---
# <a name="asn1-type-system"></a>ASN.1-Typsystem

Das Konzept eines Datentyps ist für den ASN.1-Standard (Abstract Syntax Notation One) von grundlegender Bedeutung. Jedes Feld einer Zertifikatanforderungsstruktur ist einem Typ zugeordnet. Betrachten Sie beispielsweise die IM FOLGENDEN Beispiel gezeigte PKCS \# 10 ASN.1-Zertifikatssyntax.

``` syntax
--------------------------------------------------------------------
-- PKCS #10 Certificate request.
--------------------------------------------------------------------
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

--------------------------------------------------------------------
-- Version number.
--------------------------------------------------------------------
CertificationRequestInfoVersion ::= INTEGER

--------------------------------------------------------------------
-- Subject distinguished name (DN).
--------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}

--------------------------------------------------------------------
-- Public key information.
--------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
   algorithm           AlgorithmIdentifier,
   subjectPublicKey    BITSTRING
}

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
} 

--------------------------------------------------------------------
-- Attributes.
--------------------------------------------------------------------
Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   values             AttributeSetValue
}

AttributeSetValue ::= SET OF ANY
```

Die Anforderungsstruktur auf hoher Ebene, **CertificationRequestInfo,** ist ein Typ, der aus einer Sequenz anderer Typen besteht. Wenn ein Typ ist oder nur grundlegende Typen, Zeichenfolgentypen oder **ANY** enthält, kann er nicht weiter unterteilt werden. Beispielsweise ist  das Versionsfeld ein **CertificationRequestInfoVersion-Typ,** der wiederum ein **INTEGER-Typ** ist, ein grundlegender ASN.1-Typ, der nicht aus anderen Typen besteht.

Ein Typsystem ermöglicht es, die Syntax einer Anforderung visuell auf eine Weise zu präsentieren, die von Entwicklern leicht verstanden wird, und ermöglicht es, die Anforderung konsistent für die Übertragung über ein Netzwerk zu codieren. Weitere Informationen zur Codierung finden Sie unter [Distinguished Encoding Rules](distinguished-encoding-rules.md). Weitere Informationen zu ASN.1-Typen finden Sie in den folgenden Themen.

[Standardtypen](about-basic-types.md)

Erläutert die folgenden Datentypen:

* **BIT STRING**
* **Boolean**
* **INTEGER**
* **NULL**
* **OBJEKTBEZEICHNER**
* **OKTETT-ZEICHENFOLGE**

[Zeichenfolgentypen](about-string-types.md)

Erläutert die folgenden Zeichenfolgentypen:

* **BMPString**
* **IA5String**
* **PrintableString**
* **TeletexString**
* **UTF8String**

[Konstruierte Typen](about-constructed-types.md)

Erläutert ASN.1-Datentypen, die grundlegende Typen, Zeichenfolgentypen oder andere konstruierte Typen enthalten können.




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zertifikatanforderungscodierung](about-certificate-request-encoding.md)
</dt> <dt>

[DER-Codierung von ASN.1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Einführung in ASN.1-Syntax und -Codierung](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 




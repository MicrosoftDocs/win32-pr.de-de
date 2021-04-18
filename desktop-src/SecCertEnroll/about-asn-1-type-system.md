---
description: Das Konzept eines-Datentyps ist für die abstrakte Syntax Notation One (ASN. 1) Standard wichtig.
ms.assetid: 85e88e0b-057b-42c7-a3c8-017a30195d1e
title: ASN. 1-Typsystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abbf60bf61e32c5fca882f2e40c946c043ef93e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366240"
---
# <a name="asn1-type-system"></a>ASN. 1-Typsystem

Das Konzept eines-Datentyps ist für die abstrakte Syntax Notation One (ASN. 1) Standard wichtig. Jedes Feld einer Zertifikat Anforderungs Struktur ist einem Typ zugeordnet. Beachten Sie beispielsweise die \# im folgenden Beispiel gezeigte Zertifikat Syntax PKCS 10 ASN. 1.

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

Die Anforderungs Struktur auf hoher Ebene, **certificationrequestinfo**, ist ein Typ, der aus einer Sequenz anderer Typen besteht. Wenn ein Typ ist oder nur grundlegende Typen, Zeichen folgen Typen oder **beliebige** enthält, kann er nicht weiter aufgeschlüsselt werden. Das Feld **Version** ist beispielsweise ein **certificationrequestinfoversion** -Typ, der wiederum ein **ganzzahliger** Typ ist, d. h. ein grundlegender ASN. 1-Typ, der nicht aus anderen Typen besteht.

Ein Typsystem ermöglicht der visuellen Darstellung der Syntax einer Anforderung auf eine Weise, die von Entwicklern bereitgestellt werden kann, und ermöglicht die konsistente Codierung der Anforderung für die Übertragung über ein Netzwerk. Weitere Informationen zur Codierung finden Sie unter [Distinguished Encoding Rules](distinguished-encoding-rules.md). Weitere Informationen zu ASN. 1-Typen finden Sie in den folgenden Themen.

[Standardtypen](about-basic-types.md)

Erläutert die folgenden Datentypen:

* **Bitzeichenfolge**
* **Booleschen**
* **INTEGER**
* **NULL**
* **Objekt Bezeichner**
* **Oktett-Zeichenfolge**

[Zeichen folgen Typen](about-string-types.md)

Erläutert die folgenden Zeichen folgen Typen:

* **Bmpstring**
* **IA5String**
* **PrintableString**
* **Teletexstring**
* **UTF8String**

[Konstruierte Typen](about-constructed-types.md)

Erläutert ASN. 1-Datentypen, die grundlegende Typen, Zeichen folgen Typen oder andere konstruierte Typen enthalten können.




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zertifikat Anforderungs Codierung](about-certificate-request-encoding.md)
</dt> <dt>

[Der-Codierung von ASN. 1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Einführung in die ASN. 1-Syntax und-Codierung](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 




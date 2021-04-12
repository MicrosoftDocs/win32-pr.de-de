---
description: Eine der häufigsten Verwendungen von Zeichen folgen in einer Public Key-Infrastruktur (PKI) ist das Erstellen eines X. 500-Distinguished Name.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Zeichen folgen Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1173de3b2c4c5fd64181cd19c69cfbcecb1d584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216000"
---
# <a name="string-types"></a>Zeichen folgen Typen

Eine der häufigsten Verwendungen von Zeichen folgen in einer Public Key-Infrastruktur (PKI) ist das Erstellen eines X. 500-Distinguished Name. Beispielsweise wird der Antragsteller Name einer Zertifikat Anforderung durch Kombinieren einer Sequenz von relativen Distinguished Names erstellt, wie im folgenden Syntax Beispiel gezeigt.

``` syntax
---------------------------------------------------------------------
-- Breakdown of a subject name in a certificate request.
---------------------------------------------------------------------

CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
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

Die Zertifikatregistrierungs-API unterstützt die folgenden ASN. 1-Zeichen folgen Typen.

## <a name="bmpstring"></a>Bmpstring

Codierungstag: 0x1E

Certreq.exe Name: Unicode- \_ Zeichenfolge

Bei der grundlegenden mehrsprachigen Ebene (BMP) handelt es sich um eine Zeichencodierung, die die erste Ebene des universellen Zeichensatzes (UCS) umfasst. Es gibt 17 Flächen mit der Nummerierung 0 bis 16. BMP belegt die Ebene 0 und umfasst 65.536-Code Punkte von 0x0000 bis 0xFFFF. Dies ist der Abschnitt der Unicode-Zeichen Zuordnung, in der die meisten Zeichen Zuweisungen bisher vorgenommen wurden. Es umfasst lateinische, mittlere Osten, asiatische, afrikanische und andere Sprachen.

## <a name="ia5string"></a>IA5String

Codierungstag: 0x16

Certreq.exe Name: IA5 \_ String

Die internationale Alphabet Nummer 5 (IA5) entspricht im Allgemeinen dem ASCII-Alphabet, aber unterschiedliche Versionen können Akzente oder andere Zeichen enthalten, die für eine regionale Sprache spezifisch sind. Das folgende Beispiel zeigt den **IA5String** -Typ, der in der ASN. 1-Definition der " **alternativenames** "-Zertifikat Erweiterung verwendet wird.

``` syntax
---------------------------------------------------------------------
-- AlternativeNames extension
---------------------------------------------------------------------

AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SEQUENCE OF ANY, 
   directoryName           [4] EXPLICIT ANY,    
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}

OtherName ::= SEQUENCE 
{
   type                    OBJECT IDENTIFIER,
   value                   [0] EXPLICIT ANY 
}
```

## <a name="printablestring"></a>PrintableString

Codierungstag: 0x13

Certreq.exe Name: druckbare \_ Zeichenfolge

Der **PrintableString** -Datentyp war ursprünglich für die Darstellung der beschränkten Zeichensätze vorgesehen, die für die Main Frame-Eingabe Terminals verfügbar waren, wird aber immer noch häufig verwendet. Sie enthält die folgenden Zeichen:

-   A-Z
-   a-z
-   0-9
-   ' ( ) + , - . / : = ? \[space\]

## <a name="teletexstring"></a>Teletexstring

Codierungstag: 0x14

Die **teletexstring** -und die Related **T61String** -Datentypen werden in 8 Bits (oder 16 Bits für Verbund Zeichen) codiert. Beide haben eine Tagnummer von 0x14. Sie werden nicht ausführlich verwendet.

## <a name="utf8string"></a>UTF8String

Codierungstag: 0x0c

Certreq.exe Name: UTF8- \_ Zeichenfolge

Beim 8-Bit-UCS/Unicode-Transformations Format (UTF-8) handelt es sich um eine Zeichencodierung variabler Länge, die jedes universelle Zeichen als Unicode-Zeichen darstellen kann, und das zulassen, dass anfängliche Code Punkte mit ASCII konsistent bleiben. UTF-8 verwendet ein bis vier Bytes. Die Tagnummer ist 0x0c.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN. 1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Der-Codierung von ASN. 1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




---
description: Eine der häufigsten Verwendungsmöglichkeiten von Zeichenfolgen in einer Public Key-Infrastruktur (PKI) ist das Erstellen eines X.500-Distinguished Name.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Zeichenfolgentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9e190e10bc86bd68a344f5aa279b4812bc04437418578320c36e0e1791dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903689"
---
# <a name="string-types"></a>Zeichenfolgentypen

Eine der häufigsten Verwendungsmöglichkeiten von Zeichenfolgen in einer Public Key-Infrastruktur (PKI) ist das Erstellen eines X.500-Distinguished Name. Beispielsweise wird der Betreffname einer Zertifikatanforderung erstellt, indem eine Sequenz relativer Distinguished Names kombiniert wird, wie im folgenden Syntaxbeispiel gezeigt.

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

Die Zertifikatregistrierungs-API unterstützt die folgenden ASN.1-Zeichenfolgentypen.

## <a name="bmpstring"></a>BMPString

Codierungstag: 0x1E

Certreq.exe Name: UNICODE \_ STRING

Die Basic Multilingual Plane (BMP) ist eine Zeichencodierung, die die erste Ebene des Universal Character Set (UCS) umfasst. Es gibt siebzehn Ebenen mit der Nummer 0 bis 16. BMP belegt Ebene 0 und umfasst 65.536 Codepunkte von 0x0000 0xFFFF. Dies ist der Abschnitt der Unicode-Zeichenzuordnung, in dem die meisten Zeichenzuweisungen bisher vorgenommen wurden. Dazu gehören Lateinisch, Naher Osten, Asiatisch, Afrika und andere Sprachen.

## <a name="ia5string"></a>IA5String

Codierungstag: 0x16

Certreq.exe Name: IA5 \_ STRING

Das internationale Alphabet Nummer 5 (IA5) entspricht im Allgemeinen dem ASCII-Alphabet, aber verschiedene Versionen können Akzente oder andere Zeichen enthalten, die für eine regionale Sprache spezifisch sind. Das folgende Beispiel zeigt den **IA5String-Typ,** der in der ASN.1-Definition der **AlternativeNames-Zertifikaterweiterung** verwendet wird.

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

Certreq.exe Name: DRUCKBARE \_ ZEICHENFOLGE

Der **PrintableString-Datentyp** sollte ursprünglich die begrenzten Zeichensätze darstellen, die für Mainframeeingabeterminals verfügbar sind, wird aber weiterhin häufig verwendet. Sie enthält die folgenden Zeichen:

-   A-Z
-   a-z
-   0-9
-   ' ( ) + , - . / : = ? \[space\]

## <a name="teletexstring"></a>TeletexString

Codierungstag: 0x14

Die **Datentypen TeletexString** und **T61String** werden auf 8 Bits (oder 16 Bits für zusammengesetzte Zeichen) codiert. Beide verfügen über eine Tagnummer von 0x14. Sie werden nicht häufig verwendet.

## <a name="utf8string"></a>UTF8String

Codierungstag: 0x0C

Certreq.exe Name: UTF8 \_ STRING

Das 8-Bit UCS/Unicode Transformation Format (UTF-8) ist eine Zeichencodierung variabler Länge, die jedes universelle Zeichen als Unicode-Zeichen darstellen kann, während anfängliche Codepunkte mit ASCII konsistent bleiben können. UTF-8 verwendet ein bis vier Bytes. Die Tagnummer ist 0x0C.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN.1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[DER-Codierung von ASN.1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




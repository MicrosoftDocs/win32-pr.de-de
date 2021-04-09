---
description: Ein X. 509-Zertifikat der Version 1 enthält die folgenden Felder. Die Felder der Version 2 werden in den Feldern der Version 2 behandelt. Die Felder der Version 3 werden in den Erweiterungen der Version 3 erläutert.
ms.assetid: d614130c-cf1b-4580-8903-064982ed738e
title: Grundlegende Felder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad24afa21787227b3fe47ab187a97c7886c9c9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865036"
---
# <a name="basic-fields"></a>Grundlegende Felder

Ein X. 509-Zertifikat der Version 1 enthält die folgenden Felder. Die Felder der Version 2 werden in den [Feldern der Version 2](about-version-2-fields.md)behandelt. Die Felder der Version 3 werden in den [Erweiterungen der Version 3](about-version-3-extensions.md)erläutert.

## <a name="version"></a>Version

Gibt die Versionsnummer des codierten Zertifikats an. Derzeit sind die möglichen Werte für dieses Feld "0", "1" oder "2". Dies kann jedoch in Zukunft erweitert werden.

``` syntax
---------------------------------------------------------------------
-- Version number. Currently, this can be 0, 1, or 2.
---------------------------------------------------------------------
CertificateVersion ::= INTEGER {v1(0), v2(1), v3(2)}
```

## <a name="serial-number"></a>Seriennummer

Enthält eine positive, eindeutige Ganzzahl, die dem Zertifikat von der Zertifizierungsstelle zugewiesen wurde.

``` syntax
---------------------------------------------------------------------
-- Certificate serial number
---------------------------------------------------------------------
CertificateSerialNumber ::= INTEGER
```

## <a name="signature-algorithm"></a>Signaturalgorithmus

Enthält einen [*Objekt Bezeichner*](/windows/desktop/SecGloss/o-gly) (OID), der den Algorithmus angibt, der von der Zertifizierungsstelle zum Signieren des Zertifikats verwendet wird. 1.2.840.113549.1.1.5 gibt beispielsweise einen SHA-1-Hashalgorithmus an, der mit dem RSA-Verschlüsselungsalgorithmus von RSA Laboratories kombiniert ist.

``` syntax
---------------------------------------------------------------------
-- Signature OID
---------------------------------------------------------------------
signature ::= AlgorithmIdentifier

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="issuer"></a>Issuer (Aussteller)

Enthält den [*X. 500*](/windows/desktop/SecGloss/x-gly) Distinguished Name (DN) der Zertifizierungsstelle, die das Zertifikat erstellt und signiert hat.

``` syntax
---------------------------------------------------------------------
-- Issuer name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="validity"></a>Gültigkeitsdauer

Gibt die Zeitspanne an, für die das Zertifikat gültig ist. Datumsangaben bis zum Ende 2049 verwenden das koordinierte Weltzeit (Greenwich Mean Time)-Format (*yymmddhhmmssZ*). Datumsangaben ab dem 1. Januar 2050 verwenden das verallgemeinerte Zeitformat (*yyyymmddhhmmssZ*).

``` syntax
---------------------------------------------------------------------
-- Validity period 
---------------------------------------------------------------------
Validity ::= SEQUENCE 
{
  notBefore           ChoiceOfTime,
  notAfter            ChoiceOfTime
}

ChoiceOfTime ::= CHOICE 
{
  utcTime                 UTCTime,
  generalTime             GeneralizedTime
}
```

## <a name="subject"></a>Subject

Enthält einen X.500-Distinguished Name der Entität, die dem öffentlichen Schlüssel im Zertifikat zugeordnet ist.

``` syntax
---------------------------------------------------------------------
-- Subject name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="public-key"></a>Öffentlicher Schlüssel

Enthält den öffentlichen Schlüssel und Informationen zum zugehörigen Algorithmus.

``` syntax
---------------------------------------------------------------------
--  Subject public key information
---------------------------------------------------------------------
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
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Felder der Version 2](about-version-2-fields.md)
</dt> <dt>

[Erweiterungen der Version 3](about-version-3-extensions.md)
</dt> <dt>

[X. 509-Zertifikate für öffentliche Schlüssel](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 

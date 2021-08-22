---
description: Ein X.509-Zertifikat der Version 1 enthält die folgenden Felder. Felder der Version 2 werden unter Felder der Version 2 erläutert. Felder der Version 3 werden unter Erweiterungen der Version 3 erläutert.
ms.assetid: d614130c-cf1b-4580-8903-064982ed738e
title: Grundlegende Felder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3dae9ceaa3ddd1c4ac8a8ce86425ec32eee45e82ca8b437ed0f0c27f44817ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905085"
---
# <a name="basic-fields"></a>Grundlegende Felder

Ein X.509-Zertifikat der Version 1 enthält die folgenden Felder. Felder der Version 2 werden unter [Felder der Version 2 erläutert.](about-version-2-fields.md) Felder der Version 3 werden unter [Erweiterungen der Version 3 erläutert.](about-version-3-extensions.md)

## <a name="version"></a>Version

Gibt die Versionsnummer des codierten Zertifikats an. Derzeit sind die möglichen Werte dieses Felds 0, 1 oder 2, aber dies kann in Zukunft erweitert werden.

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

Enthält einen [*Objektbezeichner*](/windows/desktop/SecGloss/o-gly) (OID), der den Algorithmus angibt, der von der Zertifizierungsstelle zum Signieren des Zertifikats verwendet wird. 1.2.840.113549.1.1.5 gibt beispielsweise einen SHA-1-Hashalgorithmus an, der mit dem RSA-Verschlüsselungsalgorithmus von RSA Laboratories kombiniert ist.

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

Enthält den [*X.500-Distinguished*](/windows/desktop/SecGloss/x-gly) Name (DN) der Zertifizierungsstelle, die das Zertifikat erstellt und signiert hat.

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

Gibt die Zeitspanne an, für die das Zertifikat gültig ist. Datumsangaben bis Ende 2049 verwenden das format koordinierte Weltzeit (Greenwich Mean Time) (*yymmddhhmmssz*). Datumsangaben ab dem 1. Januar 2050 verwenden das generalisierte Zeitformat (*yyyymmddhhmmssz*).

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

## <a name="subject"></a>Gegenstand

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

[Zertifikate mit öffentlichem X.509-Schlüssel](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 

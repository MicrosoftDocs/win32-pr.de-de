---
description: Die Zertifikatregistrierungs-API unterstützt die folgenden grundlegenden ASN. 1-Typen.
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: Grundlegende Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f3ae64c058fce3466ca06e7bf205c4c4165fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359031"
---
# <a name="basic-types"></a>Grundlegende Typen

Die Zertifikatregistrierungs-API unterstützt die folgenden grundlegenden ASN. 1-Typen.

## <a name="bit-string"></a>Bitzeichenfolge

Codierungstag: 0x03

Certreq.exe Name: \_ Bitzeichenfolge

Ein Bit oder eine binäre Zeichenfolge ist ein beliebig langes Array von Bits. Bestimmte Bits können durch ganze Zahlen und zugewiesene Namen in Klammern identifiziert werden, wie im folgenden Beispiel gezeigt.

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

Zertifikat Schlüssel und Signaturen werden oft als Bitzeichenfolgen dargestellt.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BIT STRING
-- Tag number: 0x03
---------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
  algorithm           AlgorithmIdentifier,
  subjectPublicKey    BIT STRING
} 
```

## <a name="boolean"></a>BOOLEAN

Codierungstag: 0x01

Certreq.exe Name: Boolescher Wert

Ein boolescher Typ kann einen von zwei Werten enthalten: **true** oder **false**. Im folgenden Beispiel wird die ASN. 1-Struktur für eine grundlegende Einschränkungs Zertifikats Erweiterung veranschaulicht. Das **Feld** ZS gibt an, ob ein Zertifikat Antragsteller eine Zertifizierungsstelle (Certification Authority, ca) ist. Die Standard Kritizität ist **false**.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BOOLEAN
-- Tag number: 0x01
---------------------------------------------------------------------
BasicConstraints ::= SEQUENCE 
{
  cA                  BOOLEAN DEFAULT FALSE,
  pathLenConstraint   INTEGER OPTIONAL
}
```

## <a name="integer"></a>INTEGER

Codierungstag: 0x02

Certreq.exe Name: Integer

Eine ganze Zahl kann normalerweise ein beliebiger positiver oder negativer ganzzahliger Wert sein. Das folgende Beispiel zeigt die ASN. 1-Struktur für einen öffentlichen RSA-Schlüssel. Beachten Sie, dass das Feld **publicexponent** auf eine positive ganze Zahl kleiner als 4.294.967.296 beschränkt ist.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: INTEGER
-- Tag number: 0x02
---------------------------------------------------------------------
HUGEINTEGER ::= INTEGER

RSAPublicKey ::= SEQUENCE 
{ 
  modulus         HUGEINTEGER,    
  publicExponent  INTEGER (0..4294967295) 
} 
```

## <a name="null"></a>NULL

Codierungstag: 0x05

Certreq.exe Name: **null**

Ein **null** -Typ enthält ein einzelnes Byte 0x00. Sie kann überall dort verwendet werden, wo die Zertifikat Anforderung einen leeren Wert angeben muss. Ein **AlgorithmIdentifier** ist z. b. eine Sequenz, die einen Objekt Bezeichner (OID) und optionale Parameter enthält.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: NULL
-- Tag number: 0x05
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

Wenn beim Codieren der Struktur keine Parameter vorhanden sind, wird **null** verwendet, um einen leeren Wert anzugeben.

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a>Objekt Bezeichner

Codierungstag: 0x06

Certreq.exe Name: Objekt- \_ ID

Die Zertifikatregistrierungs-API verwendet Objekt Bezeichner (OIDs) als Typ eines universellen Zeigers auf Algorithmusbezeichner, Attribute und andere PKI-Elemente. OIDs werden in der Regel in einer punktierten Dezimal Zeichenfolge wie "2.16.840.1.101.3.4.1.42" dargestellt. Die einzelnen Elemente in der Zeichenfolge, die durch Punkte voneinander getrennt sind, stellen die Bögen und Blätter in einer Registrierungsstelle dar, die das Objekt und die Organisation, die es registriert hat, eindeutig identifizieren. Beispiel: die vorangehende OID kann auf Joint-ISO-ITU-t (2) Country (16) US (840) Organization (1) gov (101) CSOR (3) nistalgorithms (4) aesalgs (1) mit angefügtem 42-Bit angehängt werden, um den Algorithmus für die Verschlüsselung des 256-Bit-AES-Verschlüsselungs Blocks (CBC

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OBJECT IDENTIFIER
-- Tag number: 0x06
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="octet-string"></a>Oktett-Zeichenfolge

Codierungstag: 0x04

Certreq.exe Name: Oktett- \_ Zeichenfolge

Eine Oktett-Zeichenfolge ist ein beliebig großes Bytearray. Im Gegensatz zum **bitstring** -Typ können bestimmten Bits und Bytes in der Zeichenfolge jedoch keine Namen zugewiesen werden. Das Wort Oktett ist eine plattformunabhängige Methode zum Verweisen auf ein Arbeitsspeicher Wort. Im Kontext der Zertifikatregistrierungs-API sind Oktett und Byte austauschbar.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OCTET STRING
-- Tag number: 0x04
---------------------------------------------------------------------
AuthorityKeyId ::= SEQUENCE 
{
  keyIdentifier       [0] IMPLICIT OCTET STRING OPTIONAL,
  certIssuer          [1] EXPLICIT NAME
  certSerialNumber    [2] IMPLICIT INTEGER OPTIONAL
}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN. 1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Der-Codierung von ASN. 1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




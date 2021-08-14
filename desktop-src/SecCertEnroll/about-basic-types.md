---
description: Die Zertifikatregistrierungs-API unterstützt die folgenden grundlegenden ASN.1-Typen.
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: Grundlegende Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e2cc1b8825872789d095616e868fe39e306736583f8ea1784543808b7ec4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905045"
---
# <a name="basic-types"></a>Grundlegende Typen

Die Zertifikatregistrierungs-API unterstützt die folgenden grundlegenden ASN.1-Typen.

## <a name="bit-string"></a>BIT STRING

Codierungstag: 0x03

Certreq.exe Name: BIT \_ STRING

Ein Bit oder eine binäre Zeichenfolge ist ein beliebig langes Array von Bits. Bestimmte Bits können durch ganze Zahlen in Klammern und zugewiesene Namen identifiziert werden, wie im folgenden Beispiel zu sehen.

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

Zertifikatschlüssel und Signaturen werden häufig als Bitzeichenfolgen dargestellt.

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

Certreq.exe Name: BOOLEAN

Ein boolescher Typ kann einen von zwei Werten enthalten: **TRUE** oder **FALSE.** Das folgende Beispiel zeigt die ASN.1-Struktur für eine Basic Constraints-Zertifikaterweiterung. Das **Feld cA** gibt an, ob ein Zertifikatsubjekt eine Zertifizierungsstelle ist. Die Standardkritischität ist **FALSE.**

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

Certreq.exe Name: INTEGER

Eine ganze Zahl kann in der Regel ein beliebiger positiver oder negativer Ganzzahlwert sein. Das folgende Beispiel zeigt die ASN.1-Struktur für einen öffentlichen RSA-Schlüssel. Beachten Sie, dass das Feld **publicExponent** auf eine positive ganze Zahl kleiner als 4.294.967.296 beschränkt ist.

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

Certreq.exe Name: **NULL**

Ein **NULL-Typ** enthält ein einzelnes Byte 0x00. Sie kann überall dort verwendet werden, wo die Zertifikatanforderung einen leeren Wert angeben muss. Beispielsweise ist ein **AlgorithmIdentifier** eine Sequenz, die einen Objektbezeichner (OID) und optionale Parameter enthält.

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

Wenn beim Codieren der Struktur keine Parameter vorhanden sind, wird **NULL** verwendet, um einen leeren Wert anzugeben.

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a>OBJEKTBEZEICHNER

Codierungstag: 0x06

Certreq.exe Name: \_ OBJEKT-ID

Die Zertifikatregistrierungs-API verwendet Objektbezeichner (OIDs) als Typ universeller Zeiger auf Algorithmusbezeichner, Attribute und andere PKI-Elemente. OIDs werden in der Regel in einer gepunkteten Dezimalzeichenfolge wie "2.16.840.1.101.3.4.1.42" dargestellt. Die einzelnen Elemente in der Zeichenfolge, die durch Punkte getrennt sind, stellen die Bogen und Blätter in einer Registrierungsautoritätsstruktur dar, die das Objekt und die Organisation, die es registriert hat, eindeutig identifiziert. Beispielsweise kann die vorherige OID auf joint-iso-itu-t(2) country(16) us(840) organization(1) gov(101) csor(3) nistAlgorithms(4) aesAlgs(1) mit .42 erweitert werden, um den Algorithmus der 256-Bit-AES-Verschlüsselungsblockverkettung (CBC) eindeutig zu identifizieren.

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

## <a name="octet-string"></a>OKTETTZEICHENFOLGE

Codierungstag: 0x04

Certreq.exe Name: OCTET \_ STRING

Eine Oktettzeichenfolge ist ein beliebig großes Bytearray. Im Gegensatz zum **BIT STRING-Typ** können bestimmten Bits und Bytes in der Zeichenfolge jedoch keine Namen zugewiesen werden. Das Wort Oktett ist eine plattformunabhängige Möglichkeit, auf ein Speicherwort zu verweisen. Im Kontext der Zertifikatregistrierungs-API sind Oktett und Byte austauschbar.

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

[ASN.1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[DER-Codierung von ASN.1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




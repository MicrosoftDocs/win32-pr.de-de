---
description: Die Zertifikatregistrierungs-API verwendet asn.1 (Abstract Syntax Notation One) zum Definieren, Codieren und Decodieren der Zertifikatanforderungen und Zertifikate, die zwischen Clientcomputern und Zertifizierungsstellen übertragen werden.
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: Einführung in die ASN.1-Syntax und -Codierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504f6e643d91951351eaef2c51f9cfeac01919c77718a88ce866670f22803146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904229"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a>Einführung in die ASN.1-Syntax und -Codierung

Die Zertifikatregistrierungs-API verwendet asn.1 (Abstract Syntax Notation One) zum Definieren, Codieren und Decodieren der Zertifikatanforderungen und Zertifikate, die zwischen Clientcomputern und Zertifizierungsstellen übertragen werden. ASN.1 kann konzeptionell in einen Satz von Syntaxregeln und einen Satz von Codierungsregeln unterteilt werden, wie in den folgenden Beispielen gezeigt.

## <a name="asn1-syntax-example"></a>Asn.1-Syntaxbeispiel

Eine Zertifikatanforderung enthält unter anderem den Namen der Entität, die die Anforderung stellt oder für die die Anforderung erfolgt. Der Name ist eine Sequenz relativer Distinguished Names (RDNs) von X.500. Jeder RDN in der Sequenz besteht aus einem Objektbezeichner (OID) und einem Wert. Die ASN.1-Syntax für einen Antragstellernamen wird im folgenden Beispiel gezeigt.

``` syntax
---------------------------------------------------------------------
-- Subject name
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}
```

## <a name="asn1-encoding-example"></a>BEISPIEL FÜR ASN.1-Codierung

Die Zertifikatregistrierungs-API verwendet [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER), um den vorherigen Antragstellernamen zu codieren. DER erfordert, dass jedes Element im Namen durch ein TLV-Triplet dargestellt wird, wobei T die Tagnummer des ASN.1-Typs, L die Länge und V den zugeordneten Wert enthält. Das folgende Beispiel zeigt, wie der Antragstellername TestCN.TestOrg codiert wird.

``` syntax
1.     30 23            ; SEQUENCE (23 Bytes)
2.     |  |  31 0f            ; SET (f Bytes)
3.     |  |  |  30 0d            ; SEQUENCE (d Bytes)
4.     |  |  |     06 03         ; OBJECT_ID (3 Bytes)
5.     |  |  |     |  55 04 03
6.     |  |  |     |     ; 2.5.4.3 Common Name (CN)
7.     |  |  |     13 06         ; PRINTABLE_STRING (6 Bytes)
8.     |  |  |        54 65 73 74 43 4e                    ; TestCN
9.     |  |  |           ; "TestCN"
10.    |  |  31 10            ; SET (10 Bytes)
11.    |  |     30 0e            ; SEQUENCE (e Bytes)
12.    |  |        06 03         ; OBJECT_ID (3 Bytes)
13.    |  |        |  55 04 0a
14.    |  |        |     ; 2.5.4.10 Organization (O)
15.    |  |        13 07         ; PRINTABLE_STRING (7 Bytes)
16.    |  |           54 65 73 74 4f 72 67                 ; TestOrg
17.    |  |              ; "TestOrg"
```

Beachten Sie folgende Punkte:

-   Zeile 1:<dl> Der Name ist eine Sequenz relativer Distinguished Names.  
    Die Tagnummer für den **SEQUENCE-Typ** ist 0x30.  
    Der Antragstellername von TestCN.TestOrg erfordert 35 (0x23) Bytes.  
    </dl>
-   Line 2:<dl> Der allgemeine Name TestCN ist ein einzelner Satz von **AttributeTypeValue-Strukturen.**  
    Die Tagnummer für einen **SET** wird 0x31.  
    </dl>
-   Zeile 3:<dl> Die **AttributeTypeValue-Struktur** ist eine Sequenz.  
    Die Tagnummer für den **SEQUENCE-Typ** ist 0x30.  
    Die -Struktur erfordert 13 (0xD) Bytes.  
    </dl>
-   Zeilen 4 bis 6:<dl> Der Objektbezeichner (OID) für den allgemeinen Namen ist 2.5.4.3.  
    Die OID ist ein **\_ OBJEKT-ID-Typ** mit drei Byte.  
    Die Tagnummer für den **\_ OBJEKT-ID-Typ** ist 0x06.  
    </dl>
-   Zeilen 7 bis 9:<dl> Der allgemeine Name TestCN ist ein Zeichenfolgenwert.  
    Die Zeichenfolge ist ein **PRINTABLE \_ STRING-Typ** mit sechs Byte.  
    Die Tagnummer für den **PRINTABLE \_ STRING-Typ** ist 0x13.  
    </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN.1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Zertifikatanforderungscodierung](about-certificate-request-encoding.md)
</dt> <dt>

[DER-Codierung von ASN.1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 

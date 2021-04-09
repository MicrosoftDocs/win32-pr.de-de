---
description: Die Zertifikatregistrierungs-API verwendet die abstrakte Syntax Notation One (ASN. 1) zum definieren, codieren und Decodieren der Zertifikat Anforderungen und Zertifikate, die zwischen Client Computern und Zertifizierungsstellen übertragen werden.
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: Einführung in die ASN. 1-Syntax und-Codierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4fe15d2fb8fba4af25b9da7c249fec3a92630e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865031"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a>Einführung in die ASN. 1-Syntax und-Codierung

Die Zertifikatregistrierungs-API verwendet die abstrakte Syntax Notation One (ASN. 1) zum definieren, codieren und Decodieren der Zertifikat Anforderungen und Zertifikate, die zwischen Client Computern und Zertifizierungsstellen übertragen werden. ASN. 1 kann konzeptionell in einen Satz von Syntax Regeln und einen Satz von Codierungsregeln aufgeteilt werden, wie in den folgenden Beispielen gezeigt.

## <a name="asn1-syntax-example"></a>Beispiel für eine ASN. 1-Syntax

Eine Zertifikat Anforderung enthält unter anderem den Namen der Entität, von der die Anforderung stammt, oder für die die Anforderung ausgeführt wird. Der Name ist eine Sequenz von X. 500 Relative Distinguished Names (rDNS). Jeder RDN in der Sequenz besteht aus einem Objekt Bezeichner (OID) und einem Wert. Die ASN. 1-Syntax für einen Betreffnamen ist im folgenden Beispiel dargestellt.

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

## <a name="asn1-encoding-example"></a>ASN. 1-Codierungs Beispiel

Die Zertifikatregistrierungs-API verwendet [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) zum Codieren des vorangehenden Antragsteller namens. Der erfordert, dass jedes Element im Namen durch ein TLV-Element dargestellt wird, wobei T die Tagnummer des ASN. 1-Typs enthält, L die Länge und V den zugeordneten Wert enthält. Im folgenden Beispiel wird gezeigt, wie der Antragsteller Name "testcn. testorg" codiert ist.

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

-   Zeile 1:<dl> Der Name ist eine Sequenz von relativen Distinguished Names.  
    Die Tagnummer für den **Sequenztyp** ist 0x30.  
    Der Antragsteller Name von testcn. testorg erfordert 35 (0x23) Bytes.  
    </dl>
-   Line 2:<dl> Der allgemeine Name, testcn, ist ein einzelner Satz von **attributetypevalue** -Strukturen.  
    Die Tagnummer für eine **Menge** ist 0x31.  
    </dl>
-   Zeile 3:<dl> Die **attributetypevalue** -Struktur ist eine Sequenz.  
    Die Tagnummer für den **Sequenztyp** ist 0x30.  
    Die-Struktur erfordert 13 (0xD) Bytes.  
    </dl>
-   Zeilen 4 bis 6:<dl> Der Objekt Bezeichner (OID) für den allgemeinen Namen ist 2.5.4.3.  
    Die OID ist ein Objekt- **\_ ID** -Typ mit drei Bytes.  
    Die Tagnummer für den **Objekt- \_ ID** -Typ ist 0x06.  
    </dl>
-   Zeilen 7 bis 9:<dl> Der allgemeine Name, testcn, ist ein Zeichen folgen Wert.  
    Die Zeichenfolge ist ein **druckbarer \_ Zeichen** Folgentyp mit sechs Byte.  
    Die Tagnummer für den Typ der **druckbaren \_ Zeichenfolge** ist 0x13.  
    </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN. 1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Zertifikat Anforderungs Codierung](about-certificate-request-encoding.md)
</dt> <dt>

[Der-Codierung von ASN. 1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 

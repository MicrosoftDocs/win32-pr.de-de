---
description: Der Datentyp ASN. 1 bmpstring, der als Unicode- \_ Zeichenfolge in der Zertifikatregistrierungs-API bezeichnet wird, wird in ein TLV-Dreieck codiert, das mit einem tagbyte von 0x1E beginnt.
ms.assetid: 66e4a6d8-2401-4346-9361-e145735cbe19
title: Bmpstring
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c911218d852b792a333f015c825a7e4d1486b62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216007"
---
# <a name="bmpstring"></a>Bmpstring

Der Datentyp ASN. 1 **bmpstring** , der als **Unicode- \_ Zeichenfolge** in der Zertifikatregistrierungs-API bezeichnet wird, wird in ein TLV-Dreieck codiert, das mit einem **tagbyte** von 0x1E beginnt. Im folgenden Beispiel, das aus dem Thema " [CMC-codierte ASN. 1](cmc-encoded-asn-1.md) " angepasst wurde, wird die Codierung für eine **templatename** -Erweiterung gezeigt. Der Name kann mithilfe der [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) -Schnittstelle angegeben werden. Der Objekt Bezeichner für die Erweiterung ist 1.3.6.1.4.1.311.13.2.1.

``` syntax
06 0a                              ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 01  ;   1.3.6.1.4.1.311.13.2.1 
31 34                              ; SET (34 Bytes)
   30 32                           ; SEQUENCE (32 Bytes)
      1e 26                        ; UNICODE_STRING (26 Bytes)
      |  00 43 00 65 00 72 00 74   ;   .C.e.r.t
      |  00 69 00 66 00 69 00 63   ;   .i.f.i.c
      |  00 61 00 74 00 65 00 54   ;   .a.t.e.T
      |  00 65 00 6d 00 70 00 6c   ;   .e.m.p.l
      |  00 61 00 74 00 65         ;   .a.t.e
      1e 08                        ; UNICODE_STRING (8 Bytes)
         00 55 00 73 00 65 00 72   ;   .U.s.e.r
```

Wenn die Zeichenfolge weniger als 128 Bytes enthält, benötigt das **Längen** Feld des TLV-Dreiecks nur ein Byte, um die Inhalts Länge anzugeben. Wenn die Zeichenfolge mehr als 127 Bytes beträgt, wird Bit 7 des **Längen** Felds auf 1 festgelegt, und Bits 6 bis 0 geben Sie die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhalts Länge verwendet werden. Weitere Informationen finden Sie unter [codierte Länge und Wert Bytes](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN. 1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Der-Codierung von ASN. 1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




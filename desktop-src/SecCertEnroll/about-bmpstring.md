---
description: Der BMPString-Datentyp ASN.1, der in der Zertifikatregistrierungs-API als UNICODE STRING bezeichnet wird, wird in ein TLV-Triplet codiert, das mit einem \_ Tag-Byte 0x1E.
ms.assetid: 66e4a6d8-2401-4346-9361-e145735cbe19
title: BMPString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 496715d380739dd68dab4266422876ecca174b9caffd3895e9c465f446d32cf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904839"
---
# <a name="bmpstring"></a>BMPString

Der ASN.1 **BMPString-Datentyp,** der in der Zertifikatregistrierungs-API als **UNICODE \_ STRING** bezeichnet wird, wird in ein TLV-Triplet codiert, das mit einem **Tag-Byte** von 0x1E. Das folgende Beispiel, das aus dem [Thema CMC-codierte ASN.1](cmc-encoded-asn-1.md) angepasst wurde, zeigt die Codierung für eine **TemplateName-Erweiterung.** Der Name kann mithilfe der [**IX509ExtensionTemplateName-Schnittstelle angegeben**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) werden. Der Objektbezeichner für die Erweiterung ist 1.3.6.1.4.1.311.13.2.1.

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

Wenn die Zeichenfolge weniger als 128 Bytes enthält, benötigt das **Feld Length** des TLV-Triplets nur ein Byte, um die Inhaltslänge anzugeben. Wenn die Zeichenfolge mehr als 127 Bytes beträgt, wird Bit 7 des **Felds Length** auf 1 festgelegt, und die Bits 6 bis 0 geben die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhaltslänge verwendet werden. Weitere Informationen finden Sie unter [Codierte Länge und Wertbytes.](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN.1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[DER-Codierung von ASN.1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




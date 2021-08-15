---
description: Der ASN.1 OCTET STRING-Datentyp wird in ein TLV-Triplet codiert, das mit einem Tag-Byte 0x04.
ms.assetid: 9d07a6c8-a15f-4030-838c-3063e315684f
title: OKTETT-ZEICHENFOLGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588547e5211efbe6b4b91a8a72f6644de0c7c4dcbacc570f0a1f272e7cc97962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903744"
---
# <a name="octet-string"></a>OKTETT-ZEICHENFOLGE

Der ASN.1 **OCTET STRING-Datentyp** wird in ein TLV-Triplet codiert, das mit einem **Tag-Byte** 0x04. Die **Datentypen OCTET STRING** und [BIT STRING](about-bit-string.md) sind sehr ähnlich. Daher werden die beiden Typen auf ähnliche Weise codiert, mit der Ausnahme, dass dem Inhalt keine führenden Bytes hinzugefügt werden müssen, da das nachführende Byte einer **OCTET-ZEICHENFOLGE** keine nicht verwendeten Bits enthalten darf. Das folgende Beispiel, das aus dem [THEMA CMC-codierte ASN.1](cmc-encoded-asn-1.md) angepasst wurde, zeigt, wie der Name einer Zertifikatvorlage als Bytearray codiert wird.

``` syntax
30 17                                 ; SEQUENCE (17 Bytes)
|  06 09                              ; OBJECT_ID (9 Bytes)
|  |  2b 06 01 04 01 82 37 14  02     ;   1.3.6.1.4.1.311.20.2
|  04 0a                              ; OCTET_STRING (a Bytes)
|     1e 08 00 55 00 73 00 65  00 72  ;   ...U.s.e.r
```

Wenn das Bytearray weniger als 128 Bytes enthält, benötigt das **Feld Length** des TLV-Triplets nur ein Byte, um die Inhaltslänge anzugeben. Wenn es sich um mehr als 127 Bytes handelt, wird Bit 7 des **Felds Length** auf 1 festgelegt, und die Bits 6 bis 0 geben die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhaltslänge verwendet werden. Dies wird im folgenden Beispiel gezeigt, in dem das obere Bit des zweiten Byte in der ersten  Zeile auf 1 festgelegt ist und das Byte angibt, dass es ein nachfolgendes Length-Byte gibt. Das dritte Byte gibt daher an, dass der Inhalt 0x80 Bytes lang ist.

``` syntax
04 81 80                       ; OCTET_STRING (80 Bytes)
   38 10 60 e2 70 69 91 4a     ;   8.`.pi.J
   8b b5 22 57 2a 62 ef de     ;   .."W*b..
   15 7d 59 d6 4e 20 9a 45     ;   .}Y.N .E
   2b e3 fd fc 68 ba af bf     ;   +...h...
   9c 17 b0 8e 6d c4 29 1e     ;   ....m.).
   e3 21 ac bb 5a 8a c9 67     ;   .!..Z..g
   0a d4 45 93 10 c0 26 eb     ;   ..E...&.
   0a 83 c2 b1 40 87 36 f7     ;   ....@.6.
   a0 26 da b9 bb 46 73 88     ;   .&...Fs.
   7a 67 b9 e6 b3 6f ea 59     ;   zg...o.Y
   28 8a d3 92 72 f6 7b 89     ;   (...r.{.
   a0 d8 2d 9e 40 eb 1e bb     ;   ..-.@...
   6e ae f0 5a ed 16 c9 e3     ;   n..Z....
   27 59 37 8f f3 4a 98 60     ;   'Y7..J.`
   f8 fb a7 0a ee 1b 6e 91     ;   ......n.
   95 96 cf 0d 56 ac ab 35     ;   ....V..5
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN.1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[DER-Codierung von ASN.1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




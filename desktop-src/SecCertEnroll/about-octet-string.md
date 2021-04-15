---
description: Der Datentyp der ASN. 1-Oktett-Zeichenfolge wird in eine TLV-Kette codiert, die mit einem tagbyte von 0x04 beginnt.
ms.assetid: 9d07a6c8-a15f-4030-838c-3063e315684f
title: Oktett-Zeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed2a042312a4415ea9554b7519404097287244f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485419"
---
# <a name="octet-string"></a>Oktett-Zeichenfolge

Der Datentyp der ASN. 1- **Oktett-Zeichenfolge** wird in eine TLV-Kette codiert, die mit einem **tagbyte** von 0x04 beginnt. Die Datentypen der **Oktett-Zeichenfolge** und der [Bitzeichenfolge](about-bit-string.md) sind sehr ähnlich. Folglich werden die beiden Typen auf ähnliche Weise codiert, es sei denn, das nachfolgende Byte einer **Oktett-Zeichenfolge** darf keine nicht verwendeten Bits aufweisen. dem Inhalt müssen keine führenden Bytes hinzugefügt werden. Das folgende Beispiel, das aus dem Thema " [CMC-codiertes ASN. 1](cmc-encoded-asn-1.md) " angepasst wurde, zeigt, wie der Name einer Zertifikat Vorlage als Bytearray codiert wird.

``` syntax
30 17                                 ; SEQUENCE (17 Bytes)
|  06 09                              ; OBJECT_ID (9 Bytes)
|  |  2b 06 01 04 01 82 37 14  02     ;   1.3.6.1.4.1.311.20.2
|  04 0a                              ; OCTET_STRING (a Bytes)
|     1e 08 00 55 00 73 00 65  00 72  ;   ...U.s.e.r
```

Wenn das Bytearray weniger als 128 Bytes enthält, benötigt das **Längen** Feld des TLV-Dreiecks nur ein Byte, um die Inhalts Länge anzugeben. Wenn Sie mehr als 127 Bytes hat, wird Bit 7 des **Längen** Felds auf 1 festgelegt, und Bits 6 bis 0 geben Sie die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhalts Länge verwendet werden. Dies wird im folgenden Beispiel gezeigt, bei dem das High-Order-Bit des zweiten Bytes in der ersten Zeile auf 1 festgelegt ist und das Byte angibt, dass ein nach gestelltes **Längen** Byte vorliegt. Das dritte Byte gibt daher an, dass der Inhalt 0x80 Bytes lang ist.

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

[ASN. 1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Der-Codierung von ASN. 1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




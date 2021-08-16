---
description: Ganzzahlige Werte werden in ein TLV-Triplet codiert, das mit dem Tagwert 0x02.
ms.assetid: a6fed62f-af59-488c-a690-be8c3413086f
title: INTEGER (Zertifikatregistrierungs-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85151947653a66c98b7a030ade7b9ff7b4f5ee87fd84edc4cc52679be296a1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904342"
---
# <a name="integer-certificate-enrollment-api"></a>INTEGER (Zertifikatregistrierungs-API)

Ganzzahlige Werte werden in ein TLV-Triplet codiert, das mit dem **Tagwert** 0x02. Das **Feld Wert** des TLV-Triplets enthält die codierte ganze Zahl, wenn sie positiv ist, oder das Komplement der beiden Werte, wenn sie negativ ist. Wenn die ganze Zahl positiv ist, das obere Bit jedoch auf 1 festgelegt ist, wird dem Inhalt eine führende 0x00 hinzugefügt, um anzugeben, dass die Zahl nicht negativ ist. Beispielsweise ist das obere Byte 0x8F (10001111) 1. Aus diesem Grund wird dem Inhalt ein führendes 0 Byte hinzugefügt, wie in der folgenden Abbildung dargestellt.

![der Codierung des booleschen Datentyps](images/der-tlv-integer.png)

Wenn die ganze Zahl weniger als 128 Bytes enthält, benötigt das *Feld Length* nur ein Byte, um die Inhaltslänge anzugeben. Wenn die ganze Zahl größer als 127 Bytes ist, wird Bit 7 des *Felds Length* auf 1 festgelegt, und die Bits 6 bis 0 geben die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhaltslänge verwendet werden. Weitere Informationen finden Sie unter [Codierte Länge und Wertbytes.](about-encoded-length-and-value-bytes.md)

Das folgende Beispiel aus [PKCS \# 10 Encoded ASN.1](pkcs--10-encoded-asn-1.md)zeigt die Codierung für einen öffentlichen 128-Byte-Schlüssel. Das erste Byte enthält den **Tag-Wert** für den **INTEGER-Datentyp** 0x02. Das zweite und dritte Bytes enthalten den **Length-Wert.** Bit 7 des zweiten Byte wird auf 1 festgelegt, da mehr als 127 Bytes Inhalt enthalten. Bits 0 bis 6 des zweiten Byte geben die Anzahl der nach folgenden Bytes an, die in diesem Fall erforderlich sind, um die Inhaltslänge genau anzugeben. Das dritte Byte gibt die Anzahl der Inhaltsbytes an, 0x81. Das vierte Byte, 0x00, wird dem Inhalt hinzugefügt, um anzugeben, dass die ganze Zahl tatsächlich ein positiver Wert ist, obwohl das Vorzeichenbit des führenden Inhalts byte (0x8F) auf 1 festgelegt ist.

``` syntax
02 81 81          ; INTEGER (81 Bytes)
|  00
|  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
```

Das folgende Beispiel zeigt, wie der ganzzahlige 0x03 codiert wird. Das  Tag-Byte enthält 0x02, und das **Length-Byte** gibt an, dass ein Byte Inhalt enthalten ist.

``` syntax
02 01             ; INTEGER (1 Bytes)
|  03
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN.1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[DER-Codierung von ASN.1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




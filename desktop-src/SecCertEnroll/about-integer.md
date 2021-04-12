---
description: Ganzzahlige Werte werden in ein TLV-Dreieck codiert, das mit dem Tagwert 0x02 beginnt.
ms.assetid: a6fed62f-af59-488c-a690-be8c3413086f
title: Ganzzahl (Zertifikatregistrierungs-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0e8ed162d4cf4b2ac4909baf1cd7b5e94ddea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345438"
---
# <a name="integer-certificate-enrollment-api"></a>Ganzzahl (Zertifikatregistrierungs-API)

Ganzzahlige Werte werden in ein TLV-Dreieck codiert, das mit dem **Tagwert** 0x02 beginnt. Das **Wertfeld** des TLV-Zweigs enthält die codierte Ganzzahl, wenn Sie positiv ist, oder die zwei Komplement, wenn Sie negativ ist. Wenn die ganze Zahl positiv ist, aber das hohe Bestell Bit auf 1 festgelegt ist, wird dem Inhalt eine führende 0x00 hinzugefügt, um anzugeben, dass die Zahl nicht negativ ist. Beispielsweise ist das hochwertigen Byte von 0x8F (10001111) 1. Daher wird dem Inhalt ein führendes NULL-Byte hinzugefügt, wie in der folgenden Abbildung dargestellt.

![der-Codierung des booleschen Datentyps.](images/der-tlv-integer.png)

Wenn die ganze Zahl weniger als 128 Bytes enthält, benötigt das *Längen* Feld nur ein Byte, um die Inhalts Länge anzugeben. Wenn die Ganzzahl mehr als 127 Bytes beträgt, wird Bit 7 des *Längen* Felds auf 1 festgelegt, und Bits 6 bis 0 geben Sie die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhalts Länge verwendet werden. Weitere Informationen finden Sie unter [codierte Länge und Wert Bytes](about-encoded-length-and-value-bytes.md).

Im folgenden Beispiel wird aus [PKCS \# 10-codiertem ASN. 1](pkcs--10-encoded-asn-1.md)die Codierung für einen öffentlichen Schlüssel mit 128 Byte veranschaulicht. Das erste Byte enthält den **Tagwert** des **ganzzahligen** Datentyps 0x02. Das zweite und das dritte Byte enthalten den **Längen** Wert. Bit 7 des zweiten Bytes ist auf 1 festgelegt, da mehr als 127 Bytes Inhalt vorhanden sind. Bits 0 bis 6 des zweiten Bytes geben Sie die Anzahl der nachfolgenden Bytes an, die in diesem Fall eine genaue Angabe der Inhalts Länge benötigen. Das dritte Byte gibt die Anzahl der Inhalts Bytes an, 0x81. Das vierte Byte, 0x00, wird dem-Inhalt hinzugefügt, um anzugeben, dass die ganze Zahl tatsächlich ein positiver Wert ist, auch wenn das Signier Bit des führenden Inhalts bytes (0x8F) auf 1 festgelegt ist.

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

Im folgenden Beispiel wird gezeigt, wie der ganzzahlige Wert 0x03 codiert wird. Das **tagbyte** enthält 0x02, und das **length** -Byte gibt an, dass ein Byte Inhalt vorhanden ist.

``` syntax
02 01             ; INTEGER (1 Bytes)
|  03
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN. 1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Der-Codierung von ASN. 1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




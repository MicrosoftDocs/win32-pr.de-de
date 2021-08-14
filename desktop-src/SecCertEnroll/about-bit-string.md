---
description: Der BIT STRING-Datentyp wird in ein TLV-Triplet codiert, das mit einem Tag-Byte 0x03.
ms.assetid: 7464dd20-5e79-4ca1-a6ae-9b706e9cb925
title: BIT STRING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056616a22cf2e683e943afef9369ed4c885963174aff0e72dea6ef718ddbdf7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905060"
---
# <a name="bit-string"></a>BIT STRING

Der **BIT STRING-Datentyp** wird in ein TLV-Triplet codiert, das mit einem **Tag-Byte** 0x03. Das **Feld Wert** des TLV-Triplets enthält ein führendes Byte, das die Anzahl der Bits angibt, die im endgültigen Byte des Inhalts nicht verwendet werden. Im folgenden Beispiel wird das Feld **Length** auf 0x03 festgelegt, da drei Inhaltsbytes folgen, und das führende Byte des Felds **Value** wird auf 0x04 festgelegt, da im letzten Inhaltsbyte vier nicht verwendete Bits enthalten sind. Jedes nicht verwendete Bit wird durch den Buchstaben x bezeichnet.

![Der-Codierung des Bitzeichenfolgen-Datentyps](images/der-tlv-bitstring.png)

Das folgende Beispiel, das aus dem [PKCS \# 10 Encoded ASN.1-Thema](pkcs--10-encoded-asn-1.md) angepasst wurde, zeigt die codierte Signatur einer PKCS \# 10-Beispielzertifikatanforderung. Das erste Byte enthält den **Tagwert** für den **BIT STRING-Datentyp** 0x03. Das zweite und dritte Bytes enthalten die Länge des Bytearrays. Bit 7 des zweiten Byte wird auf 1 festgelegt, da mehr als 127 Bytes Inhalt enthalten. Bits 0 bis 6 des zweiten Byte  geben die Anzahl der nach folgenden Längenbytes an, in diesem Fall eins. Das dritte Byte gibt die Anzahl der Inhaltsbytes an, 0x81. Das vierte Byte, 0x00, gibt die Anzahl der nicht verwendeten Bits an, die im letzten Inhalts-Byte vorhanden sind. Beachten Sie, dass die Signatur in Big-Endian-Byte-Reihenfolge codiert ist.

``` syntax
0299:    03 81 81           ; BIT_STRING (81 Bytes)
029c:       00
029d:       47 eb 99 5a df 9e 70 0d  fb a7 31 32 c1 5f 5c 24
02ad:       c2 e0 bf c6 24 af 15 66  0e b8 6a 2e ab 2b c4 97
02bd:       1f e3 cb dc 63 a5 25 ec  c7 b4 28 61 66 36 a1 31
02cd:       1b bf dd d0 fc bf 17 94  90 1d e5 5e c7 11 5e c9
02dd:       55 9f eb a3 3e 14 c7 99  a6 cb ba a1 46 0f 39 d4
02ed:       44 c4 c8 4b 76 0e 20 5d  6d a9 34 9e d4 d5 87 42
02fd:       eb 24 26 51 14 90 b4 0f  06 5e 52 88 32 7a 95 20
030d:       a0 fd f7 e5 7d 60 dd 72  68 9b f5 7b 05 8f 6d 1e
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN.1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[DER-Codierung von ASN.1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Codierte Längen- und Wertbytes](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 




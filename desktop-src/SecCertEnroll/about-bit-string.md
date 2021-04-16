---
description: Der bitstring-Datentyp wird in eine TLV-Kette codiert, die mit einem tagbyte von 0x03 beginnt.
ms.assetid: 7464dd20-5e79-4ca1-a6ae-9b706e9cb925
title: Bitzeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115ead46663b94d6db2d089f1fae2fd8c40a2ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553408"
---
# <a name="bit-string"></a>Bitzeichenfolge

Der **bitstring** -Datentyp wird in eine TLV-Kette codiert, die mit einem **tagbyte** von 0x03 beginnt. Das **Wertfeld** des TLV-Dreiecks enthält ein führendes Byte, das die Anzahl der Bits angibt, die im letzten Byte des Inhalts nicht verwendet werden. Im folgenden Beispiel wird das **Längen** Feld auf 0x03 festgelegt, da drei Inhalts Bytes befolgt werden und das führende Byte des **Wertfelds** auf 0x04 festgelegt ist, weil im letzten Inhalts Byte vier nicht verwendete Bits vorhanden sind. Alle nicht verwendeten Bits werden durch den Buchstaben x gekennzeichnet.

![der-Codierung des bitstring-Datentyps](images/der-tlv-bitstring.png)

Das folgende Beispiel, das aus dem [PKCS \# 10-codierten ASN. 1](pkcs--10-encoded-asn-1.md) -Thema angepasst wurde, zeigt die codierte Signatur einer PKCS 10-Beispiel \# Zertifikat Anforderung. Das erste Byte enthält den **Tagwert** für den **Bit-Zeichen** folgen-Datentyp 0x03. Das zweite und das dritte Byte enthalten die Länge des Byte Arrays. Bit 7 des zweiten Bytes ist auf 1 festgelegt, da mehr als 127 Bytes Inhalt vorhanden sind. Bits 0 bis 6 des zweiten Bytes geben Sie die Anzahl der nachfolgenden **Länge** von Bytes an, in diesem Fall 1. Das dritte Byte gibt die Anzahl der Inhalts Bytes an, 0x81. Das vierte Byte, 0x00, gibt die Anzahl der nicht verwendeten Bits an, die im letzten Inhalts Byte vorhanden sind. Beachten Sie, dass die Signatur in Big-Endian-Byte Reihenfolge codiert ist.

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

[ASN. 1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Der-Codierung von ASN. 1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Codierte Länge und Wert Bytes](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 




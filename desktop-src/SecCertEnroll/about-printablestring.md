---
description: Der Asn.1 PrintableString-Datentyp wird in ein TLV-Triplet codiert, das mit einem Tag-Byte von 0x13 beginnt.
ms.assetid: 998fef66-7a24-462f-96f2-92c739bbefa2
title: PrintableString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e2714013c037e834a7c083c7ab89fcdafd59e1306226af25fcb4b6edc8b0af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903752"
---
# <a name="printablestring"></a>PrintableString

Der ASN.1 **PrintableString-Datentyp** wird in ein TLV-Triplet codiert, das mit einem **Tag-Byte** von 0x13 beginnt. Das folgende Beispiel aus dem [Thema PKCS \# 10-codierte ASN.1](pkcs--10-encoded-asn-1.md) zeigt, wie ein allgemeiner Benutzername von TestCN als **PrintableString-Typ** codiert wird. Der Objektbezeichner für einen allgemeinen Namen ist 2.5.4.3.

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

Wenn die Zeichenfolge weniger als 128 Bytes enthält, benötigt das **Feld Length** des TLV-Triplets nur ein Byte, um die Inhaltslänge anzugeben. Wenn die Zeichenfolge mehr als 127 Bytes beträgt, wird Bit 7 des **Felds Length** auf 1 festgelegt, und die Bits 6 bis 0 geben die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhaltslänge verwendet werden. Weitere Informationen finden Sie unter [Codierte Länge und Wertbytes.](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN.1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[DER-Codierung von ASN.1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




---
description: Der ASN.1 IA5tring-Datentyp wird in ein TLV-Triplet codiert, das mit einem Tag-Byte von 0x16 beginnt.
ms.assetid: c1268524-4304-4c21-8f7d-f0a2826cd74e
title: IA5String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5d602f50a7a3c22cd4a57d6531603307b9f14e02c537692c200a1b19fc361e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904239"
---
# <a name="ia5string"></a>IA5String

Der ASN.1 **IA5tring-Datentyp** wird in ein TLV-Triplet codiert, das mit einem **Tag-Byte** von 0x16 beginnt. Das folgende Beispiel wurde aus dem [THEMA CMC-codierte ASN.1](cmc-encoded-asn-1.md) angepasst und zeigt, wie das **OSVersion-Attribut** als **IA5tring-Typ** codiert wird. Die Versionsnummer kann mithilfe der [**IX509AttributeOSVersion-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) angegeben werden. Der Objektbezeichner für das Attribut ist 1.3.6.1.4.1.311.13.2.3.

``` syntax
06 0a                                   ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 03       ;   1.3.6.1.4.1.311.13.2.3 
31 0c                                   ; SET (c Bytes)
   16 0a                                ; IA5_STRING (a Bytes)
      36 2e 30 2e 35 33 36 31  2e 32    ;   6.0.5361.2
```

Wenn die Zeichenfolge weniger als 128 Bytes enthält, benötigt das **Feld Length** des TLV-Triplets nur ein Byte, um die Inhaltslänge anzugeben. Wenn die Zeichenfolge mehr als 127 Bytes beträgt, wird Bit 7 des **Felds Length** auf 1 festgelegt, und die Bits 6 bis 0 geben die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhaltslänge verwendet werden. Weitere Informationen finden Sie unter [Codierte Länge und Wertbytes.](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN.1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[DER-Codierung von ASN.1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




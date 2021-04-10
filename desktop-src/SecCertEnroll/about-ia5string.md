---
description: Der ASN. 1 IA5tring-Datentyp wird in ein TLV-Dreieck codiert, das mit einem tagbyte von 0x16 beginnt.
ms.assetid: c1268524-4304-4c21-8f7d-f0a2826cd74e
title: IA5String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7562fab655462455b03d35041bdb8f572b064cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216008"
---
# <a name="ia5string"></a>IA5String

Der ASN. 1 **IA5tring** -Datentyp wird in ein TLV-Dreieck codiert, das mit einem **tagbyte** von 0x16 beginnt. Das folgende Beispiel, das aus dem Thema " [CMC-codiertes ASN. 1](cmc-encoded-asn-1.md) " angepasst wurde, zeigt, wie das **OSVersion** -Attribut als **IA5tring** -Typ codiert wird. Die Versionsnummer kann mithilfe der [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) -Schnittstelle angegeben werden. Der Objekt Bezeichner für das Attribut ist 1.3.6.1.4.1.311.13.2.3.

``` syntax
06 0a                                   ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 03       ;   1.3.6.1.4.1.311.13.2.3 
31 0c                                   ; SET (c Bytes)
   16 0a                                ; IA5_STRING (a Bytes)
      36 2e 30 2e 35 33 36 31  2e 32    ;   6.0.5361.2
```

Wenn die Zeichenfolge weniger als 128 Bytes enthält, benötigt das **Längen** Feld des TLV-Dreiecks nur ein Byte, um die Inhalts Länge anzugeben. Wenn die Zeichenfolge mehr als 127 Bytes beträgt, wird Bit 7 des **Längen** Felds auf 1 festgelegt, und Bits 6 bis 0 geben Sie die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhalts Länge verwendet werden. Weitere Informationen finden Sie unter [codierte Länge und Wert Bytes](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN. 1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Der-Codierung von ASN. 1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




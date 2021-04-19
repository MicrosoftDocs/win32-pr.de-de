---
description: Ein Satz enthält eine ungeordnete Reihe von Feldern von einem oder mehreren Typen.
ms.assetid: 6bbe89da-1177-4cfa-9515-03b271e5ef6b
title: SET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572114d754b5034babe81e3914599f48996867d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349408"
---
# <a name="set"></a>SET

Ein **Satz** enthält eine ungeordnete Reihe von Feldern von einem oder mehreren Typen. Sie wird in ein TLV-Dreieck codiert, das mit einem **tagbyte** von 0x31 beginnt. Das folgende Beispiel, das aus dem Thema " [CMC-codierte ASN. 1](cmc-encoded-asn-1.md) " angepasst wurde, veranschaulicht, wie ein **ClientID-** Attribut in einer **festgelegten** Datenstruktur codiert wird. Das-Attribut kann mithilfe der [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) -Schnittstelle angegeben werden.

``` syntax
31 59                                     ; SET (59 Bytes)
   30 57                                  ; SEQUENCE (57 Bytes)
      06 09                               ; OBJECT_ID (9 Bytes)
      |  2b 06 01 04 01 82 37 15  14      ;   1.3.6.1.4.1.311.21.20 
      31 4a                               ; SET (4a Bytes)
         30 48                            ; SEQUENCE (48 Bytes)
            02 01                         ; INTEGER (1 Bytes)
            |  09
            0c 23                         ; UTF8_STRING (23 Bytes)
            |  76 69 63 68 33 64 2e 6a    ;   vich3d.j
            |  64 6f 6d 63 73 63 2e 6e    ;   domcsc.n
            |  74 74 65 73 74 2e 6d 69    ;   ttest.mi
            |  63 72 6f 73 6f 66 74 2e    ;   crosoft.
            |  63 6f 6d                   ;   com
            0c 15                         ; UTF8_STRING (15 Bytes)
            |  4a 44 4f 4d 43 53 43 5c    ;   JDOMCSC\
            |  61 64 6d 69 6e 69 73 74    ;   administ
            |  72 61 74 6f 72             ;   rator
            0c 07                         ; UTF8_STRING 
```

Wenn die **Menge** weniger als 128 Bytes enthält, benötigt das **Längen** Feld des TLV-Dreiecks nur ein Byte, um die Inhalts Länge anzugeben. Wenn Sie mehr als 127 Bytes hat, wird Bit 7 des **Längen** Felds auf 1 festgelegt, und Bits 6 bis 0 geben Sie die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhalts Länge verwendet werden. Weitere Informationen finden Sie unter [codierte Länge und Wert Bytes](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN. 1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Der-Codierung von ASN. 1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




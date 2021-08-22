---
description: Der ASN.1-UTF8String-Datentyp wird in ein TLV-Triplet codiert, das mit einem Tag-Byte von 0x0C.
ms.assetid: e30737d3-8294-48d8-9e42-f21918acc73c
title: UTF8String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451b51a42d8c2b296b6c3c98c224b0052a7d89d95dbfe92483b852f6a0167b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903456"
---
# <a name="utf8string"></a>UTF8String

Der ASN.1-UTF8String-Datentyp wird in ein TLV-Triplet codiert, das mit einem **Tag-Byte** 0x0C.  Das folgende Beispiel aus dem [THEMA CMC-codierte ASN.1](cmc-encoded-asn-1.md) zeigt, wie das **ClientId-Attribut** als ganze Zahl und drei **UTF8String-Typen codiert** wird. Der Objektbezeichner für das Attribut ist 1.3.6.1.4.1.311.21.20. Die Informationen, die mithilfe der [**IX509AttributeClientId-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) angegeben werden können, umfassen eine Client-ID-Nummer, den Domain Name System-Computernamen (DNS), den SAM-Benutzernamen (Security Accounts Manager) und den Namen der Anwendung, die die Zertifikatanforderung erstellt hat.

``` syntax
06 09                                ; OBJECT_ID (9 Bytes)
|  2b 06 01 04 01 82 37 15  14       ;   1.3.6.1.4.1.311.21.20 
31 4a                                ; SET (4a Bytes)
   30 48                             ; SEQUENCE (48 Bytes)
      02 01                          ; INTEGER (1 Bytes)
      |  09
      0c 23                          ; UTF8_STRING (23 Bytes)
      |  76 69 63 68 33 64 2e 6a     ;   vich3d.j
      |  64 6f 6d 63 73 63 2e 6e     ;   domcsc.n
      |  74 74 65 73 74 2e 6d 69     ;   ttest.mi
      |  63 72 6f 73 6f 66 74 2e     ;   crosoft.
      |  63 6f 6d                    ;   com
      0c 15                          ; UTF8_STRING (15 Bytes)
      |  4a 44 4f 4d 43 53 43 5c     ;   JDOMCSC\
      |  61 64 6d 69 6e 69 73 74     ;   administ
      |  72 61 74 6f 72              ;   rator
      0c 07                          ; UTF8_STRING (7 Bytes)
         63 65 72 74 72 65 71        ;   certreq
```

Wenn die Zeichenfolge weniger als 128 Bytes enthält, benötigt das **Feld Length** des TLV-Triplets nur ein Byte, um die Inhaltslänge anzugeben. Wenn die Zeichenfolge mehr als 127 Bytes beträgt, wird Bit 7 des **Felds Length** auf 1 festgelegt, und die Bits 6 bis 0 geben die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhaltslänge verwendet werden. Weitere Informationen finden Sie unter [Codierte Länge und Wertbytes.](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN.1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[DER-Codierung von ASN.1-Typen](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




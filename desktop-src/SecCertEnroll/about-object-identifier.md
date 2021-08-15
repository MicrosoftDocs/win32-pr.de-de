---
description: Der OBJECT IDENTIFIER-Datentyp wird in ein TLV-Triplet codiert, das mit dem Tagwert 0x06.
ms.assetid: 42c015c8-3de1-4482-bf27-b19c422b8cdb
title: OBJEKTBEZEICHNER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35c2bf64424fa158eef3c666743142d5ec5a65108e3def28c43194d2eaf5adc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903788"
---
# <a name="object-identifier"></a>OBJEKTBEZEICHNER

Der **OBJECT IDENTIFIER-Datentyp** wird in ein TLV-Triplet codiert, das mit dem **Tagwert** 0x06. Jede ganze Zahl eines gepunkteten Dezimalobjektbezeichners (OID) wird gemäß den folgenden Regeln codiert:

-   Die ersten beiden Knoten der OID werden in einem einzelnen Byte codiert. Der erste Knoten wird mit dem Dezimaltrennzeichen 40 multipliziert, und das Ergebnis wird dem Wert des zweiten Knotens hinzugefügt.
-   Knotenwerte kleiner oder gleich 127 werden in einem Byte codiert.
-   Knotenwerte, die größer oder gleich 128 sind, werden in mehreren Bytes codiert. Bit 7 des äußerst linken Byte ist auf 1 festgelegt. Die Bits 0 bis 6 jedes Byte enthalten den codierten Wert.

Diese Punkte werden in der folgenden Abbildung dargestellt.

![der Codierung des Objektbezeichnerdatentyps](images/der-tlv-oid.png)

Das folgende Beispiel zeigt, wie das **ClientId-Attribut** in einer Zertifikatanforderung codiert wird.

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

 

 




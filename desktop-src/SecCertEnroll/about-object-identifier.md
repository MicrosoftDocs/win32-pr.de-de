---
description: Der objektbezeichnerdatentyp wird in eine TLV-Dreiecks Codierung codiert, die mit einem Tagwert von 0x06 beginnt.
ms.assetid: 42c015c8-3de1-4482-bf27-b19c422b8cdb
title: Objekt Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cc81169968bfb3be5a49b0f30b8171cd904bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216004"
---
# <a name="object-identifier"></a>Objekt Bezeichner

Der **objektbezeichnerdatentyp** wird in eine TLV-Dreiecks Codierung codiert, die mit einem **Tagwert** von 0x06 beginnt. Jede Ganzzahl eines punktierten dezimalen Objekt Bezeichners (OID) wird gemäß den folgenden Regeln codiert:

-   Die ersten beiden Knoten der OID werden auf ein einzelnes Byte codiert. Der erste Knoten wird mit dem Dezimaltrennzeichen 40 multipliziert, und das Ergebnis wird dem Wert des zweiten Knotens hinzugefügt.
-   Knotenwerte, die kleiner oder gleich 127 sind, werden auf einem Byte codiert.
-   Knotenwerte, die größer oder gleich 128 sind, werden mit mehreren Bytes codiert. Bit 7 des ganz links stehenden Byte ist auf eins festgelegt. Bits 0 bis 6 der einzelnen Bytes enthalten den codierten Wert.

Diese Punkte werden in der folgenden Abbildung dargestellt.

![der-Codierung des objektbezeichnerdatentyps](images/der-tlv-oid.png)

Im folgenden Beispiel wird gezeigt, wie das **ClientID-** Attribut in einer Zertifikat Anforderung codiert wird.

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

 

 




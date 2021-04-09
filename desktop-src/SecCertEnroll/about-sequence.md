---
description: Eine Sequenz enthält ein geordnetes Feld mit einem oder mehreren Typen.
ms.assetid: b1a37cde-d5a2-4b01-a076-cb09741ae51d
title: SEQUENCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28602a122303f341507029375a2e4762581ec197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959725"
---
# <a name="sequence"></a><span data-ttu-id="73908-103">SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="73908-103">SEQUENCE</span></span>

<span data-ttu-id="73908-104">Eine **Sequenz** enthält ein geordnetes Feld mit einem oder mehreren Typen.</span><span class="sxs-lookup"><span data-stu-id="73908-104">A **SEQUENCE** contains an ordered field of one or more types.</span></span> <span data-ttu-id="73908-105">Sie wird in ein TLV-Dreieck codiert, das mit einem **tagbyte** von 0x30 beginnt.</span><span class="sxs-lookup"><span data-stu-id="73908-105">It is encoded into a TLV triplet that begins with a **Tag** byte of 0x30.</span></span> <span data-ttu-id="73908-106">Die folgende Certutil.exe Ausgabe aus dem [PKCS \# 10-codierten ASN. 1](pkcs--10-encoded-asn-1.md) -Thema enthält mehrere Beispiele für **Sequenz** Datenstrukturen.</span><span class="sxs-lookup"><span data-stu-id="73908-106">The following Certutil.exe output from the [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md) topic provides multiple examples of **SEQUENCE** data structures.</span></span> <span data-ttu-id="73908-107">Die Ausgabe zeigt einen öffentlichen Schlüssel von 128 Byte und einen Exponenten mit drei Byte.</span><span class="sxs-lookup"><span data-stu-id="73908-107">The output shows a 128 byte public key and three byte exponent.</span></span>

``` syntax
30 81 9f                             ; SEQUENCE (9f Bytes)
|  30 0d                             ; SEQUENCE (d Bytes)
|  |  |  06 09                       ; OBJECT_ID (9 Bytes)
|  |  |  2a 86 48 86 f7 0d 01 01 01  ; 1.2.840.113549.1.1.1 
|  |  05 00                          ; NULL (0 Bytes)
|  03 81 8d                          ; BIT_STRING (8d Bytes)
|     00
|     30 81 89                       ; SEQUENCE (89 Bytes)
|        02 81 81                    ; INTEGER (81 Bytes)
|        |  00
|        |  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|        |  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|        |  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|        |  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|        |  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|        |  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|        |  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|        |  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
|        02 03                       ; INTEGER (3 Bytes)
|           01 00 01
```

<span data-ttu-id="73908-108">Wenn die **Sequenz** weniger als 128 Bytes enthält, benötigt das **Längen** Feld des TLV-Dreiecks nur ein Byte, um die Inhalts Länge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="73908-108">If the **SEQUENCE** contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="73908-109">Wenn Sie mehr als 127 Bytes hat, wird Bit 7 des **Längen** Felds auf 1 festgelegt, und Bits 6 bis 0 geben Sie die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhalts Länge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73908-109">If it is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="73908-110">Das zweite Byte der ersten Zeile im vorangehenden Beispiel gibt z. b. an, dass es ein nachfolgendes **Längen** Byte gibt, das 0x9F Bytes an Inhalt angibt (die meisten **Sequenzen** werden nicht angezeigt).</span><span class="sxs-lookup"><span data-stu-id="73908-110">For example, the second byte of the first line in the preceding example indicates that there is one trailing **Length** byte that specifies 0x9F bytes of content (most of the **SEQUENCE** is not shown).</span></span> <span data-ttu-id="73908-111">Weitere Informationen finden Sie unter [codierte Länge und Wert Bytes](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="73908-111">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="73908-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="73908-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73908-113">ASN. 1-Typsystem</span><span class="sxs-lookup"><span data-stu-id="73908-113">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="73908-114">Der-Codierung von ASN. 1-Typen</span><span class="sxs-lookup"><span data-stu-id="73908-114">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




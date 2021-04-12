---
description: Ganzzahlige Werte werden in ein TLV-Dreieck codiert, das mit dem Tagwert 0x02 beginnt.
ms.assetid: a6fed62f-af59-488c-a690-be8c3413086f
title: Ganzzahl (Zertifikatregistrierungs-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0e8ed162d4cf4b2ac4909baf1cd7b5e94ddea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345438"
---
# <a name="integer-certificate-enrollment-api"></a><span data-ttu-id="1ff96-103">Ganzzahl (Zertifikatregistrierungs-API)</span><span class="sxs-lookup"><span data-stu-id="1ff96-103">INTEGER (Certificate Enrollment API)</span></span>

<span data-ttu-id="1ff96-104">Ganzzahlige Werte werden in ein TLV-Dreieck codiert, das mit dem **Tagwert** 0x02 beginnt.</span><span class="sxs-lookup"><span data-stu-id="1ff96-104">Integer values are encoded into a TLV triplet that begins with a **Tag** value of 0x02.</span></span> <span data-ttu-id="1ff96-105">Das **Wertfeld** des TLV-Zweigs enthält die codierte Ganzzahl, wenn Sie positiv ist, oder die zwei Komplement, wenn Sie negativ ist.</span><span class="sxs-lookup"><span data-stu-id="1ff96-105">The **Value** field of the TLV triplet contains the encoded integer if it is positive, or its two's complement if it is negative.</span></span> <span data-ttu-id="1ff96-106">Wenn die ganze Zahl positiv ist, aber das hohe Bestell Bit auf 1 festgelegt ist, wird dem Inhalt eine führende 0x00 hinzugefügt, um anzugeben, dass die Zahl nicht negativ ist.</span><span class="sxs-lookup"><span data-stu-id="1ff96-106">If the integer is positive but the high order bit is set to 1, a leading 0x00 is added to the content to indicate that the number is not negative.</span></span> <span data-ttu-id="1ff96-107">Beispielsweise ist das hochwertigen Byte von 0x8F (10001111) 1.</span><span class="sxs-lookup"><span data-stu-id="1ff96-107">For example, the high order byte of 0x8F (10001111) is 1.</span></span> <span data-ttu-id="1ff96-108">Daher wird dem Inhalt ein führendes NULL-Byte hinzugefügt, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1ff96-108">Therefore a leading zero byte is added to the content as shown in the following illustration.</span></span>

![der-Codierung des booleschen Datentyps.](images/der-tlv-integer.png)

<span data-ttu-id="1ff96-110">Wenn die ganze Zahl weniger als 128 Bytes enthält, benötigt das *Längen* Feld nur ein Byte, um die Inhalts Länge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1ff96-110">If the integer contains fewer than 128 bytes, the *Length* field requires only one byte to specify the content length.</span></span> <span data-ttu-id="1ff96-111">Wenn die Ganzzahl mehr als 127 Bytes beträgt, wird Bit 7 des *Längen* Felds auf 1 festgelegt, und Bits 6 bis 0 geben Sie die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhalts Länge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ff96-111">If the integer is more than 127 bytes, bit 7 of the *Length* field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="1ff96-112">Weitere Informationen finden Sie unter [codierte Länge und Wert Bytes](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="1ff96-112">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

<span data-ttu-id="1ff96-113">Im folgenden Beispiel wird aus [PKCS \# 10-codiertem ASN. 1](pkcs--10-encoded-asn-1.md)die Codierung für einen öffentlichen Schlüssel mit 128 Byte veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1ff96-113">The following example, from [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md), shows the encoding for a 128 byte public key.</span></span> <span data-ttu-id="1ff96-114">Das erste Byte enthält den **Tagwert** des **ganzzahligen** Datentyps 0x02.</span><span class="sxs-lookup"><span data-stu-id="1ff96-114">The first byte contains the **Tag** value for the **INTEGER** data type, 0x02.</span></span> <span data-ttu-id="1ff96-115">Das zweite und das dritte Byte enthalten den **Längen** Wert.</span><span class="sxs-lookup"><span data-stu-id="1ff96-115">The second and third bytes contain the **Length** value.</span></span> <span data-ttu-id="1ff96-116">Bit 7 des zweiten Bytes ist auf 1 festgelegt, da mehr als 127 Bytes Inhalt vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="1ff96-116">Bit 7 of the second byte is set to 1 because there are more than 127 bytes of content.</span></span> <span data-ttu-id="1ff96-117">Bits 0 bis 6 des zweiten Bytes geben Sie die Anzahl der nachfolgenden Bytes an, die in diesem Fall eine genaue Angabe der Inhalts Länge benötigen.</span><span class="sxs-lookup"><span data-stu-id="1ff96-117">Bits 0 through 6 of the second byte specify the number of trailing bytes needed, in this case one, to accurately specify the content length.</span></span> <span data-ttu-id="1ff96-118">Das dritte Byte gibt die Anzahl der Inhalts Bytes an, 0x81.</span><span class="sxs-lookup"><span data-stu-id="1ff96-118">The third byte specifies the number of content bytes, 0x81.</span></span> <span data-ttu-id="1ff96-119">Das vierte Byte, 0x00, wird dem-Inhalt hinzugefügt, um anzugeben, dass die ganze Zahl tatsächlich ein positiver Wert ist, auch wenn das Signier Bit des führenden Inhalts bytes (0x8F) auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1ff96-119">The fourth byte, 0x00, is added to the content to indicate that the integer is indeed a positive value even though the sign bit of the leading content byte (0x8F) is set to 1.</span></span>

``` syntax
02 81 81          ; INTEGER (81 Bytes)
|  00
|  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
```

<span data-ttu-id="1ff96-120">Im folgenden Beispiel wird gezeigt, wie der ganzzahlige Wert 0x03 codiert wird.</span><span class="sxs-lookup"><span data-stu-id="1ff96-120">The following example shows how the integer value 0x03 is encoded.</span></span> <span data-ttu-id="1ff96-121">Das **tagbyte** enthält 0x02, und das **length** -Byte gibt an, dass ein Byte Inhalt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1ff96-121">The **Tag** byte contains 0x02, and the **Length** byte specifies that there is one byte of content.</span></span>

``` syntax
02 01             ; INTEGER (1 Bytes)
|  03
```

## <a name="related-topics"></a><span data-ttu-id="1ff96-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ff96-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ff96-123">ASN. 1-Typsystem</span><span class="sxs-lookup"><span data-stu-id="1ff96-123">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="1ff96-124">Der-Codierung von ASN. 1-Typen</span><span class="sxs-lookup"><span data-stu-id="1ff96-124">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




---
description: Der Datentyp der ASN. 1-Oktett-Zeichenfolge wird in eine TLV-Kette codiert, die mit einem tagbyte von 0x04 beginnt.
ms.assetid: 9d07a6c8-a15f-4030-838c-3063e315684f
title: Oktett-Zeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed2a042312a4415ea9554b7519404097287244f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485419"
---
# <a name="octet-string"></a><span data-ttu-id="f3f3f-103">Oktett-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f3f3f-103">OCTET STRING</span></span>

<span data-ttu-id="f3f3f-104">Der Datentyp der ASN. 1- **Oktett-Zeichenfolge** wird in eine TLV-Kette codiert, die mit einem **tagbyte** von 0x04 beginnt.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-104">The ASN.1 **OCTET STRING** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x04.</span></span> <span data-ttu-id="f3f3f-105">Die Datentypen der **Oktett-Zeichenfolge** und der [Bitzeichenfolge](about-bit-string.md) sind sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-105">The **OCTET STRING** and [BIT STRING](about-bit-string.md) data types are very similar.</span></span> <span data-ttu-id="f3f3f-106">Folglich werden die beiden Typen auf ähnliche Weise codiert, es sei denn, das nachfolgende Byte einer **Oktett-Zeichenfolge** darf keine nicht verwendeten Bits aufweisen. dem Inhalt müssen keine führenden Bytes hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-106">Thus, the two types are encoded in a similar manner except that, because the trailing byte of an **OCTET STRING** cannot have unused bits, no leading bytes must be added to the content.</span></span> <span data-ttu-id="f3f3f-107">Das folgende Beispiel, das aus dem Thema " [CMC-codiertes ASN. 1](cmc-encoded-asn-1.md) " angepasst wurde, zeigt, wie der Name einer Zertifikat Vorlage als Bytearray codiert wird.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-107">The following example, adapted from the [CMC Encoded ASN.1](cmc-encoded-asn-1.md) topic, shows how the name of a certificate template is encoded as a byte array.</span></span>

``` syntax
30 17                                 ; SEQUENCE (17 Bytes)
|  06 09                              ; OBJECT_ID (9 Bytes)
|  |  2b 06 01 04 01 82 37 14  02     ;   1.3.6.1.4.1.311.20.2
|  04 0a                              ; OCTET_STRING (a Bytes)
|     1e 08 00 55 00 73 00 65  00 72  ;   ...U.s.e.r
```

<span data-ttu-id="f3f3f-108">Wenn das Bytearray weniger als 128 Bytes enthält, benötigt das **Längen** Feld des TLV-Dreiecks nur ein Byte, um die Inhalts Länge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-108">If the byte array contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="f3f3f-109">Wenn Sie mehr als 127 Bytes hat, wird Bit 7 des **Längen** Felds auf 1 festgelegt, und Bits 6 bis 0 geben Sie die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhalts Länge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-109">If it is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="f3f3f-110">Dies wird im folgenden Beispiel gezeigt, bei dem das High-Order-Bit des zweiten Bytes in der ersten Zeile auf 1 festgelegt ist und das Byte angibt, dass ein nach gestelltes **Längen** Byte vorliegt.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-110">This is shown in the following example where the high order bit of the second byte on the first line is set to 1 and the byte indicates that there is a trailing **Length** byte.</span></span> <span data-ttu-id="f3f3f-111">Das dritte Byte gibt daher an, dass der Inhalt 0x80 Bytes lang ist.</span><span class="sxs-lookup"><span data-stu-id="f3f3f-111">The third byte therefore specifies that the content is 0x80 bytes long.</span></span>

``` syntax
04 81 80                       ; OCTET_STRING (80 Bytes)
   38 10 60 e2 70 69 91 4a     ;   8.`.pi.J
   8b b5 22 57 2a 62 ef de     ;   .."W*b..
   15 7d 59 d6 4e 20 9a 45     ;   .}Y.N .E
   2b e3 fd fc 68 ba af bf     ;   +...h...
   9c 17 b0 8e 6d c4 29 1e     ;   ....m.).
   e3 21 ac bb 5a 8a c9 67     ;   .!..Z..g
   0a d4 45 93 10 c0 26 eb     ;   ..E...&.
   0a 83 c2 b1 40 87 36 f7     ;   ....@.6.
   a0 26 da b9 bb 46 73 88     ;   .&...Fs.
   7a 67 b9 e6 b3 6f ea 59     ;   zg...o.Y
   28 8a d3 92 72 f6 7b 89     ;   (...r.{.
   a0 d8 2d 9e 40 eb 1e bb     ;   ..-.@...
   6e ae f0 5a ed 16 c9 e3     ;   n..Z....
   27 59 37 8f f3 4a 98 60     ;   'Y7..J.`
   f8 fb a7 0a ee 1b 6e 91     ;   ......n.
   95 96 cf 0d 56 ac ab 35     ;   ....V..5
```

## <a name="related-topics"></a><span data-ttu-id="f3f3f-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f3f3f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3f3f-113">ASN. 1-Typsystem</span><span class="sxs-lookup"><span data-stu-id="f3f3f-113">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="f3f3f-114">Der-Codierung von ASN. 1-Typen</span><span class="sxs-lookup"><span data-stu-id="f3f3f-114">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




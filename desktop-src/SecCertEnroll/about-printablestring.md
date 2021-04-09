---
description: Der Datentyp ASN. 1 PrintableString wird in eine TLV-Kette codiert, die mit einem tagbyte von 0x13 beginnt.
ms.assetid: 998fef66-7a24-462f-96f2-92c739bbefa2
title: PrintableString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ebc95f1a58e8d7beb4a1d3bbb037788252349a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865024"
---
# <a name="printablestring"></a><span data-ttu-id="87b8d-103">PrintableString</span><span class="sxs-lookup"><span data-stu-id="87b8d-103">PrintableString</span></span>

<span data-ttu-id="87b8d-104">Der Datentyp ASN. 1 **PrintableString** wird in eine TLV-Kette codiert, die mit einem **tagbyte** von 0x13 beginnt.</span><span class="sxs-lookup"><span data-stu-id="87b8d-104">The ASN.1 **PrintableString** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x13.</span></span> <span data-ttu-id="87b8d-105">Im folgenden Beispiel wird aus dem Thema [PKCS \# 10-codierte ASN. 1](pkcs--10-encoded-asn-1.md) gezeigt, wie ein allgemeiner Benutzername von testcn als **PrintableString** -Typ codiert wird.</span><span class="sxs-lookup"><span data-stu-id="87b8d-105">The following example, from the [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md) topic, shows how a user common name of TestCN is encoded as a **PrintableString** type.</span></span> <span data-ttu-id="87b8d-106">Der Objekt Bezeichner für einen allgemeinen Namen ist 2.5.4.3.</span><span class="sxs-lookup"><span data-stu-id="87b8d-106">The object identifier for a common name is 2.5.4.3.</span></span>

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

<span data-ttu-id="87b8d-107">Wenn die Zeichenfolge weniger als 128 Bytes enthält, benötigt das **Längen** Feld des TLV-Dreiecks nur ein Byte, um die Inhalts Länge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="87b8d-107">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="87b8d-108">Wenn die Zeichenfolge mehr als 127 Bytes beträgt, wird Bit 7 des **Längen** Felds auf 1 festgelegt, und Bits 6 bis 0 geben Sie die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhalts Länge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87b8d-108">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="87b8d-109">Weitere Informationen finden Sie unter [codierte Länge und Wert Bytes](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="87b8d-109">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="87b8d-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="87b8d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87b8d-111">ASN. 1-Typsystem</span><span class="sxs-lookup"><span data-stu-id="87b8d-111">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="87b8d-112">Der-Codierung von ASN. 1-Typen</span><span class="sxs-lookup"><span data-stu-id="87b8d-112">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




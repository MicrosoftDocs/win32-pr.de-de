---
description: Der ASN. 1 UTF8String-Datentyp wird in ein TLV-Dreieck codiert, das mit dem Tag-Byte 0x0c beginnt.
ms.assetid: e30737d3-8294-48d8-9e42-f21918acc73c
title: UTF8String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26048a46689d27b68e8cacfa4af13b37cde4d613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865020"
---
# <a name="utf8string"></a><span data-ttu-id="a3ac8-103">UTF8String</span><span class="sxs-lookup"><span data-stu-id="a3ac8-103">UTF8String</span></span>

<span data-ttu-id="a3ac8-104">Der ASN. 1 **UTF8String** -Datentyp wird in ein TLV-Dreieck codiert, das mit dem **Tag** -Byte 0x0c beginnt.</span><span class="sxs-lookup"><span data-stu-id="a3ac8-104">The ASN.1 **UTF8String** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x0C.</span></span> <span data-ttu-id="a3ac8-105">Im folgenden Beispiel wird aus dem Thema " [CMC-codierte ASN. 1](cmc-encoded-asn-1.md) " gezeigt, wie das **ClientID-** Attribut als Integer-und drei **UTF8String** -Typen codiert wird.</span><span class="sxs-lookup"><span data-stu-id="a3ac8-105">The following example, from the [CMC Encoded ASN.1](cmc-encoded-asn-1.md) topic, shows how the **ClientId** attribute is encoded as an integer and three **UTF8String** types.</span></span> <span data-ttu-id="a3ac8-106">Der Objekt Bezeichner für das Attribut ist 1.3.6.1.4.1.311.21.20.</span><span class="sxs-lookup"><span data-stu-id="a3ac8-106">The object identifier for the attribute is 1.3.6.1.4.1.311.21.20.</span></span> <span data-ttu-id="a3ac8-107">Die Informationen, die mithilfe der [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) -Schnittstelle angegeben werden können, enthalten eine Client-ID, den Domain Name System (DNS)-Computernamen, den Sam-Benutzernamen (Security Accounts Manager) und den Namen der Anwendung, die die Zertifikat Anforderung erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="a3ac8-107">The information, which can be specified by using the [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) interface, includes a client ID number, the Domain Name System (DNS) computer name, the Security Accounts Manager (SAM) user name, and the name of the application that created the certificate request.</span></span>

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

<span data-ttu-id="a3ac8-108">Wenn die Zeichenfolge weniger als 128 Bytes enthält, benötigt das **Längen** Feld des TLV-Dreiecks nur ein Byte, um die Inhalts Länge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a3ac8-108">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="a3ac8-109">Wenn die Zeichenfolge mehr als 127 Bytes beträgt, wird Bit 7 des **Längen** Felds auf 1 festgelegt, und Bits 6 bis 0 geben Sie die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhalts Länge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3ac8-109">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="a3ac8-110">Weitere Informationen finden Sie unter [codierte Länge und Wert Bytes](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="a3ac8-110">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3ac8-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a3ac8-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3ac8-112">ASN. 1-Typsystem</span><span class="sxs-lookup"><span data-stu-id="a3ac8-112">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="a3ac8-113">Der-Codierung von ASN. 1-Typen</span><span class="sxs-lookup"><span data-stu-id="a3ac8-113">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




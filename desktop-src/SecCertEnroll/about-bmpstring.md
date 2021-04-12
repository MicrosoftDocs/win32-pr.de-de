---
description: Der Datentyp ASN. 1 bmpstring, der als Unicode- \_ Zeichenfolge in der Zertifikatregistrierungs-API bezeichnet wird, wird in ein TLV-Dreieck codiert, das mit einem tagbyte von 0x1E beginnt.
ms.assetid: 66e4a6d8-2401-4346-9361-e145735cbe19
title: Bmpstring
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c911218d852b792a333f015c825a7e4d1486b62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216007"
---
# <a name="bmpstring"></a><span data-ttu-id="14b48-103">Bmpstring</span><span class="sxs-lookup"><span data-stu-id="14b48-103">BMPString</span></span>

<span data-ttu-id="14b48-104">Der Datentyp ASN. 1 **bmpstring** , der als **Unicode- \_ Zeichenfolge** in der Zertifikatregistrierungs-API bezeichnet wird, wird in ein TLV-Dreieck codiert, das mit einem **tagbyte** von 0x1E beginnt.</span><span class="sxs-lookup"><span data-stu-id="14b48-104">The ASN.1 **BMPString** data type, called a **UNICODE\_STRING** in the Certificate Enrollment API, is encoded into a TLV triplet that begins with a **Tag** byte of 0x1E.</span></span> <span data-ttu-id="14b48-105">Im folgenden Beispiel, das aus dem Thema " [CMC-codierte ASN. 1](cmc-encoded-asn-1.md) " angepasst wurde, wird die Codierung für eine **templatename** -Erweiterung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="14b48-105">The following example, adapted from the [CMC Encoded ASN.1](cmc-encoded-asn-1.md) topic, shows the encoding for a **TemplateName** extension.</span></span> <span data-ttu-id="14b48-106">Der Name kann mithilfe der [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) -Schnittstelle angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="14b48-106">The name can be specified by using the [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) interface.</span></span> <span data-ttu-id="14b48-107">Der Objekt Bezeichner für die Erweiterung ist 1.3.6.1.4.1.311.13.2.1.</span><span class="sxs-lookup"><span data-stu-id="14b48-107">The object identifier for the extension is 1.3.6.1.4.1.311.13.2.1.</span></span>

``` syntax
06 0a                              ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 01  ;   1.3.6.1.4.1.311.13.2.1 
31 34                              ; SET (34 Bytes)
   30 32                           ; SEQUENCE (32 Bytes)
      1e 26                        ; UNICODE_STRING (26 Bytes)
      |  00 43 00 65 00 72 00 74   ;   .C.e.r.t
      |  00 69 00 66 00 69 00 63   ;   .i.f.i.c
      |  00 61 00 74 00 65 00 54   ;   .a.t.e.T
      |  00 65 00 6d 00 70 00 6c   ;   .e.m.p.l
      |  00 61 00 74 00 65         ;   .a.t.e
      1e 08                        ; UNICODE_STRING (8 Bytes)
         00 55 00 73 00 65 00 72   ;   .U.s.e.r
```

<span data-ttu-id="14b48-108">Wenn die Zeichenfolge weniger als 128 Bytes enthält, benötigt das **Längen** Feld des TLV-Dreiecks nur ein Byte, um die Inhalts Länge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="14b48-108">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="14b48-109">Wenn die Zeichenfolge mehr als 127 Bytes beträgt, wird Bit 7 des **Längen** Felds auf 1 festgelegt, und Bits 6 bis 0 geben Sie die Anzahl zusätzlicher Bytes an, die zum Identifizieren der Inhalts Länge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14b48-109">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="14b48-110">Weitere Informationen finden Sie unter [codierte Länge und Wert Bytes](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="14b48-110">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="14b48-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="14b48-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14b48-112">ASN. 1-Typsystem</span><span class="sxs-lookup"><span data-stu-id="14b48-112">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="14b48-113">Der-Codierung von ASN. 1-Typen</span><span class="sxs-lookup"><span data-stu-id="14b48-113">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




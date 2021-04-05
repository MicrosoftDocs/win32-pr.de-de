---
description: Wenn Sie ein IX500DistinguishedName-Objekt mit einem Distinguished Name initialisieren, um den Betreff einer Zertifikat Anforderung zu identifizieren, wird eine ASN. 1-Sequenz (Distinguished Encoding Rules (der) codierte abstrakte Syntax Notation One (ASN. 1) erstellt.
ms.assetid: 58b05b59-2235-49bd-9543-45e786d62eaf
title: Codieren eines Antragsteller namens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fa03d95497a600c3e61fdda53820fd7a9858c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041827"
---
# <a name="encoding-a-subject-name"></a><span data-ttu-id="69c8e-103">Codieren eines Antragsteller namens</span><span class="sxs-lookup"><span data-stu-id="69c8e-103">Encoding a Subject Name</span></span>

<span data-ttu-id="69c8e-104">Wenn Sie ein [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) -Objekt mit einem Distinguished Name initialisieren, um den Betreff einer Zertifikat Anforderung zu identifizieren, wird eine ASN. 1-Sequenz ( [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) codierte [*abstrakte Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN. 1) erstellt.</span><span class="sxs-lookup"><span data-stu-id="69c8e-104">When you initialize an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object with a distinguished name to identify the subject of a certificate request, a [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) encoded [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) sequence is created.</span></span> <span data-ttu-id="69c8e-105">Nehmen Sie beispielsweise an, dass der Distinguished Name des Antragstellers die folgenden relativen Distinguished Names (rDNS) umfasst:</span><span class="sxs-lookup"><span data-stu-id="69c8e-105">For example, assume that the subject distinguished name consists of the following relative distinguished names (RDNs):</span></span><dl> <span data-ttu-id="69c8e-106">E =Administrator@jdomcsc.nttest.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="69c8e-106">E=Administrator@jdomcsc.nttest.microsoft.com</span></span>  
<span data-ttu-id="69c8e-107">CN = Administrator</span><span class="sxs-lookup"><span data-stu-id="69c8e-107">CN=Administrator</span></span>  
<span data-ttu-id="69c8e-108">CN = Benutzer</span><span class="sxs-lookup"><span data-stu-id="69c8e-108">CN=Users</span></span>  
<span data-ttu-id="69c8e-109">DC = jdomcsc</span><span class="sxs-lookup"><span data-stu-id="69c8e-109">DC=jdomcsc</span></span>  
<span data-ttu-id="69c8e-110">DC = nttest</span><span class="sxs-lookup"><span data-stu-id="69c8e-110">DC=nttest</span></span>  
<span data-ttu-id="69c8e-111">DC = Microsoft</span><span class="sxs-lookup"><span data-stu-id="69c8e-111">DC=microsoft</span></span>  
<span data-ttu-id="69c8e-112">DC = com</span><span class="sxs-lookup"><span data-stu-id="69c8e-112">DC=com</span></span>  
<span data-ttu-id="69c8e-113"></dl>The **IX500DistinguishedName** object creates the following DER-encoded (ASN.1) sequence. Notice that the sequence is encoded in reverse order. This example is derived from the<a href="pkcs--7-renewal-encoded-asn-1.md">PKCS #7 Erneuerungs codiertes ASN. 1</a> Thema.</span><span class="sxs-lookup"><span data-stu-id="69c8e-113"></dl>The **IX500DistinguishedName** object creates the following DER-encoded (ASN.1) sequence. Notice that the sequence is encoded in reverse order. This example is derived from the<a href="pkcs--7-renewal-encoded-asn-1.md">PKCS #7 Renewal Encoded ASN.1</a> topic.</span></span>

``` syntax
0a0d: 30 81 c4          ; SEQUENCE (c4 Bytes)
0a10: |  31 13          ; SET (13 Bytes)
0a12: |  |  30 11               ; SEQUENCE (11 Bytes)
0a14: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a16: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a20: |  |     16 03        ; IA5_STRING (3 Bytes)
0a22: |  |        63 6f 6d                                          ; com
      |  |           ; "com"
0a25: |  31 19          ; SET (19 Bytes)
0a27: |  |  30 17               ; SEQUENCE (17 Bytes)
0a29: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a2b: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a35: |  |     16 09            ; IA5_STRING (9 Bytes)
0a37: |  |        6d 69 63 72 6f 73 6f 66  74                       ; microsoft
      |  |           ; "microsoft"
0a40: |  31 16          ; SET (16 Bytes)
0a42: |  |  30 14               ; SEQUENCE (14 Bytes)
0a44: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a46: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a50: |  |     16 06            ; IA5_STRING (6 Bytes)
0a52: |  |        6e 74 74 65 73 74                                 ; nttest
      |  |           ; "nttest"
0a58: |  31 17          ; SET (17 Bytes)
0a5a: |  |  30 15               ; SEQUENCE (15 Bytes)
0a5c: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a5e: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a68: |  |     16 07            ; IA5_STRING (7 Bytes)
0a6a: |  |        6a 64 6f 6d 63 73 63                              ; jdomcsc
      |  |           ; "jdomcsc"
0a71: |  31 0e          ; SET (e Bytes)
0a73: |  |  30 0c               ; SEQUENCE (c Bytes)
0a75: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a77: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a7a: |  |     13 05            ; PRINTABLE_STRING (5 Bytes)
0a7c: |  |        55 73 65 72 73                                    ; Users
      |  |           ; "Users"
0a81: |  31 16          ; SET (16 Bytes)
0a83: |  |  30 14               ; SEQUENCE (14 Bytes)
0a85: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a87: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a8a: |  |     13 0d            ; PRINTABLE_STRING (d Bytes)
0a8c: |  |        41 64 6d 69 6e 69 73 74  72 61 74 6f 72           ; Administrator
      |  |           ; "Administrator"
0a99: |  31 39          ; SET (39 Bytes)
0a9b: |     30 37               ; SEQUENCE (37 Bytes)
0a9d: |        06 09            ; OBJECT_ID (9 Bytes)
0a9f: |        |  2a 86 48 86 f7 0d 01 09  01
      |        |     ; 1.2.840.113549.1.9.1 Email Address (E)
0aa8: |        16 2a            ; IA5_STRING (2a Bytes)
0aaa: |           41 64 6d 69 6e 69 73 74  72 61 74 6f 72 40 6a 64  ; Administrator@jd
0aba: |           6f 6d 63 73 63 2e 6e 74  74 65 73 74 2e 6d 69 63  ; omcsc.nttest.mic
0aca: |           72 6f 73 6f 66 74 2e 63  6f 6d                    ; rosoft.com
      |              ; "Administrator@jdomcsc.nttest.microsoft.com"
```

<span data-ttu-id="69c8e-114">Wie unter " [Betreffnamen](subject-names.md)" erläutert, besteht jede RDN in einem Distinguished Name aus einer Reihe von Attributen, und jedes Attribut enthält einen [*Objekt Bezeichner*](/windows/desktop/SecGloss/o-gly) (OID) und einen Wert.</span><span class="sxs-lookup"><span data-stu-id="69c8e-114">As discussed in [Subject Names](subject-names.md), every RDN in a distinguished name consists of a set of attributes, and each attribute contains an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) and a value.</span></span> <span data-ttu-id="69c8e-115">Um zu verstehen, wie das [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) -Objekt einen Distinguished Name codiert, sollten Sie den allgemeinen Namen CN = Users in Erwägung gezogen haben.</span><span class="sxs-lookup"><span data-stu-id="69c8e-115">To understand how the [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object encodes a distinguished name, consider the common name CN=Users.</span></span>

``` syntax
0a73: |  |  30 0c               ; SEQUENCE (c Bytes)
0a75: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a77: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a7a: |  |     13 05            ; PRINTABLE_STRING (5 Bytes)
0a7c: |  |        55 73 65 72 73                                    ; Users
      |  |           ; "Users"
```

<span data-ttu-id="69c8e-116">Die Syntax der Übertragungs Syntax eines ASN. 1-Objekts enthält immer einen Typ, eine Länge und einen Wert, und jedes Feld im Dreieck enthält mindestens ein Byte.</span><span class="sxs-lookup"><span data-stu-id="69c8e-116">The DER transfer syntax of an ASN.1 object always contains a type, length, and value triplet, and each field in the triplet contains one or more bytes.</span></span> <span data-ttu-id="69c8e-117">Bei der Codierung besteht CN = Users aus einer OID und einem Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="69c8e-117">When encoded, CN=Users consists of an OID and a string value.</span></span> <span data-ttu-id="69c8e-118">Die gepunktete Dezimal Schreibweise der CN-OID ist 2.5.4.3, und der Zeichen folgen Wert ist "Users".</span><span class="sxs-lookup"><span data-stu-id="69c8e-118">The dotted decimal notation of the CN OID is 2.5.4.3 and the string value is "Users".</span></span> <span data-ttu-id="69c8e-119">Der Zeichen folgen Wert wird als **PRINTABLE_STRING** Datentyp dargestellt.</span><span class="sxs-lookup"><span data-stu-id="69c8e-119">The string value is represented as a **PRINTABLE_STRING** data type.</span></span> <span data-ttu-id="69c8e-120">Der numerische Typwert, der **object_id** zugeordnet ist, ist immer 0x06, und der **PRINTABLE_STRING** numerischer Typ ist immer 0x13.</span><span class="sxs-lookup"><span data-stu-id="69c8e-120">The numeric type value associated with **OBJECT_ID** is always 0x06, and the numeric type associated with **PRINTABLE_STRING** is always 0x13.</span></span> <span data-ttu-id="69c8e-121">Die Länge des allgemeinen namens "Users" beträgt 0x05 bytes.</span><span class="sxs-lookup"><span data-stu-id="69c8e-121">The length of the common name "Users" is 0x05 bytes.</span></span> <span data-ttu-id="69c8e-122">Die Länge der OID beträgt 0x03 bytes, und der Wert ist 0x55 0x04 0x03.</span><span class="sxs-lookup"><span data-stu-id="69c8e-122">The length of the OID is 0x03 bytes, and it's value is 0x55 0x04 0x03.</span></span>

> [!Note]  
> <span data-ttu-id="69c8e-123">Um die ersten zwei Ziffern des OID-2.5.4.3 in den Hexadezimalwert 0x55 zu übersetzen, Multiplizieren Sie die erste Ziffer der OID um 40 (2 x 40), und fügen Sie die zweite Ziffer (5) vor dem Konvertieren in Hexadezimal ein.</span><span class="sxs-lookup"><span data-stu-id="69c8e-123">To translate the first two digits of the OID 2.5.4.3 into the hexadecimal value 0x55, multiply the first digit of the OID by 40 (2 x 40) and add the second digit (5) before converting to hexadecimal.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="69c8e-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69c8e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69c8e-125">PKCS \# 7-Erneuerung codierter ASN. 1</span><span class="sxs-lookup"><span data-stu-id="69c8e-125">PKCS \#7 Renewal Encoded ASN.1</span></span>](pkcs--7-renewal-encoded-asn-1.md)
</dt> <dt>

[<span data-ttu-id="69c8e-126">Beispiel Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69c8e-126">Sample Requests</span></span>](sample-requests.md)
</dt> <dt>

[<span data-ttu-id="69c8e-127">Antragstellernamen</span><span class="sxs-lookup"><span data-stu-id="69c8e-127">Subject Names</span></span>](subject-names.md)
</dt> </dl>

 

 

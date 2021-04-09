---
description: Die Zertifikatregistrierungs-API verwendet die abstrakte Syntax Notation One (ASN. 1) zum definieren, codieren und Decodieren der Zertifikat Anforderungen und Zertifikate, die zwischen Client Computern und Zertifizierungsstellen übertragen werden.
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: Einführung in die ASN. 1-Syntax und-Codierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4fe15d2fb8fba4af25b9da7c249fec3a92630e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865031"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a><span data-ttu-id="9f84e-103">Einführung in die ASN. 1-Syntax und-Codierung</span><span class="sxs-lookup"><span data-stu-id="9f84e-103">Introduction to ASN.1 Syntax and Encoding</span></span>

<span data-ttu-id="9f84e-104">Die Zertifikatregistrierungs-API verwendet die abstrakte Syntax Notation One (ASN. 1) zum definieren, codieren und Decodieren der Zertifikat Anforderungen und Zertifikate, die zwischen Client Computern und Zertifizierungsstellen übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="9f84e-104">The Certificate Enrollment API uses Abstract Syntax Notation One (ASN.1) to define, encode, and decode the certificate requests and certificates that it transfers between client computers and certification authorities.</span></span> <span data-ttu-id="9f84e-105">ASN. 1 kann konzeptionell in einen Satz von Syntax Regeln und einen Satz von Codierungsregeln aufgeteilt werden, wie in den folgenden Beispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9f84e-105">ASN.1 can be conceptually divided into a set of syntax rules and a set of encoding rules as shown by the following examples.</span></span>

## <a name="asn1-syntax-example"></a><span data-ttu-id="9f84e-106">Beispiel für eine ASN. 1-Syntax</span><span class="sxs-lookup"><span data-stu-id="9f84e-106">ASN.1 Syntax Example</span></span>

<span data-ttu-id="9f84e-107">Eine Zertifikat Anforderung enthält unter anderem den Namen der Entität, von der die Anforderung stammt, oder für die die Anforderung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f84e-107">A certificate request contains, among other things, the name of the entity that is making the request or for which the request is being made.</span></span> <span data-ttu-id="9f84e-108">Der Name ist eine Sequenz von X. 500 Relative Distinguished Names (rDNS).</span><span class="sxs-lookup"><span data-stu-id="9f84e-108">The name is a sequence of X.500 relative distinguished names (RDNs).</span></span> <span data-ttu-id="9f84e-109">Jeder RDN in der Sequenz besteht aus einem Objekt Bezeichner (OID) und einem Wert.</span><span class="sxs-lookup"><span data-stu-id="9f84e-109">Each RDN in the sequence consists of an object identifier (OID) and a value.</span></span> <span data-ttu-id="9f84e-110">Die ASN. 1-Syntax für einen Betreffnamen ist im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9f84e-110">The ASN.1 syntax for a subject name is shown in the following example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Subject name
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}
```

## <a name="asn1-encoding-example"></a><span data-ttu-id="9f84e-111">ASN. 1-Codierungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="9f84e-111">ASN.1 Encoding Example</span></span>

<span data-ttu-id="9f84e-112">Die Zertifikatregistrierungs-API verwendet [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) zum Codieren des vorangehenden Antragsteller namens.</span><span class="sxs-lookup"><span data-stu-id="9f84e-112">The Certificate Enrollment API uses [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) to encode the preceding subject name.</span></span> <span data-ttu-id="9f84e-113">Der erfordert, dass jedes Element im Namen durch ein TLV-Element dargestellt wird, wobei T die Tagnummer des ASN. 1-Typs enthält, L die Länge und V den zugeordneten Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="9f84e-113">DER requires that each item in the name be represented by a TLV triplet where T contains the tag number of the ASN.1 type, L contains the length, and V contains the associated value.</span></span> <span data-ttu-id="9f84e-114">Im folgenden Beispiel wird gezeigt, wie der Antragsteller Name "testcn. testorg" codiert ist.</span><span class="sxs-lookup"><span data-stu-id="9f84e-114">The following example shows how the subject name TestCN.TestOrg is encoded.</span></span>

``` syntax
1.     30 23            ; SEQUENCE (23 Bytes)
2.     |  |  31 0f            ; SET (f Bytes)
3.     |  |  |  30 0d            ; SEQUENCE (d Bytes)
4.     |  |  |     06 03         ; OBJECT_ID (3 Bytes)
5.     |  |  |     |  55 04 03
6.     |  |  |     |     ; 2.5.4.3 Common Name (CN)
7.     |  |  |     13 06         ; PRINTABLE_STRING (6 Bytes)
8.     |  |  |        54 65 73 74 43 4e                    ; TestCN
9.     |  |  |           ; "TestCN"
10.    |  |  31 10            ; SET (10 Bytes)
11.    |  |     30 0e            ; SEQUENCE (e Bytes)
12.    |  |        06 03         ; OBJECT_ID (3 Bytes)
13.    |  |        |  55 04 0a
14.    |  |        |     ; 2.5.4.10 Organization (O)
15.    |  |        13 07         ; PRINTABLE_STRING (7 Bytes)
16.    |  |           54 65 73 74 4f 72 67                 ; TestOrg
17.    |  |              ; "TestOrg"
```

<span data-ttu-id="9f84e-115">Beachten Sie folgende Punkte:</span><span class="sxs-lookup"><span data-stu-id="9f84e-115">Note the following points:</span></span>

-   <span data-ttu-id="9f84e-116">Zeile 1:</span><span class="sxs-lookup"><span data-stu-id="9f84e-116">Line 1:</span></span><dl> <span data-ttu-id="9f84e-117">Der Name ist eine Sequenz von relativen Distinguished Names.</span><span class="sxs-lookup"><span data-stu-id="9f84e-117">The name is a sequence of relative distinguished names.</span></span>  
    <span data-ttu-id="9f84e-118">Die Tagnummer für den **Sequenztyp** ist 0x30.</span><span class="sxs-lookup"><span data-stu-id="9f84e-118">The tag number for the **SEQUENCE** type is 0x30.</span></span>  
    <span data-ttu-id="9f84e-119">Der Antragsteller Name von testcn. testorg erfordert 35 (0x23) Bytes.</span><span class="sxs-lookup"><span data-stu-id="9f84e-119">The subject name of TestCN.TestOrg requires 35 (0x23) bytes.</span></span>  
    </dl>
-   Line 2:<dl> <span data-ttu-id="9f84e-120">Der allgemeine Name, testcn, ist ein einzelner Satz von **attributetypevalue** -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="9f84e-120">The Common Name, TestCN, is a single set of **AttributeTypeValue** structures.</span></span>  
    <span data-ttu-id="9f84e-121">Die Tagnummer für eine **Menge** ist 0x31.</span><span class="sxs-lookup"><span data-stu-id="9f84e-121">The tag number for a **SET** is 0x31.</span></span>  
    </dl><span data-ttu-id="9f84e-122">
-   Zeile 3:</span><span class="sxs-lookup"><span data-stu-id="9f84e-122">
-   Line 3:</span></span><dl> <span data-ttu-id="9f84e-123">Die **attributetypevalue** -Struktur ist eine Sequenz.</span><span class="sxs-lookup"><span data-stu-id="9f84e-123">The **AttributeTypeValue** structure is a sequence.</span></span>  
    <span data-ttu-id="9f84e-124">Die Tagnummer für den **Sequenztyp** ist 0x30.</span><span class="sxs-lookup"><span data-stu-id="9f84e-124">The tag number for the **SEQUENCE** type is 0x30.</span></span>  
    <span data-ttu-id="9f84e-125">Die-Struktur erfordert 13 (0xD) Bytes.</span><span class="sxs-lookup"><span data-stu-id="9f84e-125">The structure requires 13 (0xD) bytes.</span></span>  
    </dl><span data-ttu-id="9f84e-126">
-   Zeilen 4 bis 6:</span><span class="sxs-lookup"><span data-stu-id="9f84e-126">
-   Lines 4 to 6:</span></span><dl> <span data-ttu-id="9f84e-127">Der Objekt Bezeichner (OID) für den allgemeinen Namen ist 2.5.4.3.</span><span class="sxs-lookup"><span data-stu-id="9f84e-127">The object identifier (OID) for the Common Name is 2.5.4.3.</span></span>  
    <span data-ttu-id="9f84e-128">Die OID ist ein Objekt- **\_ ID** -Typ mit drei Bytes.</span><span class="sxs-lookup"><span data-stu-id="9f84e-128">The OID is a three byte **OBJECT\_ID** type.</span></span>  
    <span data-ttu-id="9f84e-129">Die Tagnummer für den **Objekt- \_ ID** -Typ ist 0x06.</span><span class="sxs-lookup"><span data-stu-id="9f84e-129">The tag number for the **OBJECT\_ID** type is 0x06.</span></span>  
    </dl><span data-ttu-id="9f84e-130">
-   Zeilen 7 bis 9:</span><span class="sxs-lookup"><span data-stu-id="9f84e-130">
-   Lines 7 to 9:</span></span><dl> <span data-ttu-id="9f84e-131">Der allgemeine Name, testcn, ist ein Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="9f84e-131">The Common Name, TestCN, is a string value.</span></span>  
    <span data-ttu-id="9f84e-132">Die Zeichenfolge ist ein **druckbarer \_ Zeichen** Folgentyp mit sechs Byte.</span><span class="sxs-lookup"><span data-stu-id="9f84e-132">The string is a six byte **PRINTABLE\_STRING** type.</span></span>  
    <span data-ttu-id="9f84e-133">Die Tagnummer für den Typ der **druckbaren \_ Zeichenfolge** ist 0x13.</span><span class="sxs-lookup"><span data-stu-id="9f84e-133">The tag number for the **PRINTABLE\_STRING** type is 0x13.</span></span>  
    </dl>

## <a name="related-topics"></a><span data-ttu-id="9f84e-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9f84e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f84e-135">ASN. 1-Typsystem</span><span class="sxs-lookup"><span data-stu-id="9f84e-135">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="9f84e-136">Zertifikat Anforderungs Codierung</span><span class="sxs-lookup"><span data-stu-id="9f84e-136">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="9f84e-137">Der-Codierung von ASN. 1-Typen</span><span class="sxs-lookup"><span data-stu-id="9f84e-137">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="9f84e-138">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="9f84e-138">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 

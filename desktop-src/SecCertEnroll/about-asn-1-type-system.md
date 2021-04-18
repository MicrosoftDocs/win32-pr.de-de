---
description: Das Konzept eines-Datentyps ist für die abstrakte Syntax Notation One (ASN. 1) Standard wichtig.
ms.assetid: 85e88e0b-057b-42c7-a3c8-017a30195d1e
title: ASN. 1-Typsystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abbf60bf61e32c5fca882f2e40c946c043ef93e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366240"
---
# <a name="asn1-type-system"></a><span data-ttu-id="340df-103">ASN. 1-Typsystem</span><span class="sxs-lookup"><span data-stu-id="340df-103">ASN.1 Type System</span></span>

<span data-ttu-id="340df-104">Das Konzept eines-Datentyps ist für die abstrakte Syntax Notation One (ASN. 1) Standard wichtig.</span><span class="sxs-lookup"><span data-stu-id="340df-104">The concept of a data type is fundamental to the Abstract Syntax Notation One (ASN.1) standard.</span></span> <span data-ttu-id="340df-105">Jedes Feld einer Zertifikat Anforderungs Struktur ist einem Typ zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="340df-105">Every field of a certificate request structure is associated with a type.</span></span> <span data-ttu-id="340df-106">Beachten Sie beispielsweise die \# im folgenden Beispiel gezeigte Zertifikat Syntax PKCS 10 ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="340df-106">Consider, for example, the PKCS \#10 ASN.1 certificate syntax shown in the following example.</span></span>

``` syntax
--------------------------------------------------------------------
-- PKCS #10 Certificate request.
--------------------------------------------------------------------
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

--------------------------------------------------------------------
-- Version number.
--------------------------------------------------------------------
CertificationRequestInfoVersion ::= INTEGER

--------------------------------------------------------------------
-- Subject distinguished name (DN).
--------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}

--------------------------------------------------------------------
-- Public key information.
--------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
   algorithm           AlgorithmIdentifier,
   subjectPublicKey    BITSTRING
}

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
} 

--------------------------------------------------------------------
-- Attributes.
--------------------------------------------------------------------
Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   values             AttributeSetValue
}

AttributeSetValue ::= SET OF ANY
```

<span data-ttu-id="340df-107">Die Anforderungs Struktur auf hoher Ebene, **certificationrequestinfo**, ist ein Typ, der aus einer Sequenz anderer Typen besteht.</span><span class="sxs-lookup"><span data-stu-id="340df-107">The high-level request structure, **CertificationRequestInfo**, is a type that is made up from a sequence of other types.</span></span> <span data-ttu-id="340df-108">Wenn ein Typ ist oder nur grundlegende Typen, Zeichen folgen Typen oder **beliebige** enthält, kann er nicht weiter aufgeschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="340df-108">When a type is or contains only basic types, string types, or **ANY**, it cannot be broken down further.</span></span> <span data-ttu-id="340df-109">Das Feld **Version** ist beispielsweise ein **certificationrequestinfoversion** -Typ, der wiederum ein **ganzzahliger** Typ ist, d. h. ein grundlegender ASN. 1-Typ, der nicht aus anderen Typen besteht.</span><span class="sxs-lookup"><span data-stu-id="340df-109">For example, the **version** field is a **CertificationRequestInfoVersion** type which is, in turn, an **INTEGER** type, a basic ASN.1 type that is not composed from other types.</span></span>

<span data-ttu-id="340df-110">Ein Typsystem ermöglicht der visuellen Darstellung der Syntax einer Anforderung auf eine Weise, die von Entwicklern bereitgestellt werden kann, und ermöglicht die konsistente Codierung der Anforderung für die Übertragung über ein Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="340df-110">A type system enables the syntax of a request to be presented visually in a manner readily understood by developers, and it enables the request to be consistently encoded for transmission across a network.</span></span> <span data-ttu-id="340df-111">Weitere Informationen zur Codierung finden Sie unter [Distinguished Encoding Rules](distinguished-encoding-rules.md).</span><span class="sxs-lookup"><span data-stu-id="340df-111">For more information about encoding, see [Distinguished Encoding Rules](distinguished-encoding-rules.md).</span></span> <span data-ttu-id="340df-112">Weitere Informationen zu ASN. 1-Typen finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="340df-112">For more information about ASN.1 types, see the following topics.</span></span>

[<span data-ttu-id="340df-113">Standardtypen</span><span class="sxs-lookup"><span data-stu-id="340df-113">Basic Types</span></span>](about-basic-types.md)

<span data-ttu-id="340df-114">Erläutert die folgenden Datentypen:</span><span class="sxs-lookup"><span data-stu-id="340df-114">Discusses the following data types:</span></span>

* <span data-ttu-id="340df-115">**Bitzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="340df-115">**BIT STRING**</span></span>
* <span data-ttu-id="340df-116">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="340df-116">**BOOLEAN**</span></span>
* <span data-ttu-id="340df-117">**INTEGER**</span><span class="sxs-lookup"><span data-stu-id="340df-117">**INTEGER**</span></span>
* <span data-ttu-id="340df-118">**NULL**</span><span class="sxs-lookup"><span data-stu-id="340df-118">**NULL**</span></span>
* <span data-ttu-id="340df-119">**Objekt Bezeichner**</span><span class="sxs-lookup"><span data-stu-id="340df-119">**OBJECT IDENTIFIER**</span></span>
* <span data-ttu-id="340df-120">**Oktett-Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="340df-120">**OCTET STRING**</span></span>

[<span data-ttu-id="340df-121">Zeichen folgen Typen</span><span class="sxs-lookup"><span data-stu-id="340df-121">String Types</span></span>](about-string-types.md)

<span data-ttu-id="340df-122">Erläutert die folgenden Zeichen folgen Typen:</span><span class="sxs-lookup"><span data-stu-id="340df-122">Discusses the following string types:</span></span>

* <span data-ttu-id="340df-123">**Bmpstring**</span><span class="sxs-lookup"><span data-stu-id="340df-123">**BMPString**</span></span>
* <span data-ttu-id="340df-124">**IA5String**</span><span class="sxs-lookup"><span data-stu-id="340df-124">**IA5String**</span></span>
* <span data-ttu-id="340df-125">**PrintableString**</span><span class="sxs-lookup"><span data-stu-id="340df-125">**PrintableString**</span></span>
* <span data-ttu-id="340df-126">**Teletexstring**</span><span class="sxs-lookup"><span data-stu-id="340df-126">**TeletexString**</span></span>
* <span data-ttu-id="340df-127">**UTF8String**</span><span class="sxs-lookup"><span data-stu-id="340df-127">**UTF8String**</span></span>

[<span data-ttu-id="340df-128">Konstruierte Typen</span><span class="sxs-lookup"><span data-stu-id="340df-128">Constructed Types</span></span>](about-constructed-types.md)

<span data-ttu-id="340df-129">Erläutert ASN. 1-Datentypen, die grundlegende Typen, Zeichen folgen Typen oder andere konstruierte Typen enthalten können.</span><span class="sxs-lookup"><span data-stu-id="340df-129">Discusses ASN.1 data types that can contain basic types, string types, or other constructed types.</span></span>




 

## <a name="related-topics"></a><span data-ttu-id="340df-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="340df-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="340df-131">Zertifikat Anforderungs Codierung</span><span class="sxs-lookup"><span data-stu-id="340df-131">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="340df-132">Der-Codierung von ASN. 1-Typen</span><span class="sxs-lookup"><span data-stu-id="340df-132">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="340df-133">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="340df-133">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="340df-134">Einführung in die ASN. 1-Syntax und-Codierung</span><span class="sxs-lookup"><span data-stu-id="340df-134">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 




---
description: Die Zertifikatregistrierungs-API unterstützt die folgenden grundlegenden ASN. 1-Typen.
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: Grundlegende Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f3ae64c058fce3466ca06e7bf205c4c4165fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359031"
---
# <a name="basic-types"></a><span data-ttu-id="bb89b-103">Grundlegende Typen</span><span class="sxs-lookup"><span data-stu-id="bb89b-103">Basic Types</span></span>

<span data-ttu-id="bb89b-104">Die Zertifikatregistrierungs-API unterstützt die folgenden grundlegenden ASN. 1-Typen.</span><span class="sxs-lookup"><span data-stu-id="bb89b-104">The Certificate Enrollment API supports the following basic ASN.1 types.</span></span>

## <a name="bit-string"></a><span data-ttu-id="bb89b-105">Bitzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bb89b-105">BIT STRING</span></span>

<span data-ttu-id="bb89b-106">Codierungstag: 0x03</span><span class="sxs-lookup"><span data-stu-id="bb89b-106">Encoding tag: 0x03</span></span>

<span data-ttu-id="bb89b-107">Certreq.exe Name: \_ Bitzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bb89b-107">Certreq.exe name: BIT\_STRING</span></span>

<span data-ttu-id="bb89b-108">Ein Bit oder eine binäre Zeichenfolge ist ein beliebig langes Array von Bits.</span><span class="sxs-lookup"><span data-stu-id="bb89b-108">A bit or binary string is an arbitrarily long array of bits.</span></span> <span data-ttu-id="bb89b-109">Bestimmte Bits können durch ganze Zahlen und zugewiesene Namen in Klammern identifiziert werden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="bb89b-109">Specific bits can be identified by parenthesized integers and assigned names as in the following example.</span></span>

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

<span data-ttu-id="bb89b-110">Zertifikat Schlüssel und Signaturen werden oft als Bitzeichenfolgen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bb89b-110">Certificate keys and signatures are often represented as bit strings.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BIT STRING
-- Tag number: 0x03
---------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
  algorithm           AlgorithmIdentifier,
  subjectPublicKey    BIT STRING
} 
```

## <a name="boolean"></a><span data-ttu-id="bb89b-111">BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bb89b-111">BOOLEAN</span></span>

<span data-ttu-id="bb89b-112">Codierungstag: 0x01</span><span class="sxs-lookup"><span data-stu-id="bb89b-112">Encoding tag: 0x01</span></span>

<span data-ttu-id="bb89b-113">Certreq.exe Name: Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="bb89b-113">Certreq.exe name: BOOLEAN</span></span>

<span data-ttu-id="bb89b-114">Ein boolescher Typ kann einen von zwei Werten enthalten: **true** oder **false**.</span><span class="sxs-lookup"><span data-stu-id="bb89b-114">A Boolean type can contain one of two values, **TRUE** or **FALSE**.</span></span> <span data-ttu-id="bb89b-115">Im folgenden Beispiel wird die ASN. 1-Struktur für eine grundlegende Einschränkungs Zertifikats Erweiterung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="bb89b-115">The following example shows the ASN.1 structure for a Basic Constraints certificate extension.</span></span> <span data-ttu-id="bb89b-116">Das **Feld** ZS gibt an, ob ein Zertifikat Antragsteller eine Zertifizierungsstelle (Certification Authority, ca) ist.</span><span class="sxs-lookup"><span data-stu-id="bb89b-116">The **cA** field specifies whether a certificate subject is a certification authority (CA).</span></span> <span data-ttu-id="bb89b-117">Die Standard Kritizität ist **false**.</span><span class="sxs-lookup"><span data-stu-id="bb89b-117">The default criticality is **FALSE**.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BOOLEAN
-- Tag number: 0x01
---------------------------------------------------------------------
BasicConstraints ::= SEQUENCE 
{
  cA                  BOOLEAN DEFAULT FALSE,
  pathLenConstraint   INTEGER OPTIONAL
}
```

## <a name="integer"></a><span data-ttu-id="bb89b-118">INTEGER</span><span class="sxs-lookup"><span data-stu-id="bb89b-118">INTEGER</span></span>

<span data-ttu-id="bb89b-119">Codierungstag: 0x02</span><span class="sxs-lookup"><span data-stu-id="bb89b-119">Encoding tag: 0x02</span></span>

<span data-ttu-id="bb89b-120">Certreq.exe Name: Integer</span><span class="sxs-lookup"><span data-stu-id="bb89b-120">Certreq.exe name: INTEGER</span></span>

<span data-ttu-id="bb89b-121">Eine ganze Zahl kann normalerweise ein beliebiger positiver oder negativer ganzzahliger Wert sein.</span><span class="sxs-lookup"><span data-stu-id="bb89b-121">An integer can typically be any positive or negative integral value.</span></span> <span data-ttu-id="bb89b-122">Das folgende Beispiel zeigt die ASN. 1-Struktur für einen öffentlichen RSA-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="bb89b-122">The following example shows the ASN.1 structure for an RSA public key.</span></span> <span data-ttu-id="bb89b-123">Beachten Sie, dass das Feld **publicexponent** auf eine positive ganze Zahl kleiner als 4.294.967.296 beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="bb89b-123">Note that the **publicExponent** field is restricted to a positive integer less than 4,294,967,296.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: INTEGER
-- Tag number: 0x02
---------------------------------------------------------------------
HUGEINTEGER ::= INTEGER

RSAPublicKey ::= SEQUENCE 
{ 
  modulus         HUGEINTEGER,    
  publicExponent  INTEGER (0..4294967295) 
} 
```

## <a name="null"></a><span data-ttu-id="bb89b-124">NULL</span><span class="sxs-lookup"><span data-stu-id="bb89b-124">NULL</span></span>

<span data-ttu-id="bb89b-125">Codierungstag: 0x05</span><span class="sxs-lookup"><span data-stu-id="bb89b-125">Encoding tag: 0x05</span></span>

<span data-ttu-id="bb89b-126">Certreq.exe Name: **null**</span><span class="sxs-lookup"><span data-stu-id="bb89b-126">Certreq.exe name: **NULL**</span></span>

<span data-ttu-id="bb89b-127">Ein **null** -Typ enthält ein einzelnes Byte 0x00.</span><span class="sxs-lookup"><span data-stu-id="bb89b-127">A **NULL** type contains a single byte 0x00.</span></span> <span data-ttu-id="bb89b-128">Sie kann überall dort verwendet werden, wo die Zertifikat Anforderung einen leeren Wert angeben muss.</span><span class="sxs-lookup"><span data-stu-id="bb89b-128">It can be used anywhere that the certificate request must indicate an empty value.</span></span> <span data-ttu-id="bb89b-129">Ein **AlgorithmIdentifier** ist z. b. eine Sequenz, die einen Objekt Bezeichner (OID) und optionale Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="bb89b-129">For example, an **AlgorithmIdentifier** is a sequence that contains an object identifier (OID) and optional parameters.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: NULL
-- Tag number: 0x05
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

<span data-ttu-id="bb89b-130">Wenn beim Codieren der Struktur keine Parameter vorhanden sind, wird **null** verwendet, um einen leeren Wert anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bb89b-130">If there are no parameters when the structure is encoded, **NULL** is used to indicate an empty value.</span></span>

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a><span data-ttu-id="bb89b-131">Objekt Bezeichner</span><span class="sxs-lookup"><span data-stu-id="bb89b-131">OBJECT IDENTIFIER</span></span>

<span data-ttu-id="bb89b-132">Codierungstag: 0x06</span><span class="sxs-lookup"><span data-stu-id="bb89b-132">Encoding tag: 0x06</span></span>

<span data-ttu-id="bb89b-133">Certreq.exe Name: Objekt- \_ ID</span><span class="sxs-lookup"><span data-stu-id="bb89b-133">Certreq.exe name: OBJECT\_ID</span></span>

<span data-ttu-id="bb89b-134">Die Zertifikatregistrierungs-API verwendet Objekt Bezeichner (OIDs) als Typ eines universellen Zeigers auf Algorithmusbezeichner, Attribute und andere PKI-Elemente.</span><span class="sxs-lookup"><span data-stu-id="bb89b-134">The Certificate Enrollment API uses object identifiers (OIDs) as a type of universal pointer to algorithm identifiers, attributes, and other PKI elements.</span></span> <span data-ttu-id="bb89b-135">OIDs werden in der Regel in einer punktierten Dezimal Zeichenfolge wie "2.16.840.1.101.3.4.1.42" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bb89b-135">OIDs are typically presented in a dotted decimal string such as "2.16.840.1.101.3.4.1.42".</span></span> <span data-ttu-id="bb89b-136">Die einzelnen Elemente in der Zeichenfolge, die durch Punkte voneinander getrennt sind, stellen die Bögen und Blätter in einer Registrierungsstelle dar, die das Objekt und die Organisation, die es registriert hat, eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bb89b-136">The individual elements in the string, separated by periods, represent the arcs and leaves in a registration authority tree that uniquely identifies the object and the organization that registered it.</span></span> <span data-ttu-id="bb89b-137">Beispiel: die vorangehende OID kann auf Joint-ISO-ITU-t (2) Country (16) US (840) Organization (1) gov (101) CSOR (3) nistalgorithms (4) aesalgs (1) mit angefügtem 42-Bit angehängt werden, um den Algorithmus für die Verschlüsselung des 256-Bit-AES-Verschlüsselungs Blocks (CBC</span><span class="sxs-lookup"><span data-stu-id="bb89b-137">For example, the preceding OID can be expanded to joint-iso-itu-t(2) country(16) us(840) organization(1) gov(101) csor(3) nistAlgorithms(4) aesAlgs(1) with .42 appended to uniquely identify the 256-bit AES cipher block chaining (CBC) mode algorithm.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OBJECT IDENTIFIER
-- Tag number: 0x06
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="octet-string"></a><span data-ttu-id="bb89b-138">Oktett-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bb89b-138">OCTET STRING</span></span>

<span data-ttu-id="bb89b-139">Codierungstag: 0x04</span><span class="sxs-lookup"><span data-stu-id="bb89b-139">Encoding tag: 0x04</span></span>

<span data-ttu-id="bb89b-140">Certreq.exe Name: Oktett- \_ Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bb89b-140">Certreq.exe name: OCTET\_STRING</span></span>

<span data-ttu-id="bb89b-141">Eine Oktett-Zeichenfolge ist ein beliebig großes Bytearray.</span><span class="sxs-lookup"><span data-stu-id="bb89b-141">An octet string is an arbitrarily large byte array.</span></span> <span data-ttu-id="bb89b-142">Im Gegensatz zum **bitstring** -Typ können bestimmten Bits und Bytes in der Zeichenfolge jedoch keine Namen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="bb89b-142">Unlike the **BIT STRING** type, however, specific bits and bytes in the string cannot be assigned names.</span></span> <span data-ttu-id="bb89b-143">Das Wort Oktett ist eine plattformunabhängige Methode zum Verweisen auf ein Arbeitsspeicher Wort.</span><span class="sxs-lookup"><span data-stu-id="bb89b-143">The word octet is meant to be a platform independent way to refer to a memory word.</span></span> <span data-ttu-id="bb89b-144">Im Kontext der Zertifikatregistrierungs-API sind Oktett und Byte austauschbar.</span><span class="sxs-lookup"><span data-stu-id="bb89b-144">Within the context of the Certificate Enrollment API, octet and byte are interchangeable.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OCTET STRING
-- Tag number: 0x04
---------------------------------------------------------------------
AuthorityKeyId ::= SEQUENCE 
{
  keyIdentifier       [0] IMPLICIT OCTET STRING OPTIONAL,
  certIssuer          [1] EXPLICIT NAME
  certSerialNumber    [2] IMPLICIT INTEGER OPTIONAL
}
```

## <a name="related-topics"></a><span data-ttu-id="bb89b-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb89b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb89b-146">ASN. 1-Typsystem</span><span class="sxs-lookup"><span data-stu-id="bb89b-146">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="bb89b-147">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="bb89b-147">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="bb89b-148">Der-Codierung von ASN. 1-Typen</span><span class="sxs-lookup"><span data-stu-id="bb89b-148">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




---
description: Eine der häufigsten Verwendungen von Zeichen folgen in einer Public Key-Infrastruktur (PKI) ist das Erstellen eines X. 500-Distinguished Name.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Zeichen folgen Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1173de3b2c4c5fd64181cd19c69cfbcecb1d584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216000"
---
# <a name="string-types"></a><span data-ttu-id="fc018-103">Zeichen folgen Typen</span><span class="sxs-lookup"><span data-stu-id="fc018-103">String Types</span></span>

<span data-ttu-id="fc018-104">Eine der häufigsten Verwendungen von Zeichen folgen in einer Public Key-Infrastruktur (PKI) ist das Erstellen eines X. 500-Distinguished Name.</span><span class="sxs-lookup"><span data-stu-id="fc018-104">One of the most common uses of strings in a public key infrastructure (PKI) is to create an X.500 Distinguished Name.</span></span> <span data-ttu-id="fc018-105">Beispielsweise wird der Antragsteller Name einer Zertifikat Anforderung durch Kombinieren einer Sequenz von relativen Distinguished Names erstellt, wie im folgenden Syntax Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc018-105">For example, the subject name of a certificate request is created by combining a sequence of relative distinguished names as shown in the following syntax example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Breakdown of a subject name in a certificate request.
---------------------------------------------------------------------

CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

<span data-ttu-id="fc018-106">Die Zertifikatregistrierungs-API unterstützt die folgenden ASN. 1-Zeichen folgen Typen.</span><span class="sxs-lookup"><span data-stu-id="fc018-106">The Certificate Enrollment API supports the following ASN.1 string types.</span></span>

## <a name="bmpstring"></a><span data-ttu-id="fc018-107">Bmpstring</span><span class="sxs-lookup"><span data-stu-id="fc018-107">BMPString</span></span>

<span data-ttu-id="fc018-108">Codierungstag: 0x1E</span><span class="sxs-lookup"><span data-stu-id="fc018-108">Encoding tag: 0x1E</span></span>

<span data-ttu-id="fc018-109">Certreq.exe Name: Unicode- \_ Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fc018-109">Certreq.exe name: UNICODE\_STRING</span></span>

<span data-ttu-id="fc018-110">Bei der grundlegenden mehrsprachigen Ebene (BMP) handelt es sich um eine Zeichencodierung, die die erste Ebene des universellen Zeichensatzes (UCS) umfasst.</span><span class="sxs-lookup"><span data-stu-id="fc018-110">The Basic Multilingual Plane (BMP) is a character encoding that encompasses the first plane of the Universal Character Set (UCS).</span></span> <span data-ttu-id="fc018-111">Es gibt 17 Flächen mit der Nummerierung 0 bis 16.</span><span class="sxs-lookup"><span data-stu-id="fc018-111">There are seventeen planes numbered 0 to 16.</span></span> <span data-ttu-id="fc018-112">BMP belegt die Ebene 0 und umfasst 65.536-Code Punkte von 0x0000 bis 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="fc018-112">BMP occupies plane 0 and includes 65,536 code points from 0x0000 to 0xFFFF.</span></span> <span data-ttu-id="fc018-113">Dies ist der Abschnitt der Unicode-Zeichen Zuordnung, in der die meisten Zeichen Zuweisungen bisher vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="fc018-113">This is the section of the Unicode character map where most of the characters assignments have so far been made.</span></span> <span data-ttu-id="fc018-114">Es umfasst lateinische, mittlere Osten, asiatische, afrikanische und andere Sprachen.</span><span class="sxs-lookup"><span data-stu-id="fc018-114">It includes Latin, Middle Eastern, Asian, African, and other languages.</span></span>

## <a name="ia5string"></a><span data-ttu-id="fc018-115">IA5String</span><span class="sxs-lookup"><span data-stu-id="fc018-115">IA5String</span></span>

<span data-ttu-id="fc018-116">Codierungstag: 0x16</span><span class="sxs-lookup"><span data-stu-id="fc018-116">Encoding tag: 0x16</span></span>

<span data-ttu-id="fc018-117">Certreq.exe Name: IA5 \_ String</span><span class="sxs-lookup"><span data-stu-id="fc018-117">Certreq.exe name: IA5\_STRING</span></span>

<span data-ttu-id="fc018-118">Die internationale Alphabet Nummer 5 (IA5) entspricht im Allgemeinen dem ASCII-Alphabet, aber unterschiedliche Versionen können Akzente oder andere Zeichen enthalten, die für eine regionale Sprache spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="fc018-118">The International Alphabet number 5 (IA5) is generally equivalent to the ASCII alphabet, but different versions can include accents or other characters specific to a regional language.</span></span> <span data-ttu-id="fc018-119">Das folgende Beispiel zeigt den **IA5String** -Typ, der in der ASN. 1-Definition der " **alternativenames** "-Zertifikat Erweiterung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc018-119">The following example shows the **IA5String** type used in the ASN.1 definition of the **AlternativeNames** certificate extension.</span></span>

``` syntax
---------------------------------------------------------------------
-- AlternativeNames extension
---------------------------------------------------------------------

AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SEQUENCE OF ANY, 
   directoryName           [4] EXPLICIT ANY,    
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}

OtherName ::= SEQUENCE 
{
   type                    OBJECT IDENTIFIER,
   value                   [0] EXPLICIT ANY 
}
```

## <a name="printablestring"></a><span data-ttu-id="fc018-120">PrintableString</span><span class="sxs-lookup"><span data-stu-id="fc018-120">PrintableString</span></span>

<span data-ttu-id="fc018-121">Codierungstag: 0x13</span><span class="sxs-lookup"><span data-stu-id="fc018-121">Encoding tag: 0x13</span></span>

<span data-ttu-id="fc018-122">Certreq.exe Name: druckbare \_ Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fc018-122">Certreq.exe name: PRINTABLE\_STRING</span></span>

<span data-ttu-id="fc018-123">Der **PrintableString** -Datentyp war ursprünglich für die Darstellung der beschränkten Zeichensätze vorgesehen, die für die Main Frame-Eingabe Terminals verfügbar waren, wird aber immer noch häufig verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc018-123">The **PrintableString** data type was originally intended to represent the limited character sets available to mainframe input terminals, but it is still commonly used.</span></span> <span data-ttu-id="fc018-124">Sie enthält die folgenden Zeichen:</span><span class="sxs-lookup"><span data-stu-id="fc018-124">It contains the following characters:</span></span>

-   <span data-ttu-id="fc018-125">A-Z</span><span class="sxs-lookup"><span data-stu-id="fc018-125">A-Z</span></span>
-   <span data-ttu-id="fc018-126">a-z</span><span class="sxs-lookup"><span data-stu-id="fc018-126">a-z</span></span>
-   <span data-ttu-id="fc018-127">0-9</span><span class="sxs-lookup"><span data-stu-id="fc018-127">0-9</span></span>
-   <span data-ttu-id="fc018-128">' ( ) + , - .</span><span class="sxs-lookup"><span data-stu-id="fc018-128">' ( ) + , - .</span></span> <span data-ttu-id="fc018-129">/ : = ?</span><span class="sxs-lookup"><span data-stu-id="fc018-129">/ : = ?</span></span> <span data-ttu-id="fc018-130">\[space\]</span><span class="sxs-lookup"><span data-stu-id="fc018-130">\[space\]</span></span>

## <a name="teletexstring"></a><span data-ttu-id="fc018-131">Teletexstring</span><span class="sxs-lookup"><span data-stu-id="fc018-131">TeletexString</span></span>

<span data-ttu-id="fc018-132">Codierungstag: 0x14</span><span class="sxs-lookup"><span data-stu-id="fc018-132">Encoding tag: 0x14</span></span>

<span data-ttu-id="fc018-133">Die **teletexstring** -und die Related **T61String** -Datentypen werden in 8 Bits (oder 16 Bits für Verbund Zeichen) codiert.</span><span class="sxs-lookup"><span data-stu-id="fc018-133">The **TeletexString** and the related **T61String** data types are encoded on 8 bits (or 16 bits for composite characters).</span></span> <span data-ttu-id="fc018-134">Beide haben eine Tagnummer von 0x14.</span><span class="sxs-lookup"><span data-stu-id="fc018-134">They both have a tag number of 0x14.</span></span> <span data-ttu-id="fc018-135">Sie werden nicht ausführlich verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc018-135">They are not extensively used.</span></span>

## <a name="utf8string"></a><span data-ttu-id="fc018-136">UTF8String</span><span class="sxs-lookup"><span data-stu-id="fc018-136">UTF8String</span></span>

<span data-ttu-id="fc018-137">Codierungstag: 0x0c</span><span class="sxs-lookup"><span data-stu-id="fc018-137">Encoding tag: 0x0C</span></span>

<span data-ttu-id="fc018-138">Certreq.exe Name: UTF8- \_ Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fc018-138">Certreq.exe name: UTF8\_STRING</span></span>

<span data-ttu-id="fc018-139">Beim 8-Bit-UCS/Unicode-Transformations Format (UTF-8) handelt es sich um eine Zeichencodierung variabler Länge, die jedes universelle Zeichen als Unicode-Zeichen darstellen kann, und das zulassen, dass anfängliche Code Punkte mit ASCII konsistent bleiben.</span><span class="sxs-lookup"><span data-stu-id="fc018-139">The 8-bit UCS/Unicode Transformation Format (UTF-8) is a variable-length character encoding that can represent any universal character as a Unicode character while allowing initial code points to remain consistent with ASCII.</span></span> <span data-ttu-id="fc018-140">UTF-8 verwendet ein bis vier Bytes.</span><span class="sxs-lookup"><span data-stu-id="fc018-140">UTF-8 uses one to four bytes.</span></span> <span data-ttu-id="fc018-141">Die Tagnummer ist 0x0c.</span><span class="sxs-lookup"><span data-stu-id="fc018-141">The tag number is 0x0C.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc018-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fc018-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc018-143">ASN. 1-Typsystem</span><span class="sxs-lookup"><span data-stu-id="fc018-143">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="fc018-144">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="fc018-144">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="fc018-145">Der-Codierung von ASN. 1-Typen</span><span class="sxs-lookup"><span data-stu-id="fc018-145">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




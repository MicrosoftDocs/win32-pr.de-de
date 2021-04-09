---
description: Ein X. 509-Zertifikat der Version 1 enthält die folgenden Felder. Die Felder der Version 2 werden in den Feldern der Version 2 behandelt. Die Felder der Version 3 werden in den Erweiterungen der Version 3 erläutert.
ms.assetid: d614130c-cf1b-4580-8903-064982ed738e
title: Grundlegende Felder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad24afa21787227b3fe47ab187a97c7886c9c9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865036"
---
# <a name="basic-fields"></a><span data-ttu-id="49e57-105">Grundlegende Felder</span><span class="sxs-lookup"><span data-stu-id="49e57-105">Basic Fields</span></span>

<span data-ttu-id="49e57-106">Ein X. 509-Zertifikat der Version 1 enthält die folgenden Felder.</span><span class="sxs-lookup"><span data-stu-id="49e57-106">An X.509 version 1 certificate contains the following fields.</span></span> <span data-ttu-id="49e57-107">Die Felder der Version 2 werden in den [Feldern der Version 2](about-version-2-fields.md)behandelt.</span><span class="sxs-lookup"><span data-stu-id="49e57-107">Version 2 fields are discussed in [Version 2 Fields](about-version-2-fields.md).</span></span> <span data-ttu-id="49e57-108">Die Felder der Version 3 werden in den [Erweiterungen der Version 3](about-version-3-extensions.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="49e57-108">Version 3 fields are discussed in [Version 3 Extensions](about-version-3-extensions.md).</span></span>

## <a name="version"></a><span data-ttu-id="49e57-109">Version</span><span class="sxs-lookup"><span data-stu-id="49e57-109">Version</span></span>

<span data-ttu-id="49e57-110">Gibt die Versionsnummer des codierten Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="49e57-110">Specifies the version number of the encoded certificate.</span></span> <span data-ttu-id="49e57-111">Derzeit sind die möglichen Werte für dieses Feld "0", "1" oder "2". Dies kann jedoch in Zukunft erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="49e57-111">Currently, the possible values of this field are 0, 1, or 2, but this may be expanded in the future.</span></span>

``` syntax
---------------------------------------------------------------------
-- Version number. Currently, this can be 0, 1, or 2.
---------------------------------------------------------------------
CertificateVersion ::= INTEGER {v1(0), v2(1), v3(2)}
```

## <a name="serial-number"></a><span data-ttu-id="49e57-112">Seriennummer</span><span class="sxs-lookup"><span data-stu-id="49e57-112">Serial Number</span></span>

<span data-ttu-id="49e57-113">Enthält eine positive, eindeutige Ganzzahl, die dem Zertifikat von der Zertifizierungsstelle zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="49e57-113">Contains a positive, unique integer assigned by the certification authority (CA) to the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Certificate serial number
---------------------------------------------------------------------
CertificateSerialNumber ::= INTEGER
```

## <a name="signature-algorithm"></a><span data-ttu-id="49e57-114">Signaturalgorithmus</span><span class="sxs-lookup"><span data-stu-id="49e57-114">Signature Algorithm</span></span>

<span data-ttu-id="49e57-115">Enthält einen [*Objekt Bezeichner*](/windows/desktop/SecGloss/o-gly) (OID), der den Algorithmus angibt, der von der Zertifizierungsstelle zum Signieren des Zertifikats verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49e57-115">Contains an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) that specifies the algorithm used by the CA to sign the certificate.</span></span> <span data-ttu-id="49e57-116">1.2.840.113549.1.1.5 gibt beispielsweise einen SHA-1-Hashalgorithmus an, der mit dem RSA-Verschlüsselungsalgorithmus von RSA Laboratories kombiniert ist.</span><span class="sxs-lookup"><span data-stu-id="49e57-116">For example, 1.2.840.113549.1.1.5 specifies a SHA-1 hashing algorithm combined with the RSA encryption algorithm from RSA Laboratories.</span></span>

``` syntax
---------------------------------------------------------------------
-- Signature OID
---------------------------------------------------------------------
signature ::= AlgorithmIdentifier

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="issuer"></a><span data-ttu-id="49e57-117">Issuer (Aussteller)</span><span class="sxs-lookup"><span data-stu-id="49e57-117">Issuer</span></span>

<span data-ttu-id="49e57-118">Enthält den [*X. 500*](/windows/desktop/SecGloss/x-gly) Distinguished Name (DN) der Zertifizierungsstelle, die das Zertifikat erstellt und signiert hat.</span><span class="sxs-lookup"><span data-stu-id="49e57-118">Contains the [*X.500*](/windows/desktop/SecGloss/x-gly) distinguished name (DN) of the CA that created and signed the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="validity"></a><span data-ttu-id="49e57-119">Gültigkeitsdauer</span><span class="sxs-lookup"><span data-stu-id="49e57-119">Validity</span></span>

<span data-ttu-id="49e57-120">Gibt die Zeitspanne an, für die das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="49e57-120">Specifies the time interval during which the certificate is valid.</span></span> <span data-ttu-id="49e57-121">Datumsangaben bis zum Ende 2049 verwenden das koordinierte Weltzeit (Greenwich Mean Time)-Format (*yymmddhhmmssZ*).</span><span class="sxs-lookup"><span data-stu-id="49e57-121">Dates through the end of 2049 use the Coordinated Universal Time (Greenwich Mean Time) format (*yymmddhhmmssz*).</span></span> <span data-ttu-id="49e57-122">Datumsangaben ab dem 1. Januar 2050 verwenden das verallgemeinerte Zeitformat (*yyyymmddhhmmssZ*).</span><span class="sxs-lookup"><span data-stu-id="49e57-122">Dates beginning with January 1st, 2050 use the generalized time format (*yyyymmddhhmmssz*).</span></span>

``` syntax
---------------------------------------------------------------------
-- Validity period 
---------------------------------------------------------------------
Validity ::= SEQUENCE 
{
  notBefore           ChoiceOfTime,
  notAfter            ChoiceOfTime
}

ChoiceOfTime ::= CHOICE 
{
  utcTime                 UTCTime,
  generalTime             GeneralizedTime
}
```

## <a name="subject"></a><span data-ttu-id="49e57-123">Subject</span><span class="sxs-lookup"><span data-stu-id="49e57-123">Subject</span></span>

<span data-ttu-id="49e57-124">Enthält einen X.500-Distinguished Name der Entität, die dem öffentlichen Schlüssel im Zertifikat zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="49e57-124">Contains an X.500 distinguished name of the entity associated with the public key contained in the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Subject name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="public-key"></a><span data-ttu-id="49e57-125">Öffentlicher Schlüssel</span><span class="sxs-lookup"><span data-stu-id="49e57-125">Public Key</span></span>

<span data-ttu-id="49e57-126">Enthält den öffentlichen Schlüssel und Informationen zum zugehörigen Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="49e57-126">Contains the public key and associated algorithm information.</span></span>

``` syntax
---------------------------------------------------------------------
--  Subject public key information
---------------------------------------------------------------------
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
```

## <a name="related-topics"></a><span data-ttu-id="49e57-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49e57-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49e57-128">Felder der Version 2</span><span class="sxs-lookup"><span data-stu-id="49e57-128">Version 2 Fields</span></span>](about-version-2-fields.md)
</dt> <dt>

[<span data-ttu-id="49e57-129">Erweiterungen der Version 3</span><span class="sxs-lookup"><span data-stu-id="49e57-129">Version 3 Extensions</span></span>](about-version-3-extensions.md)
</dt> <dt>

[<span data-ttu-id="49e57-130">X. 509-Zertifikate für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="49e57-130">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 

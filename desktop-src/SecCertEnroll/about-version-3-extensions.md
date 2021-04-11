---
description: Ein X.509-Zertifikat der Version 3 enthält die Felder, die in Version 1 und Version 2 definiert sind, und es werden Zertifikaterweiterungen hinzugefügt. Die ASN. 1-Syntax von Zertifikat Erweiterungen wird im folgenden Beispiel gezeigt.
ms.assetid: ca8df7a4-caa4-4fe7-81a8-8fce372454f4
title: Erweiterungen der Version 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee23ce35ba7031a1a9f7a2c9caa79fd955ccbe2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215999"
---
# <a name="version-3-extensions"></a><span data-ttu-id="c94ae-104">Erweiterungen der Version 3</span><span class="sxs-lookup"><span data-stu-id="c94ae-104">Version 3 Extensions</span></span>

<span data-ttu-id="c94ae-105">Ein X.509-Zertifikat der Version 3 enthält die Felder, die in Version 1 und Version 2 definiert sind, und es werden Zertifikaterweiterungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c94ae-105">An X.509 version 3 certificate contains the fields defined in version 1 and version 2 and adds certificate extensions.</span></span> <span data-ttu-id="c94ae-106">Die ASN. 1-Syntax von Zertifikat Erweiterungen wird im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c94ae-106">The ASN.1 syntax of certificate extensions is shown in the following example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Extensions (beginning with version 3).
---------------------------------------------------------------------
Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
  Id                  OBJECT IDENTIFIER,
  critical            BOOLEAN DEFAULT FALSE,
  extnValue           OCTET STRING
}
```

<span data-ttu-id="c94ae-107">In der folgenden Tabelle sind die Standard Erweiterungen der Version 3 und ihre Objekt-IDs (OIDs) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c94ae-107">The standard version 3 extensions and their object identifiers (OIDs) are listed in the following table.</span></span> <span data-ttu-id="c94ae-108">Microsoft unterstützt diese und umfasst zusätzliche benutzerdefinierte Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="c94ae-108">Microsoft supports these and includes additional custom extensions.</span></span> <span data-ttu-id="c94ae-109">Weitere Informationen finden Sie unter [Erweiterungen](extensions.md).</span><span class="sxs-lookup"><span data-stu-id="c94ae-109">For more information, see [Extensions](extensions.md).</span></span>

| <span data-ttu-id="c94ae-110">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="c94ae-110">Extension</span></span>                                         | <span data-ttu-id="c94ae-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c94ae-111">Description</span></span>                                                                                                                                                                                              |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c94ae-112">Autoritäts Bezeichner der Zertifizierungsstelle (2.5.29.19)</span><span class="sxs-lookup"><span data-stu-id="c94ae-112">Authority Key Identifier(2.5.29.19)</span></span><br/>    | <span data-ttu-id="c94ae-113">Gibt den öffentlichen Schlüssel der Zertifizierungsstelle an, der dem privaten Schlüssel der Zertifizierungsstelle entspricht, mit dem das Zertifikat signiert wird.</span><span class="sxs-lookup"><span data-stu-id="c94ae-113">Identifies the certification authority (CA) public key that corresponds to the CA private key used to sign the certificate.</span></span>                                                                              |
| <span data-ttu-id="c94ae-114">Grundlegende Einschränkungen (2.5.29.35)</span><span class="sxs-lookup"><span data-stu-id="c94ae-114">Basic Constraints(2.5.29.35)</span></span><br/>           | <span data-ttu-id="c94ae-115">Gibt an, ob die Entität als Zertifizierungsstelle fungieren kann, und wenn dies der Fall ist, wie viele untergeordnete Zertifizierungsstellen in der Zertifikatkette darunter vorhanden sein können.</span><span class="sxs-lookup"><span data-stu-id="c94ae-115">Specifies whether the entity can be used as a CA and, if so, the number of subordinate CAs that can exist beneath it in the certificate chain.</span></span>                                                           |
| <span data-ttu-id="c94ae-116">Zertifikat Richtlinien (2.5.29.32)</span><span class="sxs-lookup"><span data-stu-id="c94ae-116">Certificate Policies(2.5.29.32)</span></span><br/>        | <span data-ttu-id="c94ae-117">Gibt die Richtlinien an, unter denen das Zertifikat ausgestellt wurde, sowie die Zwecke, für die es genutzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c94ae-117">Specifies the policies under which the certificate has been issued and the purposes for which it can be used.</span></span>                                                                                            |
| <span data-ttu-id="c94ae-118">CRL-Verteilungs Punkte (2.5.29.31)</span><span class="sxs-lookup"><span data-stu-id="c94ae-118">CRL Distribution Points(2.5.29.31)</span></span><br/>     | <span data-ttu-id="c94ae-119">Enthält den URI der Basis [*Zertifikat Sperr Liste*](/windows/desktop/SecGloss/c-gly) (CRL).</span><span class="sxs-lookup"><span data-stu-id="c94ae-119">Contains the URI of the base [*certificate revocation list*](/windows/desktop/SecGloss/c-gly) (CRL).</span></span>                                  |
| <span data-ttu-id="c94ae-120">Erweiterte Schlüssel Verwendung (2.5.29.46)</span><span class="sxs-lookup"><span data-stu-id="c94ae-120">Enhanced Key Usage(2.5.29.46)</span></span><br/>          | <span data-ttu-id="c94ae-121">Gibt die Art und Weise an, in welcher der öffentliche Schlüssel im Zertifikat verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c94ae-121">Specifies the manner in which the public key contained in the certificate can be used.</span></span>                                                                                                                   |
| <span data-ttu-id="c94ae-122">Alternativer Aussteller Name (2.5.29.8)</span><span class="sxs-lookup"><span data-stu-id="c94ae-122">Issuer Alternative Name(2.5.29.8)</span></span><br/>      | <span data-ttu-id="c94ae-123">Gibt einen oder mehrere alternative Namen für den Aussteller der Zertifikatanforderung an.</span><span class="sxs-lookup"><span data-stu-id="c94ae-123">Specifies one or more alternative name forms for the issuer of the certificate request.</span></span>                                                                                                                  |
| <span data-ttu-id="c94ae-124">Schlüssel Verwendung (2.5.29.15)</span><span class="sxs-lookup"><span data-stu-id="c94ae-124">Key Usage(2.5.29.15)</span></span><br/>                   | <span data-ttu-id="c94ae-125">Gibt die Einschränkungen für die Vorgänge an, die durch den öffentlichen Schlüssel im Zertifikat ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c94ae-125">Specifies restrictions on the operations that can be performed by the public key contained in the certificate.</span></span>                                                                                           |
| <span data-ttu-id="c94ae-126">Namens Einschränkungen (2.5.29.30)</span><span class="sxs-lookup"><span data-stu-id="c94ae-126">Name Constraints(2.5.29.30)</span></span><br/>            | <span data-ttu-id="c94ae-127">Gibt den Namespace an, in dem alle Antragstellernamen in einer Zertifikathierarchie liegen müssen.</span><span class="sxs-lookup"><span data-stu-id="c94ae-127">Specifies the namespace within which all subject names in a certificate hierarchy must be located.</span></span> <span data-ttu-id="c94ae-128">Die Erweiterung wird lediglich in einem Zertifizierungsstellenzertifikat verwendet.</span><span class="sxs-lookup"><span data-stu-id="c94ae-128">The extension is used only in a CA certificate.</span></span>                                                       |
| <span data-ttu-id="c94ae-129">Richtlinien Einschränkungen (2.5.29.36)</span><span class="sxs-lookup"><span data-stu-id="c94ae-129">Policy Constraints(2.5.29.36)</span></span><br/>          | <span data-ttu-id="c94ae-130">Schränkt die Zertifikatüberprüfung ein, indem die Richtlinienzuordnung untersagt oder gefordert wird, dass jedes Zertifikat in der Hierarchie eine akzeptable Richtlinienkennung aufweisen muss.</span><span class="sxs-lookup"><span data-stu-id="c94ae-130">Constrains path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</span></span> <span data-ttu-id="c94ae-131">Die Erweiterung wird lediglich in einem Zertifizierungsstellenzertifikat verwendet.</span><span class="sxs-lookup"><span data-stu-id="c94ae-131">The extension is used only in a CA certificate.</span></span> |
| <span data-ttu-id="c94ae-132">Richtlinien Zuordnungen (2.5.29.33)</span><span class="sxs-lookup"><span data-stu-id="c94ae-132">Policy Mappings(2.5.29.33)</span></span><br/>             | <span data-ttu-id="c94ae-133">Gibt die Richtlinien in einer untergeordneten Zertifizierungsstelle an, die Richtlinien in der ausstellenden Zertifizierungsstelle entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c94ae-133">Specifies the policies in a subordinate CA that correspond to policies in the issuing CA.</span></span>                                                                                                                |
| <span data-ttu-id="c94ae-134">Verwendungs Zeitraum für privaten Schlüssel (2.5.29.16)</span><span class="sxs-lookup"><span data-stu-id="c94ae-134">Private Key Usage Period(2.5.29.16)</span></span><br/>    | <span data-ttu-id="c94ae-135">Gibt einen anderen Gültigkeitszeitraum für den privaten Schlüssel als für das Zertifikat an, dem der private Schlüssel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c94ae-135">Specifies a different validity period for the private key than for the certificate with which the private key is associated.</span></span>                                                                             |
| <span data-ttu-id="c94ae-136">Alternativer Antragsteller Name (2.5.29.17)</span><span class="sxs-lookup"><span data-stu-id="c94ae-136">Subject Alternative Name(2.5.29.17)</span></span><br/>    | <span data-ttu-id="c94ae-137">Gibt einen oder mehrere alternative Namen für den Antragsteller der Zertifikatanforderung an.</span><span class="sxs-lookup"><span data-stu-id="c94ae-137">Specifies one or more alternative name forms for the subject of the certificate request.</span></span> <span data-ttu-id="c94ae-138">Beispiele für alternative Namen sind E-Mail-Adressen, DNS-Namen, IP-Adressen und URIs.</span><span class="sxs-lookup"><span data-stu-id="c94ae-138">Example alternative forms include email addresses, DNS names, IP addresses, and URIs.</span></span>                           |
| <span data-ttu-id="c94ae-139">Attribute des betreffverzeichnisses (2.5.29.9)</span><span class="sxs-lookup"><span data-stu-id="c94ae-139">Subject Directory Attributes(2.5.29.9)</span></span><br/> | <span data-ttu-id="c94ae-140">Vermittelt identifizierende Attribute, beispielsweise die Nationalität des Zertifikatantragstellers.</span><span class="sxs-lookup"><span data-stu-id="c94ae-140">Conveys identification attributes such as the nationality of the certificate subject.</span></span> <span data-ttu-id="c94ae-141">Der Erweiterungswert ist eine Folge von OID-Wertepaaren.</span><span class="sxs-lookup"><span data-stu-id="c94ae-141">The extension value is a sequence of OID-value pairs.</span></span>                                                              |
| <span data-ttu-id="c94ae-142">Subjekt Schlüssel Bezeichner (2.5.29.14)</span><span class="sxs-lookup"><span data-stu-id="c94ae-142">Subject Key Identifier(2.5.29.14)</span></span><br/>      | <span data-ttu-id="c94ae-143">Unterscheidet zwischen mehreren öffentlichen Schlüsseln im Besitz des Zertifikatantragstellers.</span><span class="sxs-lookup"><span data-stu-id="c94ae-143">Differentiates between multiple public keys held by the certificate subject.</span></span> <span data-ttu-id="c94ae-144">Der Erweiterungswert ist normalerweise ein SHA-1-Hash des Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="c94ae-144">The extension value is typically a SHA-1 hash of the key.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="c94ae-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c94ae-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c94ae-146">Grundlegende Felder</span><span class="sxs-lookup"><span data-stu-id="c94ae-146">Basic Fields</span></span>](about-basic-fields.md)
</dt> <dt>

[<span data-ttu-id="c94ae-147">Felder der Version 2</span><span class="sxs-lookup"><span data-stu-id="c94ae-147">Version 2 Fields</span></span>](about-version-2-fields.md)
</dt> <dt>

[<span data-ttu-id="c94ae-148">X. 509-Zertifikate für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c94ae-148">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 


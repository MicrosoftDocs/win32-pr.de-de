---
description: Die Kryptografie mit öffentlichem Schlüssel basiert auf einem Paar aus öffentlichem und privatem Schlüssel zum Verschlüsseln und Entschlüsseln von Inhalt.
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: X. 509-Zertifikate für öffentliche Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acd602e9b47cb7825f6d75df0fb74399b914db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565760"
---
# <a name="x509-public-key-certificates"></a><span data-ttu-id="584f5-103">X. 509-Zertifikate für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="584f5-103">X.509 Public Key Certificates</span></span>

<span data-ttu-id="584f5-104">Die Kryptografie mit öffentlichem Schlüssel basiert auf einem Paar aus öffentlichem und privatem Schlüssel zum Verschlüsseln und Entschlüsseln von Inhalt.</span><span class="sxs-lookup"><span data-stu-id="584f5-104">Public key cryptography relies on a public and private key pair to encrypt and decrypt content.</span></span> <span data-ttu-id="584f5-105">Die Schlüssel sind mathematisch miteinander verknüpft, und Inhalte, die mit einem der Schlüssel verschlüsselt wurden, können nur mit dem anderen entschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="584f5-105">The keys are mathematically related, and content encrypted by using one of the keys can only be decrypted by using the other.</span></span> <span data-ttu-id="584f5-106">Der private Schlüssel wird geheim gehalten.</span><span class="sxs-lookup"><span data-stu-id="584f5-106">The private key is kept secret.</span></span> <span data-ttu-id="584f5-107">Der öffentliche Schlüssel ist in der Regel in ein binäres Zertifikat eingebettet, und das Zertifikat wird in einer Datenbank veröffentlicht, die von allen autorisierten Benutzern erreicht werden kann.</span><span class="sxs-lookup"><span data-stu-id="584f5-107">The public key is typically embedded in a binary certificate, and the certificate is published to a database that can be reached by all authorized users.</span></span>

<span data-ttu-id="584f5-108">Der X. 509-PKI-Standard (Public Key Infrastructure) identifiziert die Anforderungen für robuste Zertifikate für öffentliche Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="584f5-108">The X.509 public key infrastructure (PKI) standard identifies the requirements for robust public key certificates.</span></span> <span data-ttu-id="584f5-109">Ein Zertifikat ist eine signierte Datenstruktur, die einen öffentlichen Schlüssel an eine Person, einen Computer oder eine Organisation bindet.</span><span class="sxs-lookup"><span data-stu-id="584f5-109">A certificate is a signed data structure that binds a public key to a person, computer, or organization.</span></span> <span data-ttu-id="584f5-110">Zertifikate werden von [*Zertifizierungs*](/windows/desktop/SecGloss/c-gly) stellen (CAS) ausgestellt.</span><span class="sxs-lookup"><span data-stu-id="584f5-110">Certificates are issued by [*certification authorities*](/windows/desktop/SecGloss/c-gly) (CAs).</span></span> <span data-ttu-id="584f5-111">Alle Personen, die die Kommunikation mit einem öffentlichen Schlüssel unterstützen, verlassen sich auf die Zertifizierungsstelle, um die Identitäten der Personen, Systeme oder Entitäten, für die Zertifikate ausgestellt werden, adäquat zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="584f5-111">All who are party to secure communications that make use of a public key rely on the CA to adequately verify the identities of the individuals, systems, or entities to which it issues certificates.</span></span> <span data-ttu-id="584f5-112">Die Ebene der Überprüfung hängt in der Regel von der Sicherheitsstufe ab, die für die Transaktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="584f5-112">The level of verification typically depends on the level of security required for the transaction.</span></span> <span data-ttu-id="584f5-113">Wenn die Zertifizierungsstelle die Identität des Anforderers entsprechend überprüfen kann, wird das Zertifikat signiert (verschlüsselt), codiert und ausgestellt.</span><span class="sxs-lookup"><span data-stu-id="584f5-113">If the CA can suitably verify the identity of the requester, it signs (encrypts), encodes, and issues the certificate.</span></span>

<span data-ttu-id="584f5-114">Ein Zertifikat ist eine signierte Datenstruktur, die einen öffentlichen Schlüssel an eine Entität bindet.</span><span class="sxs-lookup"><span data-stu-id="584f5-114">A certificate is a signed data structure that binds a public key to an entity.</span></span> <span data-ttu-id="584f5-115">Die Syntax für die [*abstrakte Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN. 1) für das [*X. 509*](/windows/desktop/SecGloss/x-gly) -Zertifikat der Version 3 wird im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="584f5-115">The [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) syntax for the version 3 [*X.509*](/windows/desktop/SecGloss/x-gly) certificate is shown in the following example.</span></span>

``` syntax
-- X.509 signed certificate 

SignedContent ::= SEQUENCE 
{
  certificate         CertificateToBeSigned,
  algorithm           Object Identifier,
  signature           BITSTRING
}
 
-- X.509 certificate to be signed

CertificateToBeSigned ::= SEQUENCE 
{
  version                 [0] CertificateVersion DEFAULT v1,
  serialNumber            CertificateSerialNumber,
  signature               AlgorithmIdentifier,
  issuer                  Name
  validity                Validity,
  subject                 Name
  subjectPublicKeyInfo    SubjectPublicKeyInfo,
  issuerUniqueIdentifier  [1] IMPLICIT UniqueIdentifier OPTIONAL,
  subjectUniqueIdentifier [2] IMPLICIT UniqueIdentifier OPTIONAL,
  extensions              [3] Extensions OPTIONAL
}
```

<span data-ttu-id="584f5-116">Seit seiner Einführung in 1998 haben sich drei Versionen des öffentlichen X. 509-Zertifikat Standards entwickelt.</span><span class="sxs-lookup"><span data-stu-id="584f5-116">Since its inception in 1998, three versions of the X.509 public key certificate standard have evolved.</span></span> <span data-ttu-id="584f5-117">Wie in der folgenden Abbildung dargestellt, hat jede aufeinander folgende Version der Datenstruktur die Felder, die in den vorherigen Versionen vorhanden waren, aufbewahrt und weitere hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="584f5-117">As shown by the following illustration, each successive version of the data structure has retained the fields that existed in the previous versions and added more.</span></span>

![x. 509-Zertifikate, Versionen 1, 2 und 3](images/x509certificateversions.png)

<span data-ttu-id="584f5-119">In den folgenden Themen werden die verfügbaren Felder ausführlicher erläutert:</span><span class="sxs-lookup"><span data-stu-id="584f5-119">The following topics discuss the available fields in more detail:</span></span>

-   [<span data-ttu-id="584f5-120">Grundlegende Felder</span><span class="sxs-lookup"><span data-stu-id="584f5-120">Basic Fields</span></span>](about-basic-fields.md)
-   [<span data-ttu-id="584f5-121">Felder der Version 2</span><span class="sxs-lookup"><span data-stu-id="584f5-121">Version 2 Fields</span></span>](about-version-2-fields.md)
-   [<span data-ttu-id="584f5-122">Erweiterungen der Version 3</span><span class="sxs-lookup"><span data-stu-id="584f5-122">Version 3 Extensions</span></span>](about-version-3-extensions.md)

## <a name="related-topics"></a><span data-ttu-id="584f5-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="584f5-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="584f5-124">Public Key-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="584f5-124">Public Key Infrastructure</span></span>](public-key-infrastructure.md)
</dt> </dl>

 

 

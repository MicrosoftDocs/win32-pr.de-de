---
description: Die Daten in einem Zertifikat, einer Zertifikat Sperr Liste oder einem CTL (Certificate Trust List)-Kontext, einschließlich Erweiterungen, sind schreibgeschützt und können nicht geändert werden.
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: Erweiterte Zertifikat Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29853736433cb143a201ca352fceff0141cc96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131052"
---
# <a name="certificate-extended-properties"></a><span data-ttu-id="3b608-103">Erweiterte Zertifikat Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3b608-103">Certificate Extended Properties</span></span>

<span data-ttu-id="3b608-104">Die Daten in einem [*Zertifikat*](../secgloss/c-gly.md), einer Zertifikat Sperr [*Liste*](../secgloss/c-gly.md) oder einem CTL ( [*Certificate Trust List*](../secgloss/c-gly.md) )- [*Kontext*](../secgloss/c-gly.md), einschließlich Erweiterungen, sind schreibgeschützt und können nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3b608-104">The data in a [*certificate*](../secgloss/c-gly.md), [*certificate revocation list*](../secgloss/c-gly.md) (CRL), or [*certificate trust list*](../secgloss/c-gly.md) (CTL) [*context*](../secgloss/c-gly.md), including any extensions, is read-only and cannot be changed.</span></span> <span data-ttu-id="3b608-105">Auf Microsoft-Plattformen verfügen CryptoAPI-Zertifikate jedoch auch über dynamische erweiterte Eigenschaften, die hinzugefügt und geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="3b608-105">However, on Microsoft platforms, CryptoAPI certificates also have dynamic extended properties that can be added and changed.</span></span>

> [!Note]  
> <span data-ttu-id="3b608-106">Erweiterte Eigenschaften werden einem Zertifikat zugeordnet und sind nicht Teil eines Zertifikats, das von einer Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3b608-106">Extended properties are associated with a certificate and are not part of a certificate as issued by a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span> <span data-ttu-id="3b608-107">Erweiterte Eigenschaften sind für ein Zertifikat nicht verfügbar, wenn es auf einer anderen Plattform als Microsoft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b608-107">Extended properties are not available on a certificate when it is used on a non-Microsoft platform.</span></span>

 

<span data-ttu-id="3b608-108">Zu diesen Eigenschaften zählen folgende Daten:</span><span class="sxs-lookup"><span data-stu-id="3b608-108">These properties include data that:</span></span>

-   <span data-ttu-id="3b608-109">Bezieht sich auf den privaten Schlüssel, der mit dem Zertifikat verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b608-109">Pertains to the private key to be used with the certificate.</span></span>
-   <span data-ttu-id="3b608-110">Gibt den Typ der Hashes an, die für das Zertifikat ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3b608-110">Indicates the type of hashes to be performed on the certificate.</span></span>
-   <span data-ttu-id="3b608-111">Stellt benutzerdefinierte Informationen bereit, die dem Zertifikat zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3b608-111">Provides user-defined information associated with the certificate.</span></span>

<span data-ttu-id="3b608-112">Auf Microsoft-Plattformen werden Werte für diese Eigenschaften angefügt und mit dem Zertifikat verschoben.</span><span class="sxs-lookup"><span data-stu-id="3b608-112">On Microsoft platforms, values for these properties are attached to and move with the certificate.</span></span> <span data-ttu-id="3b608-113">Aktuell vordefinierte Eigenschaften, die mit Eigenschaften-IDs identifiziert werden, enthalten die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3b608-113">Currently predefined properties identified with property IDs include the following properties:</span></span>

-   <span data-ttu-id="3b608-114">Mit diesen Eigenschaften wird ein Zertifikat mit einem bestimmten CSP und innerhalb des CSP mit einem bestimmten privaten Schlüssel verknüpft:</span><span class="sxs-lookup"><span data-stu-id="3b608-114">These properties tie a certificate to a particular CSP and, within that CSP, to a particular private key:</span></span>
    -   <span data-ttu-id="3b608-115">Stamm-ID des CERT \_ Key- \_ Prov- \_ Handles \_ \_</span><span class="sxs-lookup"><span data-stu-id="3b608-115">CERT\_KEY\_PROV\_HANDLE\_PROP\_ID</span></span>
    -   <span data-ttu-id="3b608-116">Zertifikat \_ Schlüssel- \_ Prov- \_ \_ Infoprop- \_ ID</span><span class="sxs-lookup"><span data-stu-id="3b608-116">CERT\_KEY\_PROV\_INFO\_PROP\_ID</span></span>
    -   <span data-ttu-id="3b608-117">CERT \_ Key- \_ Kontext-Prop- \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="3b608-117">CERT\_KEY\_CONTEXT\_PROP\_ID</span></span>
-   <span data-ttu-id="3b608-118">Diese Eigenschaften geben den Hash Algorithmus an, der verwendet werden soll, wenn ein Hash Vorgang durchgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="3b608-118">These properties indicate the hashing algorithm to be used when a hashing operation is performed:</span></span>
    -   <span data-ttu-id="3b608-119">CERT \_ SHA1- \_ Hashwert- \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="3b608-119">CERT\_SHA1\_HASH\_PROP\_ID</span></span>
    -   <span data-ttu-id="3b608-120">Zertifikat- \_ MD5- \_ \_ hashprop- \_ ID</span><span class="sxs-lookup"><span data-stu-id="3b608-120">CERT\_MD5\_HASH\_PROP\_ID</span></span>

<span data-ttu-id="3b608-121">Eine Liste der derzeit definierten erweiterten Zertifikat Eigenschaften und Beschreibungen der Bedeutung und Verwendung der einzelnen Eigenschaften finden Sie unter [**certgetcertifiaseecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) und [**certsetcertifikatecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).</span><span class="sxs-lookup"><span data-stu-id="3b608-121">For complete lists of currently defined extended certificate properties and descriptions of the meaning and use of each property, see [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b608-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3b608-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b608-123">**Certgetcrlcontextproperty**</span><span class="sxs-lookup"><span data-stu-id="3b608-123">**CertGetCRLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)
</dt> <dt>

[<span data-ttu-id="3b608-124">**Certgetctlcontextproperty**</span><span class="sxs-lookup"><span data-stu-id="3b608-124">**CertGetCTLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)
</dt> <dt>

[<span data-ttu-id="3b608-125">**Certsetcrlcontextproperty**</span><span class="sxs-lookup"><span data-stu-id="3b608-125">**CertSetCRLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)
</dt> <dt>

[<span data-ttu-id="3b608-126">**Certsetctlcontextproperty**</span><span class="sxs-lookup"><span data-stu-id="3b608-126">**CertSetCTLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)
</dt> </dl>

 

 

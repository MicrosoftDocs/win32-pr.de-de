---
description: Die folgenden Schnittstellen können zum Erstellen von Zertifikat Attributen verwendet werden.
ms.assetid: 3701f9b2-0857-45f0-b3ed-4f1b3db4d6d8
title: Zertifikat Attribut Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 930f427ae6333084c8a180e5d227e4c24daa5426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368088"
---
# <a name="certificate-attribute-interfaces"></a><span data-ttu-id="d399c-103">Zertifikat Attribut Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d399c-103">Certificate Attribute Interfaces</span></span>

<span data-ttu-id="d399c-104">Die folgenden Schnittstellen können zum Erstellen von Zertifikat Attributen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d399c-104">The following interfaces can be used to create certificate attributes.</span></span>



| <span data-ttu-id="d399c-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d399c-105">Interface</span></span>                                                                    | <span data-ttu-id="d399c-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d399c-106">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d399c-107">**Icryptattribute**</span><span class="sxs-lookup"><span data-stu-id="d399c-107">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                   | <span data-ttu-id="d399c-108">Stellt ein kryptografieattribut in einer Zertifikat Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="d399c-108">Represents a cryptographic attribute in a certificate request.</span></span>                                                                              |
| [<span data-ttu-id="d399c-109">**Icryptattributes**</span><span class="sxs-lookup"><span data-stu-id="d399c-109">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)                                 | <span data-ttu-id="d399c-110">Verwaltet eine Auflistung von [**icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="d399c-110">Manages a collection of [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) objects.</span></span>                                                                 |
| [<span data-ttu-id="d399c-111">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="d399c-111">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                     | <span data-ttu-id="d399c-112">Stellt ein Attribut in einer PKCS \# 7-, PKCS \# 10-oder CMC-Zertifikat Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="d399c-112">Represents an attribute in a PKCS \#7, PKCS \#10, or CMC certificate request.</span></span>                                                               |
| [<span data-ttu-id="d399c-113">**IX509AttributeClientId**</span><span class="sxs-lookup"><span data-stu-id="d399c-113">**IX509AttributeClientId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)                     | <span data-ttu-id="d399c-114">Stellt ein Attribut dar, das verwendet werden kann, um den Client zu identifizieren, von dem eine Zertifikat Anforderung generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d399c-114">Represents an attribute that can be used to identify the client that generated a certificate request.</span></span>                                       |
| [<span data-ttu-id="d399c-115">**IX509AttributeExtensions**</span><span class="sxs-lookup"><span data-stu-id="d399c-115">**IX509AttributeExtensions**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)                 | <span data-ttu-id="d399c-116">Stellt die Zertifikat Erweiterungen in einer Zertifikat Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="d399c-116">Represents the certificate extensions in a certificate request.</span></span>                                                                             |
| [<span data-ttu-id="d399c-117">**IX509AttributeArchiveKey**</span><span class="sxs-lookup"><span data-stu-id="d399c-117">**IX509AttributeArchiveKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)                 | <span data-ttu-id="d399c-118">Stellt ein Attribut dar, das einen verschlüsselten privaten Schlüssel enthält, der von einer Zertifizierungsstelle archiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d399c-118">Represents an attribute that contains an encrypted private key to be archived by a certification authority.</span></span>                                 |
| [<span data-ttu-id="d399c-119">**IX509AttributeArchiveKeyHash**</span><span class="sxs-lookup"><span data-stu-id="d399c-119">**IX509AttributeArchiveKeyHash**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)         | <span data-ttu-id="d399c-120">Stellt ein Attribut dar, das einen SHA-1-Hash des verschlüsselten privaten Schlüssels enthält, der von einer Zertifizierungsstelle archiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d399c-120">Represents an attribute that contains a SHA-1 hash of the encrypted private key to be archived by a certification authority.</span></span>                |
| [<span data-ttu-id="d399c-121">**IX509AttributeCspProvider**</span><span class="sxs-lookup"><span data-stu-id="d399c-121">**IX509AttributeCspProvider**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)               | <span data-ttu-id="d399c-122">Stellt ein Attribut dar, das den Kryptografieanbieter identifiziert, der von der Entität, die das Zertifikat anfordert</span><span class="sxs-lookup"><span data-stu-id="d399c-122">Represents an attribute that identifies the cryptographic provider used by the entity requesting the certificate.</span></span>                           |
| [<span data-ttu-id="d399c-123">**IX509AttributeOSVersion**</span><span class="sxs-lookup"><span data-stu-id="d399c-123">**IX509AttributeOSVersion**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)                   | <span data-ttu-id="d399c-124">Stellt ein Attribut dar, das Versionsinformationen über das Client Betriebssystem enthält, für das die Zertifikat Anforderung generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d399c-124">Represents an attribute that contains version information about the client operating system on which the certificate request was generated.</span></span> |
| [<span data-ttu-id="d399c-125">**IX509AttributeRenewalCertificate**</span><span class="sxs-lookup"><span data-stu-id="d399c-125">**IX509AttributeRenewalCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) | <span data-ttu-id="d399c-126">Stellt ein Attribut dar, das das Zertifikat enthält, das erneuert wird.</span><span class="sxs-lookup"><span data-stu-id="d399c-126">Represents an attribute that contains the certificate being renewed.</span></span>                                                                        |
| [<span data-ttu-id="d399c-127">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="d399c-127">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)                                   | <span data-ttu-id="d399c-128">Verwaltet eine Auflistung von [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="d399c-128">Manages a collection of [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) objects.</span></span>                                                                   |
| [<span data-ttu-id="d399c-129">**IX509NameValuePair**</span><span class="sxs-lookup"><span data-stu-id="d399c-129">**IX509NameValuePair**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                             | <span data-ttu-id="d399c-130">Stellt ein generisches Name-Wert-Paar dar.</span><span class="sxs-lookup"><span data-stu-id="d399c-130">Represents a generic name-value pair.</span></span>                                                                                                       |
| [<span data-ttu-id="d399c-131">**IX509NameValuePairs**</span><span class="sxs-lookup"><span data-stu-id="d399c-131">**IX509NameValuePairs**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)                           | <span data-ttu-id="d399c-132">Verwaltet eine Auflistung von [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="d399c-132">Manages a collection of [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) objects.</span></span>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="d399c-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d399c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d399c-134">CertEnroll-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d399c-134">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 




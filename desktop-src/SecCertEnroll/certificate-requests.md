---
description: Mit dem Zertifikatregistrierungs-SDK können PKCS \# 10-, PKCS \# 7-, CMC-und selbst signierte Zertifikat Anforderungen erstellt werden.
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: Zertifikat Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690f3a5117abfa0ae262f0a8fa38f68528abf02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368133"
---
# <a name="certificate-requests"></a><span data-ttu-id="f0799-103">Zertifikat Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0799-103">Certificate Requests</span></span>

<span data-ttu-id="f0799-104">Mit dem Zertifikatregistrierungs-SDK können PKCS \# 10-, PKCS \# 7-, CMC-und selbst signierte Zertifikat Anforderungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f0799-104">The Certificate Enrollment SDK can be used to create PKCS \#10, PKCS \#7, CMC, and self-signed certificate requests.</span></span> <span data-ttu-id="f0799-105">Jeder Anforderungstyp wird durch eine der in der folgenden Tabelle aufgelisteten Schnittstellen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f0799-105">Each type of request is represented by one of the interfaces listed in the following table.</span></span> <span data-ttu-id="f0799-106">Alle Anforderungs Schnittstellen erben direkt oder indirekt von der [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f0799-106">All request interfaces inherit directly or indirectly from the [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) interface.</span></span> 

| <span data-ttu-id="f0799-107">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f0799-107">Interface</span></span>                                                                        | <span data-ttu-id="f0799-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0799-108">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0799-109">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="f0799-109">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | <span data-ttu-id="f0799-110">Stellt eine PKCS \# 10-Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="f0799-110">Represents a PKCS \#10 request.</span></span> <span data-ttu-id="f0799-111">Diese Schnittstelle erbt von [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span><span class="sxs-lookup"><span data-stu-id="f0799-111">This interface inherits from [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span></span>                   |
| [<span data-ttu-id="f0799-112">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="f0799-112">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | <span data-ttu-id="f0799-113">Stellt eine PKCS \# 7-Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="f0799-113">Represents a PKCS \#7 request.</span></span> <span data-ttu-id="f0799-114">Diese Schnittstelle erbt von [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span><span class="sxs-lookup"><span data-stu-id="f0799-114">This interface inherits from [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span></span>                    |
| [<span data-ttu-id="f0799-115">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="f0799-115">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | <span data-ttu-id="f0799-116">Stellt ein selbst signiertes Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="f0799-116">Represents a self-signed certificate.</span></span> <span data-ttu-id="f0799-117">Diese Schnittstelle erbt von [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10).</span><span class="sxs-lookup"><span data-stu-id="f0799-117">This interface inherits from [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10).</span></span> |
| [<span data-ttu-id="f0799-118">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="f0799-118">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | <span data-ttu-id="f0799-119">Stellt eine CMC-Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="f0799-119">Represents a CMC request.</span></span> <span data-ttu-id="f0799-120">Diese Schnittstelle erbt von [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).</span><span class="sxs-lookup"><span data-stu-id="f0799-120">This interface inherits from [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).</span></span>               |



 

<span data-ttu-id="f0799-121">Die folgende Abbildung zeigt die Vererbungs Struktur der Anforderungs Objekte, die von der Zertifikatregistrierungs-API unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f0799-121">The following illustration shows the inheritance structure of the request objects supported by the Certificate Enrollment API.</span></span> <span data-ttu-id="f0799-122">Ein [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) -Objekt dient direkt oder indirekt als Basisklasse für alle verfügbaren Anforderungs Objekte.</span><span class="sxs-lookup"><span data-stu-id="f0799-122">An [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) object serves, directly or indirectly, as the base class for all of the available request objects.</span></span>

![Vererbungs Struktur für die Anforderungs Schnittstellen](images/certificate-request-inheritance.png)

<span data-ttu-id="f0799-124">Unabhängig vom Typ enthält eine Zertifikat Anforderung Informationen über den Betreff der Anforderung, den öffentlichen Schlüssel des Antragstellers, eine Gruppe von Attributen, eine Reihe von X. 509 Version 3-Erweiterungen (die als Teil der Attribute übermittelt werden können) und eine Signatur.</span><span class="sxs-lookup"><span data-stu-id="f0799-124">Regardless of type, a certificate request contains information about the subject making the request, the subject's public key, a set of attributes, a set of X.509 version 3 extensions (which may be submitted as part of the attributes), and a signature.</span></span> <span data-ttu-id="f0799-125">Diese Probleme werden in den folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="f0799-125">These issues are addressed by the following topics:</span></span>

-   [<span data-ttu-id="f0799-126">Antragstellernamen</span><span class="sxs-lookup"><span data-stu-id="f0799-126">Subject Names</span></span>](subject-names.md)
-   [<span data-ttu-id="f0799-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="f0799-127">Attributes</span></span>](attributes.md)
-   [<span data-ttu-id="f0799-128">Extensions (Erweiterungen)</span><span class="sxs-lookup"><span data-stu-id="f0799-128">Extensions</span></span>](extensions.md)

## <a name="related-topics"></a><span data-ttu-id="f0799-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0799-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0799-130">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="f0799-130">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[<span data-ttu-id="f0799-131">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="f0799-131">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[<span data-ttu-id="f0799-132">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="f0799-132">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[<span data-ttu-id="f0799-133">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="f0799-133">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> </dl>

 

 




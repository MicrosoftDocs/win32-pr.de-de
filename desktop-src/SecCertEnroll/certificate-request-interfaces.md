---
description: Die folgenden Schnittstellen können verwendet werden, um Zertifikat Anforderungen zu erstellen.
ms.assetid: 6021db79-ac90-4e0c-afbd-0f926abcab78
title: Schnittstellen für Zertifikat Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e18a4f8e1ce60348ffdf52afe210247f6d20a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129892"
---
# <a name="certificate-request-interfaces"></a><span data-ttu-id="0dbad-103">Schnittstellen für Zertifikat Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0dbad-103">Certificate Request Interfaces</span></span>

<span data-ttu-id="0dbad-104">Die folgenden Schnittstellen können verwendet werden, um Zertifikat Anforderungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0dbad-104">The following interfaces can be used to create certificate requests.</span></span>



| <span data-ttu-id="0dbad-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0dbad-105">Interface</span></span>                                                                          | <span data-ttu-id="0dbad-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0dbad-106">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0dbad-107">**IX509CertificateRequest**</span><span class="sxs-lookup"><span data-stu-id="0dbad-107">**IX509CertificateRequest**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                         | <span data-ttu-id="0dbad-108">Stellt die abstrakte Oberfläche der obersten Ebene für eine Zertifikat Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="0dbad-108">Represents the abstract top-level interface for a certificate request.</span></span>                                                                                        |
| [<span data-ttu-id="0dbad-109">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="0dbad-109">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)   | <span data-ttu-id="0dbad-110">Ermöglicht das direkte Erstellen von Zertifikaten, ohne eine Registrierung oder Zertifizierungsstelle durchlaufen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="0dbad-110">Enables you to create certificates directly without going through a registration or certification authority.</span></span>                                                  |
| [<span data-ttu-id="0dbad-111">**IX509CertificateRequestCertificate2**</span><span class="sxs-lookup"><span data-stu-id="0dbad-111">**IX509CertificateRequestCertificate2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcertificate2) | <span data-ttu-id="0dbad-112">Erweitert die [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) -Schnittstelle, um die Initialisierung aus einer Vorlage zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0dbad-112">Extends the [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) interface to enable initialization from a template.</span></span>              |
| [<span data-ttu-id="0dbad-113">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="0dbad-113">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                   | <span data-ttu-id="0dbad-114">Stellt eine CMC-Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="0dbad-114">Represents a CMC request.</span></span>                                                                                                                                     |
| [<span data-ttu-id="0dbad-115">**IX509CertificateRequestCmc2**</span><span class="sxs-lookup"><span data-stu-id="0dbad-115">**IX509CertificateRequestCmc2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcmc2)                 | <span data-ttu-id="0dbad-116">Erweitert die [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Schnittstelle, um die Initialisierung aus einer Vorlage zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0dbad-116">Extends the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) interface to enable initialization from a template.</span></span>                              |
| [<span data-ttu-id="0dbad-117">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="0dbad-117">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)             | <span data-ttu-id="0dbad-118">Stellt eine PKCS \# 10-Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="0dbad-118">Represents a PKCS \#10 request.</span></span>                                                                                                                               |
| [<span data-ttu-id="0dbad-119">**IX509CertificateRequestPkcs10V2**</span><span class="sxs-lookup"><span data-stu-id="0dbad-119">**IX509CertificateRequestPkcs10V2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v2)         | <span data-ttu-id="0dbad-120">Erweitert die [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Schnittstelle, um die Initialisierung aus einer Vorlage zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0dbad-120">Extends the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) interface to enable initialization from a template.</span></span>                        |
| [<span data-ttu-id="0dbad-121">**IX509CertificateRequestPkcs10V3**</span><span class="sxs-lookup"><span data-stu-id="0dbad-121">**IX509CertificateRequestPkcs10V3**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)         | <span data-ttu-id="0dbad-122">Erweitert die [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Schnittstelle und fügt Eigenschaften hinzu, die den TPM-Zertifikat Nachweis aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0dbad-122">Extends the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) interface and adds properties that enable TPM certificate attestation.</span></span> |
| [<span data-ttu-id="0dbad-123">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="0dbad-123">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               | <span data-ttu-id="0dbad-124">Stellt eine PKCS \# 7-Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="0dbad-124">Represents a PKCS \#7 request.</span></span>                                                                                                                                |
| [<span data-ttu-id="0dbad-125">**IX509CertificateRequestPkcs7V2**</span><span class="sxs-lookup"><span data-stu-id="0dbad-125">**IX509CertificateRequestPkcs7V2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs7v2)           | <span data-ttu-id="0dbad-126">Erweitert die [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) -Schnittstelle, um die Initialisierung aus einer Vorlage zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0dbad-126">Extends the [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) interface to enable initialization from a template.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="0dbad-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0dbad-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dbad-128">CertEnroll-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0dbad-128">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 




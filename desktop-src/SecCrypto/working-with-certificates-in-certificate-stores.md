---
description: Mehrere Funktionen fügen einen Zertifikat Kontext oder einen Link zu einem Kontext zu einem Store \[ Platform Software Development Kit (SDK) hinzu \] .
ms.assetid: 0355b254-be52-4af4-9567-ee2df092075f
title: Arbeiten mit Zertifikaten in Zertifikat speichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba1ce89c9b9352ef787ed65230b709967125532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347659"
---
# <a name="working-with-certificates-in-certificate-stores"></a><span data-ttu-id="3ed1f-103">Arbeiten mit Zertifikaten in Zertifikat speichern</span><span class="sxs-lookup"><span data-stu-id="3ed1f-103">Working with Certificates in Certificate Stores</span></span>

<span data-ttu-id="3ed1f-104">Mehrere Funktionen fügen einen Zertifikat Kontext oder einen Link zu einem Speicher zu einem Speicher hinzu.</span><span class="sxs-lookup"><span data-stu-id="3ed1f-104">Several functions add a certificate context or a link to a context to a store.</span></span>

<span data-ttu-id="3ed1f-105">Für Zertifikate, die bereits im Zertifikat Kontext Formular vorhanden sind:</span><span class="sxs-lookup"><span data-stu-id="3ed1f-105">For certificates already in certificate context form:</span></span>

-   [<span data-ttu-id="3ed1f-106">**Certaddcertificatcher econtextto Store**</span><span class="sxs-lookup"><span data-stu-id="3ed1f-106">**CertAddCertificateContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
-   [<span data-ttu-id="3ed1f-107">**Certaddcrlcontextflistore**</span><span class="sxs-lookup"><span data-stu-id="3ed1f-107">**CertAddCRLContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)
-   [<span data-ttu-id="3ed1f-108">**Certaddctlcontextto Store**</span><span class="sxs-lookup"><span data-stu-id="3ed1f-108">**CertAddCTLContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)
-   [<span data-ttu-id="3ed1f-109">**Certaddcertifialisielinktostore**</span><span class="sxs-lookup"><span data-stu-id="3ed1f-109">**CertAddCertificateLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)
-   [<span data-ttu-id="3ed1f-110">**Certaddcrllinkto Store**</span><span class="sxs-lookup"><span data-stu-id="3ed1f-110">**CertAddCRLLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)
-   [<span data-ttu-id="3ed1f-111">**Certaddctllinkto Store**</span><span class="sxs-lookup"><span data-stu-id="3ed1f-111">**CertAddCTLLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)

<span data-ttu-id="3ed1f-112">Für Zertifikate, die codierte Formulare, aber keine vollständigen Zertifikat Kontexte sind:</span><span class="sxs-lookup"><span data-stu-id="3ed1f-112">For certificates that are in encoded form but not full certificate contexts:</span></span>

-   [<span data-ttu-id="3ed1f-113">**Bei CertAddEncodedCertificateToStore**</span><span class="sxs-lookup"><span data-stu-id="3ed1f-113">**CertAddEncodedCertificateToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)
-   [<span data-ttu-id="3ed1f-114">**Certaddencodedcrldestore**</span><span class="sxs-lookup"><span data-stu-id="3ed1f-114">**CertAddEncodedCRLToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)
-   [<span data-ttu-id="3ed1f-115">**Certaddencodedctldestore**</span><span class="sxs-lookup"><span data-stu-id="3ed1f-115">**CertAddEncodedCTLToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

<span data-ttu-id="3ed1f-116">Mit den folgenden Funktionen wird ein Zertifikat, eine Zertifikat Sperr Liste oder eine CTL aus einem Speicher gelöscht, indem der Verweis Zähler um 1 dekrementiert wird.</span><span class="sxs-lookup"><span data-stu-id="3ed1f-116">The following functions delete a certificate, CRL, or CTL from a store by decrementing its reference count by one.</span></span> <span data-ttu-id="3ed1f-117">Wenn dies bewirkt, dass der Verweis Zähler Null wird, wird der zum Speichern des Zertifikats, der CRL oder der CTL verwendete Arbeitsspeicher freigegeben.</span><span class="sxs-lookup"><span data-stu-id="3ed1f-117">If this causes the reference count to become zero, the memory used to store the certificate, CRL, or CTL is freed.</span></span>

-   [<span data-ttu-id="3ed1f-118">**Certdeletecertifipeefromstore**</span><span class="sxs-lookup"><span data-stu-id="3ed1f-118">**CertDeleteCertificateFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)
-   [<span data-ttu-id="3ed1f-119">**Certdeletecrlfromstore**</span><span class="sxs-lookup"><span data-stu-id="3ed1f-119">**CertDeleteCRLFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)
-   [<span data-ttu-id="3ed1f-120">**Certdeletectlfromstore**</span><span class="sxs-lookup"><span data-stu-id="3ed1f-120">**CertDeleteCTLFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)

 

 




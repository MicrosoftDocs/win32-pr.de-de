---
description: Eine Windows-Public Key-Infrastruktur (PKI) speichert Zertifikate auf dem Server, auf dem die Zertifizierungsstelle (Certification Authority, ca) und auf dem lokalen Computer oder Gerät gehostet werden.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Zertifikatsverzeichnis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee525e4d910de1c75516c6aaa27ca41a6cfa17c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218666"
---
# <a name="certificate-directory"></a><span data-ttu-id="e0ae4-103">Zertifikatsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="e0ae4-103">Certificate Directory</span></span>

<span data-ttu-id="e0ae4-104">Eine Windows-Public Key-Infrastruktur (PKI) speichert Zertifikate auf dem Server, auf dem die Zertifizierungsstelle (Certification Authority, ca) und auf dem lokalen Computer oder Gerät gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-104">A Windows public key infrastructure (PKI) saves certificates on the server that hosts the certification authority (CA) and on the local computer or device.</span></span> <span data-ttu-id="e0ae4-105">Der ca-Speicher wird in der Regel als Zertifikat Datenbank bezeichnet, und der lokale Speicher wird als Zertifikat Speicher bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-105">CA storage is typically referred to as the certificate database, and local storage is known as the certificate store.</span></span>

## <a name="certificate-database"></a><span data-ttu-id="e0ae4-106">Zertifikat Datenbank</span><span class="sxs-lookup"><span data-stu-id="e0ae4-106">Certificate Database</span></span>

<span data-ttu-id="e0ae4-107">Wenn Sie Zertifikat Dienste auf einem Windows-Server hinzufügen und eine Zertifizierungsstelle konfigurieren, wird eine Zertifikat Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-107">When you add Certificate Services on a Windows server and configure a CA, a certificate database is created.</span></span> <span data-ttu-id="e0ae4-108">Standardmäßig ist die Datenbank im Ordner *% systemroot%* \\ system32 \\ certlog enthalten, und der Name basiert auf dem Namen der Zertifizierungsstelle mit der Erweiterung EDB.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-108">By default, the database is contained in the *%SystemRoot%*\\System32\\Certlog folder, and the name is based on the CA name with an .edb extension.</span></span> <span data-ttu-id="e0ae4-109">Die Datenbank kann Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="e0ae4-109">The database can contain:</span></span>

-   <span data-ttu-id="e0ae4-110">Ausgestellte Zertifikate</span><span class="sxs-lookup"><span data-stu-id="e0ae4-110">Issued certificates</span></span>
-   <span data-ttu-id="e0ae4-111">Gesperrte Zertifikate</span><span class="sxs-lookup"><span data-stu-id="e0ae4-111">Revoked certificates</span></span>
-   <span data-ttu-id="e0ae4-112">Archivierte private Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e0ae4-112">Archived private keys</span></span>
-   <span data-ttu-id="e0ae4-113">Zertifikat Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0ae4-113">Certificate requests</span></span>

<span data-ttu-id="e0ae4-114">Die Zertifikat Registrierungs-API kann nicht zum Bearbeiten der Datenbank verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-114">You cannot use the Certificate Enrollment API to manipulate the database.</span></span> <span data-ttu-id="e0ae4-115">Beim Registrierungsprozess werden automatisch die erforderlichen Einträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-115">The enrollment process automatically creates the necessary entries.</span></span>

## <a name="certificate-stores"></a><span data-ttu-id="e0ae4-116">Zertifikatspeicher</span><span class="sxs-lookup"><span data-stu-id="e0ae4-116">Certificate Stores</span></span>

<span data-ttu-id="e0ae4-117">Die Microsoft-Zertifikat Dienste kopieren ausgestellte Zertifikate und ausstehende oder abgelehnte Anforderungen auf lokale Computer und Geräte.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-117">Microsoft Certificate Services copies issued certificates and pending or rejected requests to local computers and devices.</span></span> <span data-ttu-id="e0ae4-118">Der Speicherort wird als Zertifikat Speicher bezeichnet und besteht aus den folgenden logischen Speichern.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-118">The storage location is called the certificate store and consists of the following logical stores.</span></span>

| <span data-ttu-id="e0ae4-119">Logischer Speicher</span><span class="sxs-lookup"><span data-stu-id="e0ae4-119">Logical store</span></span>                                         | <span data-ttu-id="e0ae4-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0ae4-120">Description</span></span>                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ae4-121">Persönlich</span><span class="sxs-lookup"><span data-stu-id="e0ae4-121">Personal</span></span><br/>                                   | <span data-ttu-id="e0ae4-122">Enthält Zertifikate, die einem privaten Schlüssel zugeordnet sind, der vom Benutzer oder Computer gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-122">Contains certificates associated with a private key controlled by the user or computer.</span></span><br/>                     |
| <span data-ttu-id="e0ae4-123">Trusted Root Certification Authorities</span><span class="sxs-lookup"><span data-stu-id="e0ae4-123">Trusted Root Certification Authorities</span></span><br/>     | <span data-ttu-id="e0ae4-124">Enthält Zertifikate von implizit vertrauenswürdigen Zertifizierungsstellen (CAS).</span><span class="sxs-lookup"><span data-stu-id="e0ae4-124">Contains certificates from implicitly trusted certification authorities (CAs).</span></span><br/>                              |
| <span data-ttu-id="e0ae4-125">Organisationsvertrauen</span><span class="sxs-lookup"><span data-stu-id="e0ae4-125">Enterprise Trust</span></span><br/>                           | <span data-ttu-id="e0ae4-126">Enthält Zertifikat Vertrauens Listen, die normalerweise verwendet werden, um selbst signierte Zertifikate von anderen Organisationen zu vertrauen.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-126">Contains certificate trust lists typically used to trust self-signed certificates from other organizations.</span></span><br/> |
| <span data-ttu-id="e0ae4-127">Zwischenzertifizierungsstellen</span><span class="sxs-lookup"><span data-stu-id="e0ae4-127">Intermediate Certification Authorities</span></span><br/>     | <span data-ttu-id="e0ae4-128">Enthält Zertifikate, die für in der ZS-Hierarchie untergeordnete Zertifizierungsstellen ausgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-128">Contains certificates issued to subordinate CAs in the certification hierarchy.</span></span><br/>                             |
| <span data-ttu-id="e0ae4-129">Active Directory-Benutzerobjekt</span><span class="sxs-lookup"><span data-stu-id="e0ae4-129">Active Directory User Object</span></span><br/>               | <span data-ttu-id="e0ae4-130">Enthält das Benutzerobjekt Zertifikat oder die Zertifikate, die in Active Directory veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-130">Contains the user object certificate or certificates published in Active Directory.</span></span><br/>                         |
| <span data-ttu-id="e0ae4-131">Vertrauenswürdige Herausgeber</span><span class="sxs-lookup"><span data-stu-id="e0ae4-131">Trusted Publishers</span></span><br/>                         | <span data-ttu-id="e0ae4-132">Enthält Zertifikate von vertrauenswürdigen Zertifizierungsstellen.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-132">Contains certificates from trusted CAs.</span></span><br/>                                                                     |
| <span data-ttu-id="e0ae4-133">Nicht vertrauenswürdige Zertifikate</span><span class="sxs-lookup"><span data-stu-id="e0ae4-133">Untrusted Certificates</span></span><br/>                     | <span data-ttu-id="e0ae4-134">Enthält Zertifikate, die explizit als nicht vertrauenswürdig identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-134">Contains certificates that have been explicitly identified as untrusted.</span></span><br/>                                    |
| <span data-ttu-id="e0ae4-135">Stammzertifizierungsstellen von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="e0ae4-135">Third-Party Root Certification Authorities</span></span><br/> | <span data-ttu-id="e0ae4-136">Enthält vertrauenswürdige Stamm Zertifikate von CAS außerhalb der internen Zertifikat Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-136">Contains trusted root certificates from CAs outside the internal certificate hierarchy.</span></span><br/>                     |
| <span data-ttu-id="e0ae4-137">Vertrauenswürdige Personen</span><span class="sxs-lookup"><span data-stu-id="e0ae4-137">Trusted People</span></span><br/>                             | <span data-ttu-id="e0ae4-138">Enthält Zertifikate, die für Benutzer oder Entitäten ausgestellt werden, die explizit vertrauenswürdig sind.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-138">Contains certificates issued to users or entities that have been explicitly trusted.</span></span><br/>                        |
| <span data-ttu-id="e0ae4-139">Andere Personen</span><span class="sxs-lookup"><span data-stu-id="e0ae4-139">Other People</span></span><br/>                               | <span data-ttu-id="e0ae4-140">Enthält Zertifikate, die für Benutzer oder Entitäten ausgestellt wurden, die implizit vertrauenswürdig sind.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-140">Contains certificates issued to users or entities that have been implicitly trusted.</span></span><br/>                        |
| <span data-ttu-id="e0ae4-141">Zertifikatregistrierungsanforderungen</span><span class="sxs-lookup"><span data-stu-id="e0ae4-141">Certificate Enrollment Requests</span></span><br/>            | <span data-ttu-id="e0ae4-142">Enthält ausstehende oder abgelehnte Zertifikat Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-142">Contains pending or rejected certificate requests.</span></span><br/>                                                          |



 

<span data-ttu-id="e0ae4-143">Die Zertifikatregistrierungs-API kann nicht zum angeben oder Abrufen von Speicher Eigenschaften oder zum Kopieren von Zertifikaten in bestimmte Speicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0ae4-143">You cannot use the Certificate Enrollment API to specify or retrieve store properties or copy certificates to specific stores.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0ae4-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0ae4-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0ae4-145">PKI-Elemente</span><span class="sxs-lookup"><span data-stu-id="e0ae4-145">PKI Elements</span></span>](about-pki-components.md)
</dt> </dl>

 

 





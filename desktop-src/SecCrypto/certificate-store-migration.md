---
description: Während eines Computer Upgrades oder einer Computer-zu-Computer-Migration werden die Zertifikate in bestimmten Zertifikat speichern migriert.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Zertifikat Speicher Migration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31b42b83718aa1cab786ad79cc2df754b8fd9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050273"
---
# <a name="certificate-store-migration"></a><span data-ttu-id="42ca5-103">Zertifikat Speicher Migration</span><span class="sxs-lookup"><span data-stu-id="42ca5-103">Certificate Store Migration</span></span>

<span data-ttu-id="42ca5-104">Während eines Computer Upgrades oder einer Computer-zu-Computer-Migration werden die Zertifikate in bestimmten Zertifikat speichern migriert.</span><span class="sxs-lookup"><span data-stu-id="42ca5-104">During a computer upgrade or a computer-to-computer migration, the certificates in certain certificate stores will be migrated.</span></span> <span data-ttu-id="42ca5-105">In der folgenden Tabelle sind die Zertifikat Speicher aufgelistet, die standardmäßig migriert werden.</span><span class="sxs-lookup"><span data-stu-id="42ca5-105">The following table lists the certificate stores that are migrated by default.</span></span> <span data-ttu-id="42ca5-106">Für den automatischen Speicher der Zertifikat Anforderungs Einstellungen (ACRS) werden nur die [*Zertifikat Vertrauens Listen*](../secgloss/c-gly.md) (CTLs) migriert.</span><span class="sxs-lookup"><span data-stu-id="42ca5-106">For the system Automatic Certificate Request Settings (ACRS) store, only the [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) are migrated.</span></span> <span data-ttu-id="42ca5-107">Für alle anderen unten aufgeführten Geschäfte werden nur die Zertifikate migriert.</span><span class="sxs-lookup"><span data-stu-id="42ca5-107">For all other stores listed below, only the certificates are migrated.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="42ca5-108">System/Benutzer</span><span class="sxs-lookup"><span data-stu-id="42ca5-108">System/user</span></span></th>
<th><span data-ttu-id="42ca5-109">Speicher</span><span class="sxs-lookup"><span data-stu-id="42ca5-109">Store</span></span></th>
<th><span data-ttu-id="42ca5-110">Speicherort</span><span class="sxs-lookup"><span data-stu-id="42ca5-110">Storage location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42ca5-111">$ {ROWSPAN8} $System $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="42ca5-111">${ROWSPAN8}$System${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="42ca5-112">ROOT</span><span class="sxs-lookup"><span data-stu-id="42ca5-112">ROOT</span></span></td>
<td><span data-ttu-id="42ca5-113"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong></strong> Stamm \ <strong>Zertifikate</strong></span><span class="sxs-lookup"><span data-stu-id="42ca5-113"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Root</strong>\<strong>Certificates</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42ca5-114">MY</span><span class="sxs-lookup"><span data-stu-id="42ca5-114">MY</span></span></td>
<td><span data-ttu-id="42ca5-115"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong>Meine</strong> \ <strong>Zertifikate</strong></span><span class="sxs-lookup"><span data-stu-id="42ca5-115"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>My</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="42ca5-116">ANFORDERUNG</span><span class="sxs-lookup"><span data-stu-id="42ca5-116">REQUEST</span></span></td>
<td><span data-ttu-id="42ca5-117"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong>Anforderung</strong> \ <strong>Zertifikate</strong></span><span class="sxs-lookup"><span data-stu-id="42ca5-117"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Request</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="42ca5-118">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="42ca5-118">TrustedPublisher</span></span></td>
<td><span data-ttu-id="42ca5-119"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong>Treuhänder Publisher</strong> \ <strong>Zertifikate</strong></span><span class="sxs-lookup"><span data-stu-id="42ca5-119"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPublisher</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="42ca5-120">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="42ca5-120">TrustedPeople</span></span></td>
<td><span data-ttu-id="42ca5-121"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong>Treuhänder</strong> \ <strong>Zertifikate</strong></span><span class="sxs-lookup"><span data-stu-id="42ca5-121"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPeople</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="42ca5-122">Unzulässig</span><span class="sxs-lookup"><span data-stu-id="42ca5-122">Disallowed</span></span></td>
<td><span data-ttu-id="42ca5-123"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ Nicht <strong>zulässig</strong> \ <strong>Zertifikate</strong></span><span class="sxs-lookup"><span data-stu-id="42ca5-123"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Disallowed</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="42ca5-124">CA</span><span class="sxs-lookup"><span data-stu-id="42ca5-124">CA</span></span></td>
<td><span data-ttu-id="42ca5-125"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ Zertifizierungsstelle <strong></strong> \ <strong>Zertifikate</strong></span><span class="sxs-lookup"><span data-stu-id="42ca5-125"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>CA</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="42ca5-126">ACRS</span><span class="sxs-lookup"><span data-stu-id="42ca5-126">ACRS</span></span></td>
<td><span data-ttu-id="42ca5-127"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong>ACRS</strong> \ <strong>CTLs</strong></span><span class="sxs-lookup"><span data-stu-id="42ca5-127"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>ACRS</strong>\<strong>CTLs</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td rowspan="7"><span data-ttu-id="42ca5-128">Benutzer $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="42ca5-128">User${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="42ca5-129">ROOT</span><span class="sxs-lookup"><span data-stu-id="42ca5-129">ROOT</span></span></td>
<td><span data-ttu-id="42ca5-130"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong></strong> Stamm \ <strong>Zertifikate</strong></span><span class="sxs-lookup"><span data-stu-id="42ca5-130"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Root</strong>\<strong>Certificates</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42ca5-131">MY</span><span class="sxs-lookup"><span data-stu-id="42ca5-131">MY</span></span></td>
<td><span data-ttu-id="42ca5-132">Datei: \\ %AppData%\microsoft\systemcertifieres\my\zertifikate</span><span class="sxs-lookup"><span data-stu-id="42ca5-132">file:\\%APPDATA%\Microsoft\SystemCertificates\My\Certificates</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="42ca5-133">ANFORDERUNG</span><span class="sxs-lookup"><span data-stu-id="42ca5-133">REQUEST</span></span></td>
<td><span data-ttu-id="42ca5-134">Datei: \\ %AppData%\microsoft\systemcertifieres\request\zertifikate</span><span class="sxs-lookup"><span data-stu-id="42ca5-134">file:\\%APPDATA%\Microsoft\SystemCertificates\Request\Certificates</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="42ca5-135">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="42ca5-135">TrustedPublisher</span></span></td>
<td><span data-ttu-id="42ca5-136"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong>Treuhänder Publisher</strong> \ <strong>Zertifikate</strong></span><span class="sxs-lookup"><span data-stu-id="42ca5-136"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPublisher</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="42ca5-137">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="42ca5-137">TrustedPeople</span></span></td>
<td><span data-ttu-id="42ca5-138"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong>Treuhänder</strong> \ <strong>Zertifikate</strong></span><span class="sxs-lookup"><span data-stu-id="42ca5-138"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPeople</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="42ca5-139">Unzulässig</span><span class="sxs-lookup"><span data-stu-id="42ca5-139">Disallowed</span></span></td>
<td><span data-ttu-id="42ca5-140"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ Nicht <strong>zulässig</strong> \ <strong>Zertifikate</strong></span><span class="sxs-lookup"><span data-stu-id="42ca5-140"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Disallowed</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="42ca5-141">CA</span><span class="sxs-lookup"><span data-stu-id="42ca5-141">CA</span></span></td>
<td><span data-ttu-id="42ca5-142"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ Zertifizierungsstelle <strong></strong> \ <strong>Zertifikate</strong></span><span class="sxs-lookup"><span data-stu-id="42ca5-142"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>CA</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="42ca5-143">Andere von Anwendungen erstellte Zertifikat Speicher werden standardmäßig nicht migriert.</span><span class="sxs-lookup"><span data-stu-id="42ca5-143">Other certificate stores created by applications are not migrated by default.</span></span> <span data-ttu-id="42ca5-144">Anwendungen, die ihre eigenen Speicher erstellen, sind für die Migration der von Ihnen erstellten Filialen verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="42ca5-144">Applications that create their own stores are responsible for migration of the stores that they create.</span></span> <span data-ttu-id="42ca5-145">Zum Erstellen von Stores empfiehlt es sich, einen Registrierungsschlüssel in den Anwendungseinstellungen zu definieren und in den Registrierungs Einstellungen einen Speicher zu erstellen, indem Sie den Speicher Anbieter für den **Zertifikat \_ Speicher \_ Prov \_ reg** verwenden.</span><span class="sxs-lookup"><span data-stu-id="42ca5-145">To create stores, we recommend that you define a registry key in the application settings and create a store within the registry settings by using the **CERT\_STORE\_PROV\_REG** store provider.</span></span> <span data-ttu-id="42ca5-146">Weitere Informationen zum Migrieren von Anwendungseinstellungen finden Sie im Thema *Erstellen einer benutzerdefinierten XML-Datei* im Leitfaden *using US MT 3,0* unter [Migrationstool für den Benutzerstatus 3,0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx).</span><span class="sxs-lookup"><span data-stu-id="42ca5-146">For more information about migrating application settings, see the *How To Create a Custom .xml File* topic in the *Using USMT 3.0* guide at [User State Migration Tool 3.0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx).</span></span> <span data-ttu-id="42ca5-147">(Diese Ressource ist möglicherweise in einigen Sprachen und Ländern oder Regionen nicht verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="42ca5-147">(This resource may not be available in some languages and countries or regions.)</span></span>

 

 

---
description: Bei einem Systemspeicher handelt es sich um eine Sammlung, die aus einem oder mehreren physischen gleich geordneten speichern besteht.
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: System Speicherorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0863ffde8be5db67459908b1ec26ec73da029744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959867"
---
# <a name="system-store-locations"></a><span data-ttu-id="95891-103">System Speicherorte</span><span class="sxs-lookup"><span data-stu-id="95891-103">System Store Locations</span></span>

<span data-ttu-id="95891-104">Bei einem Systemspeicher handelt es sich um eine Sammlung, die aus einem oder mehreren physischen gleich geordneten speichern besteht.</span><span class="sxs-lookup"><span data-stu-id="95891-104">A system store is a collection that consists of one or more physical sibling stores.</span></span> <span data-ttu-id="95891-105">Für jeden Systemspeicher sind vordefinierte physische neben geordnete Speicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="95891-105">For each system store, there are predefined physical sibling stores.</span></span> <span data-ttu-id="95891-106">Nachdem Sie einen Systemspeicher geöffnet haben, z. b. "My at \_ System \_ Store \_ Current \_ User", ruft der Speicher Anbieter " [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) " auf, um jeden physischen Speicher in der Sammlung "Systemspeicher" zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="95891-106">After opening a system store such as MY at CERT\_SYSTEM\_STORE\_CURRENT\_USER, the store provider calls [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) to open each of the physical stores in the system store collection.</span></span> <span data-ttu-id="95891-107">Im geöffneten Prozess wird jeder dieser physischen Speicher mithilfe von [**certaddstoretocollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection)der Systemspeicher Sammlung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="95891-107">In the open process, each of these physical stores is added to the system store collection using [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).</span></span> <span data-ttu-id="95891-108">Alle Zertifikate in diesen physischen Speichern sind über die Sammlung logischer Systemspeicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="95891-108">All certificates in those physical stores are available through the logical system store collection.</span></span>

<span data-ttu-id="95891-109">Die vordefinierten Systemspeicher Orte für jeden System Speicherort sind:</span><span class="sxs-lookup"><span data-stu-id="95891-109">For each system store location, the predefined systems stores are:</span></span>

-   <span data-ttu-id="95891-110">MY</span><span class="sxs-lookup"><span data-stu-id="95891-110">MY</span></span>
-   <span data-ttu-id="95891-111">Root</span><span class="sxs-lookup"><span data-stu-id="95891-111">Root</span></span>
-   <span data-ttu-id="95891-112">Vertrauensstellung</span><span class="sxs-lookup"><span data-stu-id="95891-112">Trust</span></span>
-   <span data-ttu-id="95891-113">CA</span><span class="sxs-lookup"><span data-stu-id="95891-113">CA</span></span>

<span data-ttu-id="95891-114">In CERT \_ System \_ Store \_ aktueller \_ Benutzer gibt es auch einen vordefinierten userds-Speicher.</span><span class="sxs-lookup"><span data-stu-id="95891-114">In CERT\_SYSTEM\_STORE\_CURRENT\_USER, there is also a predefined UserDS store.</span></span> <span data-ttu-id="95891-115">Für diesen Standort ist ein smartcardspeicher geplant.</span><span class="sxs-lookup"><span data-stu-id="95891-115">A smart card store is planned for this location.</span></span>

<span data-ttu-id="95891-116">Im folgenden finden Sie die Systemspeicher, auf die weitere Hinweise folgt:</span><span class="sxs-lookup"><span data-stu-id="95891-116">Here are the system stores followed by further remarks:</span></span>

-   [<span data-ttu-id="95891-117">Zertifikat \_ System \_ Speicher \_ aktueller \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="95891-117">CERT\_SYSTEM\_STORE\_CURRENT\_USER</span></span>](#cert_system_store_current_user)
-   [<span data-ttu-id="95891-118">\_lokaler Zertifikat System \_ Speicher- \_ \_ Computer</span><span class="sxs-lookup"><span data-stu-id="95891-118">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>](#cert_system_store_local_machine)
-   [<span data-ttu-id="95891-119">\_ \_ \_ Aktueller Dienst des Zertifikat System Stores \_</span><span class="sxs-lookup"><span data-stu-id="95891-119">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE</span></span>](#cert_system_store_current_service)
-   [<span data-ttu-id="95891-120">Zertifikat- \_ System \_ Speicher \_ Dienste</span><span class="sxs-lookup"><span data-stu-id="95891-120">CERT\_SYSTEM\_STORE\_SERVICES</span></span>](#cert_system_store_services)
-   [<span data-ttu-id="95891-121">Zertifikat \_ System \_ Speicher- \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="95891-121">CERT\_SYSTEM\_STORE\_USERS</span></span>](#cert_system_store_users)
-   [<span data-ttu-id="95891-122">\_ \_ \_ Richtlinie zur aktuellen \_ Benutzer \_ Gruppe des Zertifikat Systems</span><span class="sxs-lookup"><span data-stu-id="95891-122">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY</span></span>](#cert_system_current_user_group_policy)
-   [<span data-ttu-id="95891-123">\_ \_ \_ \_ Gruppen \_ Richtlinie für den lokalen Zertifikat System Computer</span><span class="sxs-lookup"><span data-stu-id="95891-123">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>](#cert_system_local_machine_group_policy)
-   [<span data-ttu-id="95891-124">\_Enterprise-Zertifikat System \_ Speicher \_ lokaler \_ Computer \_</span><span class="sxs-lookup"><span data-stu-id="95891-124">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE</span></span>](#cert_system_store_local_machine_enterprise)
-   [<span data-ttu-id="95891-125">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="95891-125">Remarks</span></span>](#remarks)

### <a name="cert_system_store_current_user"></a><span data-ttu-id="95891-126">Zertifikat \_ System \_ Speicher \_ aktueller \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="95891-126">CERT\_SYSTEM\_STORE\_CURRENT\_USER</span></span>

<span data-ttu-id="95891-127">\_ \_ Systemspeicher für Systemspeicher im Zertifikat Systemspeicher \_ \_ befinden sich am folgenden Registrierungs Speicherort:</span><span class="sxs-lookup"><span data-stu-id="95891-127">CERT\_SYSTEM\_STORE\_CURRENT\_USER system stores are at the following registry location:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

<span data-ttu-id="95891-128">Die diesem Systemspeicher zugeordneten vordefinierten physischen Speicher lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="95891-128">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="95891-129">System Speicher</span><span class="sxs-lookup"><span data-stu-id="95891-129">System store</span></span> | <span data-ttu-id="95891-130">Physischer Speicher</span><span class="sxs-lookup"><span data-stu-id="95891-130">Physical store</span></span>                                           |
|--------------|----------------------------------------------------------|
| <span data-ttu-id="95891-131">MY</span><span class="sxs-lookup"><span data-stu-id="95891-131">MY</span></span>           | <span data-ttu-id="95891-132">. Vorgegebene</span><span class="sxs-lookup"><span data-stu-id="95891-132">.Default</span></span>                                                 |
| <span data-ttu-id="95891-133">Root</span><span class="sxs-lookup"><span data-stu-id="95891-133">Root</span></span>         | <span data-ttu-id="95891-134">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="95891-134">.Default.LocalMachine</span></span><br/> <span data-ttu-id="95891-135">. Smartcard</span><span class="sxs-lookup"><span data-stu-id="95891-135">.SmartCard</span></span><br/>   |
| <span data-ttu-id="95891-136">Vertrauensstellung</span><span class="sxs-lookup"><span data-stu-id="95891-136">Trust</span></span>        | <span data-ttu-id="95891-137">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="95891-137">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="95891-138">. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="95891-138">.LocalMachine</span></span><br/> |
| <span data-ttu-id="95891-139">CA</span><span class="sxs-lookup"><span data-stu-id="95891-139">CA</span></span>           | <span data-ttu-id="95891-140">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="95891-140">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="95891-141">. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="95891-141">.LocalMachine</span></span><br/> |
| <span data-ttu-id="95891-142">Userds</span><span class="sxs-lookup"><span data-stu-id="95891-142">UserDS</span></span>       | <span data-ttu-id="95891-143">. UserCertificate</span><span class="sxs-lookup"><span data-stu-id="95891-143">.UserCertificate</span></span>                                         |



 

### <a name="cert_system_store_local_machine"></a><span data-ttu-id="95891-144">\_lokaler Zertifikat System \_ Speicher- \_ \_ Computer</span><span class="sxs-lookup"><span data-stu-id="95891-144">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>

<span data-ttu-id="95891-145">\_ \_ \_ Systemspeicher des lokalen Zertifikat System Speichers \_ befinden sich am folgenden Registrierungs Speicherort:</span><span class="sxs-lookup"><span data-stu-id="95891-145">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

<span data-ttu-id="95891-146">Die vordefinierten physischen Speicher sind diesen System speichern folgendermaßen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="95891-146">The predefined physical stores are associated with those system stores are as follows.</span></span>



| <span data-ttu-id="95891-147">System Speicher</span><span class="sxs-lookup"><span data-stu-id="95891-147">System store</span></span> | <span data-ttu-id="95891-148">Physischer Speicher</span><span class="sxs-lookup"><span data-stu-id="95891-148">Physical store</span></span>                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95891-149">MY</span><span class="sxs-lookup"><span data-stu-id="95891-149">MY</span></span>           | <span data-ttu-id="95891-150">. Vorgegebene</span><span class="sxs-lookup"><span data-stu-id="95891-150">.Default</span></span>                                                                                          |
| <span data-ttu-id="95891-151">Root</span><span class="sxs-lookup"><span data-stu-id="95891-151">Root</span></span>         | <span data-ttu-id="95891-152">. Default. AuthRoot</span><span class="sxs-lookup"><span data-stu-id="95891-152">.Default.AuthRoot</span></span><br/> <span data-ttu-id="95891-153">. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="95891-153">.GroupPolicy</span></span><br/> <span data-ttu-id="95891-154">. Fangen</span><span class="sxs-lookup"><span data-stu-id="95891-154">.Enterprise</span></span><br/> <span data-ttu-id="95891-155">. Smartcard</span><span class="sxs-lookup"><span data-stu-id="95891-155">.SmartCard</span></span><br/> |
| <span data-ttu-id="95891-156">Vertrauensstellung</span><span class="sxs-lookup"><span data-stu-id="95891-156">Trust</span></span>        | <span data-ttu-id="95891-157">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="95891-157">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="95891-158">. Fangen</span><span class="sxs-lookup"><span data-stu-id="95891-158">.Enterprise</span></span><br/>                                            |
| <span data-ttu-id="95891-159">CA</span><span class="sxs-lookup"><span data-stu-id="95891-159">CA</span></span>           | <span data-ttu-id="95891-160">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="95891-160">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="95891-161">. Fangen</span><span class="sxs-lookup"><span data-stu-id="95891-161">.Enterprise</span></span> <br/>                                           |



 

### <a name="cert_system_store_current_service"></a><span data-ttu-id="95891-162">\_ \_ \_ Aktueller Dienst des Zertifikat System Stores \_</span><span class="sxs-lookup"><span data-stu-id="95891-162">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE</span></span>

<span data-ttu-id="95891-163">\_ \_ \_ \_ Die aktuellen Dienst System Speicher des Zertifikat System Speichers befinden sich am folgenden Registrierungs Speicherort:</span><span class="sxs-lookup"><span data-stu-id="95891-163">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

<span data-ttu-id="95891-164">Die diesem Systemspeicher zugeordneten vordefinierten physischen Speicher lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="95891-164">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="95891-165">System Speicher</span><span class="sxs-lookup"><span data-stu-id="95891-165">System store</span></span> | <span data-ttu-id="95891-166">Physischer Speicher</span><span class="sxs-lookup"><span data-stu-id="95891-166">Physical store</span></span>                   |
|--------------|----------------------------------|
| <span data-ttu-id="95891-167">MY</span><span class="sxs-lookup"><span data-stu-id="95891-167">MY</span></span>           | <span data-ttu-id="95891-168">. Vorgegebene</span><span class="sxs-lookup"><span data-stu-id="95891-168">.Default</span></span>                         |
| <span data-ttu-id="95891-169">Root</span><span class="sxs-lookup"><span data-stu-id="95891-169">Root</span></span>         | <span data-ttu-id="95891-170">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="95891-170">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="95891-171">Vertrauensstellung</span><span class="sxs-lookup"><span data-stu-id="95891-171">Trust</span></span>        | <span data-ttu-id="95891-172">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="95891-172">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="95891-173">CA</span><span class="sxs-lookup"><span data-stu-id="95891-173">CA</span></span>           | <span data-ttu-id="95891-174">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="95891-174">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_store_services"></a><span data-ttu-id="95891-175">Zertifikat- \_ System \_ Speicher \_ Dienste</span><span class="sxs-lookup"><span data-stu-id="95891-175">CERT\_SYSTEM\_STORE\_SERVICES</span></span>

<span data-ttu-id="95891-176">Systemspeicher für Zertifikat \_ System \_ Speicher \_ Dienste befinden sich am folgenden Registrierungs Speicherort:</span><span class="sxs-lookup"><span data-stu-id="95891-176">CERT\_SYSTEM\_STORE\_SERVICES system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

<span data-ttu-id="95891-177">Die diesem Systemspeicher zugeordneten vordefinierten physischen Speicher lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="95891-177">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="95891-178">System Speicher</span><span class="sxs-lookup"><span data-stu-id="95891-178">System store</span></span>       | <span data-ttu-id="95891-179">Physischer Speicher</span><span class="sxs-lookup"><span data-stu-id="95891-179">Physical store</span></span>                   |
|--------------------|----------------------------------|
| <span data-ttu-id="95891-180">Dienst Name \\ My</span><span class="sxs-lookup"><span data-stu-id="95891-180">ServiceName\\MY</span></span>    | <span data-ttu-id="95891-181">. Vorgegebene</span><span class="sxs-lookup"><span data-stu-id="95891-181">.Default</span></span>                         |
| <span data-ttu-id="95891-182">Dienst \\ Name Stamm</span><span class="sxs-lookup"><span data-stu-id="95891-182">ServiceName\\Root</span></span>  | <span data-ttu-id="95891-183">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="95891-183">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="95891-184">ServiceName- \\ Vertrauensstellung</span><span class="sxs-lookup"><span data-stu-id="95891-184">ServiceName\\Trust</span></span> | <span data-ttu-id="95891-185">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="95891-185">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="95891-186">Dienst Name ( \\ ca)</span><span class="sxs-lookup"><span data-stu-id="95891-186">ServiceName\\CA</span></span>    | <span data-ttu-id="95891-187">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="95891-187">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_store_users"></a><span data-ttu-id="95891-188">Zertifikat \_ System \_ Speicher- \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="95891-188">CERT\_SYSTEM\_STORE\_USERS</span></span>

<span data-ttu-id="95891-189">\_Systemspeicher für Zertifikat System \_ Speicher- \_ Benutzer befinden sich am folgenden Registrierungs Speicherort:</span><span class="sxs-lookup"><span data-stu-id="95891-189">CERT\_SYSTEM\_STORE\_USERS system stores are at the following registry location:</span></span>

```
HKEY_USERS
   UserName
      Software
         Microsoft
            SystemCertificates
```

<span data-ttu-id="95891-190">Die diesem Systemspeicher zugeordneten vordefinierten physischen Speicher lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="95891-190">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="95891-191">System Speicher</span><span class="sxs-lookup"><span data-stu-id="95891-191">System store</span></span>  | <span data-ttu-id="95891-192">Physischer Speicher</span><span class="sxs-lookup"><span data-stu-id="95891-192">Physical store</span></span>                   |
|---------------|----------------------------------|
| <span data-ttu-id="95891-193">Benutzer-ID \\ My</span><span class="sxs-lookup"><span data-stu-id="95891-193">userid\\MY</span></span>    | <span data-ttu-id="95891-194">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="95891-194">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="95891-195">UserID \\ -Stamm</span><span class="sxs-lookup"><span data-stu-id="95891-195">userid\\Root</span></span>  | <span data-ttu-id="95891-196">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="95891-196">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="95891-197">UserID- \\ Vertrauensstellung</span><span class="sxs-lookup"><span data-stu-id="95891-197">userid\\Trust</span></span> | <span data-ttu-id="95891-198">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="95891-198">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="95891-199">UserID- \\ ca</span><span class="sxs-lookup"><span data-stu-id="95891-199">userid\\CA</span></span>    | <span data-ttu-id="95891-200">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="95891-200">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_current_user_group_policy"></a><span data-ttu-id="95891-201">\_ \_ \_ Richtlinie zur aktuellen \_ Benutzer \_ Gruppe des Zertifikat Systems</span><span class="sxs-lookup"><span data-stu-id="95891-201">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY</span></span>

<span data-ttu-id="95891-202">\_ \_ \_ \_ Systemspeicher der aktuellen Benutzergruppen Richtlinien für Zertifikat Systeme \_ befinden sich am folgenden Registrierungs Speicherort:</span><span class="sxs-lookup"><span data-stu-id="95891-202">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY system stores are at the following registry location:</span></span>

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a><span data-ttu-id="95891-203">\_ \_ \_ \_ Gruppen \_ Richtlinie für den lokalen Zertifikat System Computer</span><span class="sxs-lookup"><span data-stu-id="95891-203">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>

<span data-ttu-id="95891-204">\_ \_ \_ \_ \_ Systemspeicher für die Gruppenrichtlinien-Systemspeicher des Zertifikat Systems befinden sich am folgenden Registrierungs Speicherort:</span><span class="sxs-lookup"><span data-stu-id="95891-204">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a><span data-ttu-id="95891-205">\_Enterprise-Zertifikat System \_ Speicher \_ lokaler \_ Computer \_</span><span class="sxs-lookup"><span data-stu-id="95891-205">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE</span></span>

<span data-ttu-id="95891-206">\_ \_ \_ \_ \_ Enterprise Enterprise Enterprise Computer Enterprise enthält Zertifikate, die Domänen übergreifend im Unternehmen freigegeben und aus dem globalen Unternehmensverzeichnis heruntergeladen wurden</span><span class="sxs-lookup"><span data-stu-id="95891-206">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE contains certificates shared across domains in the enterprise and downloaded from the global enterprise directory.</span></span> <span data-ttu-id="95891-207">Um den Unternehmens Speicher des Clients zu synchronisieren, wird das Unternehmensverzeichnis alle acht Stunden abgerufen, und Zertifikate werden automatisch im Hintergrund heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="95891-207">To synchronize the client's enterprise store, the enterprise directory is polled every eight hours and certificates are downloaded automatically in the background.</span></span>

<span data-ttu-id="95891-208">Die diesem Systemspeicher zugeordneten vordefinierten physischen Speicher sind wie folgt.</span><span class="sxs-lookup"><span data-stu-id="95891-208">The predefined physical stores associated with these system stores are as follows.</span></span>



| <span data-ttu-id="95891-209">System Speicher</span><span class="sxs-lookup"><span data-stu-id="95891-209">System store</span></span> | <span data-ttu-id="95891-210">Physischer Speicher</span><span class="sxs-lookup"><span data-stu-id="95891-210">Physical store</span></span> |
|--------------|----------------|
| <span data-ttu-id="95891-211">MY</span><span class="sxs-lookup"><span data-stu-id="95891-211">MY</span></span>           | <span data-ttu-id="95891-212">. Vorgegebene</span><span class="sxs-lookup"><span data-stu-id="95891-212">.Default</span></span>       |
| <span data-ttu-id="95891-213">Root</span><span class="sxs-lookup"><span data-stu-id="95891-213">Root</span></span>         | <span data-ttu-id="95891-214">. Vorgegebene</span><span class="sxs-lookup"><span data-stu-id="95891-214">.Default</span></span>       |
| <span data-ttu-id="95891-215">Vertrauensstellung</span><span class="sxs-lookup"><span data-stu-id="95891-215">Trust</span></span>        | <span data-ttu-id="95891-216">. Vorgegebene</span><span class="sxs-lookup"><span data-stu-id="95891-216">.Default</span></span>       |
| <span data-ttu-id="95891-217">CA</span><span class="sxs-lookup"><span data-stu-id="95891-217">CA</span></span>           | <span data-ttu-id="95891-218">. Vorgegebene</span><span class="sxs-lookup"><span data-stu-id="95891-218">.Default</span></span>       |



 

### <a name="remarks"></a><span data-ttu-id="95891-219">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95891-219">Remarks</span></span>

<span data-ttu-id="95891-220">Weitere physische Speicher können einem Systemspeicher mithilfe von [**certregisterphysicalstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore)zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="95891-220">Additional physical stores can be associated with a system store by using [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span></span>

<span data-ttu-id="95891-221">Die \_ Speicher des Zertifikats System \_ Speicher \_ Dienstanbieter-und Zertifikat \_ System \_ Speichers \_ werden geöffnet, indem der Name des Speichers in der Zeichenfolge, die an *pvpara* übergeben wird, mit dem Dienst-oder Benutzernamen, wie z. b. *ServiceName* \\ **Trust** oder, **Standardeinstellung** \\ **My**.</span><span class="sxs-lookup"><span data-stu-id="95891-221">CERT\_SYSTEM\_STORE\_SERVICE and CERT\_SYSTEM\_STORE\_USERS stores are opened by prefixing the name of the store in the string passed to *pvPara* with the service or user name such as *ServiceName*\\**Trust** or **.Default**\\**MY**.</span></span> <span data-ttu-id="95891-222">Der Speicherort des Zertifikats Systemspeicher Diensts oder des Zertifikats \_ \_ \_ \_ Systemspeicher Benutzers \_ \_ kann denselben Speicher im Zertifikat \_ System \_ Current \_ Service oder CERT \_ System \_ Store \_ Current \_ User mithilfe der [*textsicherheits*](../secgloss/s-gly.md) -ID (SID) des aktuellen Diensts oder Benutzers öffnen.</span><span class="sxs-lookup"><span data-stu-id="95891-222">The CERT\_SYSTEM\_STORE\_SERVICES or CERT\_SYSTEM\_STORE\_USERS location can open the same store in CERT\_SYSTEM\_CURRENT\_SERVICE or CERT\_SYSTEM\_STORE\_CURRENT\_USER by using the textual [*security identifier*](../secgloss/s-gly.md) (SID) of the current service or user.</span></span>

<span data-ttu-id="95891-223">Filialen in \_ der System \_ Speicher \_ \_ -Benutzergruppen \_ Richtlinie und der Zertifikat \_ System- \_ Gruppenrichtlinie für den lokalen \_ \_ \_ Computer in einer Netzwerk Einstellung werden beim Computer Start oder bei der Benutzeranmeldung von der Gruppenrichtlinie Vorlage (GPT) auf den Client Computer heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="95891-223">Stores in CERT\_SYSTEM\_STORE\_USER\_GROUP\_POLICY and CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY in a network setting are downloaded to the client computer from the Group Policy Template (GPT) during computer startup or user logon.</span></span> <span data-ttu-id="95891-224">Diese Speicher können nach dem Start oder der Anmeldung auf dem Client Computer aktualisiert werden, wenn der GPT von einem Administrator auf dem Domänen Server geändert wird.</span><span class="sxs-lookup"><span data-stu-id="95891-224">These stores can be updated on the client computer after startup or logon when the GPT is changed on the domain server by an administrator.</span></span> <span data-ttu-id="95891-225">Mit der [**certcontrolstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) -Funktion kann eine Anwendung benachrichtigt werden, wenn sich die Filialen an einem dieser Standorte geändert haben.</span><span class="sxs-lookup"><span data-stu-id="95891-225">The [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) function allows an application to be notified when stores in either of these locations have changed.</span></span>

<span data-ttu-id="95891-226">Die folgenden Systemspeicher Orte können Remote geöffnet werden:</span><span class="sxs-lookup"><span data-stu-id="95891-226">The following system store locations can be opened remotely:</span></span>

-   <span data-ttu-id="95891-227">\_lokaler Zertifikat System \_ Speicher- \_ \_ Computer</span><span class="sxs-lookup"><span data-stu-id="95891-227">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>
-   <span data-ttu-id="95891-228">\_ \_ \_ \_ \_ Gruppen \_ Richtlinie für den lokalen Zertifikat System Speicher</span><span class="sxs-lookup"><span data-stu-id="95891-228">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>
-   <span data-ttu-id="95891-229">Zertifikat- \_ System \_ Speicher \_ Dienste</span><span class="sxs-lookup"><span data-stu-id="95891-229">CERT\_SYSTEM\_STORE\_SERVICES</span></span>
-   <span data-ttu-id="95891-230">Zertifikat \_ System \_ Speicher- \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="95891-230">CERT\_SYSTEM\_STORE\_USERS</span></span>

<span data-ttu-id="95891-231">System Speicherorte werden Remote geöffnet, indem der Speicher Name in der Zeichenfolge, die an *pvpara* übergeben wird, mit dem Computernamen vorangestellt wird.</span><span class="sxs-lookup"><span data-stu-id="95891-231">System store locations are opened remotely by prefixing the store name in the string passed to *pvPara* with the computer name.</span></span> <span data-ttu-id="95891-232">Beispiele für Remote System-Speicher Namen:</span><span class="sxs-lookup"><span data-stu-id="95891-232">Examples of remote system store names are:</span></span>

-   <span data-ttu-id="95891-233">*Computername* \\  Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="95891-233">*ComputerName*\\**CA**</span></span>
-   <span data-ttu-id="95891-234">\\\\*Computername* \\  Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="95891-234">\\\\*ComputerName*\\**CA**</span></span>
-   <span data-ttu-id="95891-235">*Computername* \\ *Dienst Name* \\ **Vertrauens** Stellung</span><span class="sxs-lookup"><span data-stu-id="95891-235">*ComputerName*\\*ServiceName*\\**Trust**</span></span>
-   <span data-ttu-id="95891-236">\\\\*Computername* \\ *Dienst Name* \\ **Vertrauens** Stellung</span><span class="sxs-lookup"><span data-stu-id="95891-236">\\\\*ComputerName*\\*ServiceName*\\**Trust**</span></span>

 

 

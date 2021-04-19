---
description: Mithilfe des Windows-Sicherheitsmodells können Sie den Zugriff auf den Dienststeuerungs-Manager (Service Control Manager, SCM) und die Dienst Objekte steuern.
ms.assetid: 23d1c382-6ba4-49e2-8039-c2a91471076c
title: Dienst Sicherheit und Zugriffsrechte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7677b8a9f7a5e1fadf8231999d266a9474fb731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352698"
---
# <a name="service-security-and-access-rights"></a><span data-ttu-id="75d60-103">Dienst Sicherheit und Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="75d60-103">Service Security and Access Rights</span></span>

<span data-ttu-id="75d60-104">Mithilfe des Windows-Sicherheitsmodells können Sie den Zugriff auf den Dienststeuerungs-Manager (Service Control Manager, SCM) und die Dienst Objekte steuern.</span><span class="sxs-lookup"><span data-stu-id="75d60-104">The Windows security model enables you to control access to the service control manager (SCM) and service objects.</span></span> <span data-ttu-id="75d60-105">Die folgenden Abschnitte enthalten ausführliche Informationen:</span><span class="sxs-lookup"><span data-stu-id="75d60-105">The following sections provide detailed information:</span></span>

-   [<span data-ttu-id="75d60-106">Zugriffsrechte für den Dienststeuerungs-Manager</span><span class="sxs-lookup"><span data-stu-id="75d60-106">Access Rights for the Service Control Manager</span></span>](#access-rights-for-the-service-control-manager)
-   [<span data-ttu-id="75d60-107">Zugriffsrechte für einen Dienst</span><span class="sxs-lookup"><span data-stu-id="75d60-107">Access Rights for a Service</span></span>](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a><span data-ttu-id="75d60-108">Zugriffsrechte für den Dienststeuerungs-Manager</span><span class="sxs-lookup"><span data-stu-id="75d60-108">Access Rights for the Service Control Manager</span></span>

<span data-ttu-id="75d60-109">Im folgenden finden Sie die spezifischen Zugriffsrechte für den SCM.</span><span class="sxs-lookup"><span data-stu-id="75d60-109">The following are the specific access rights for the SCM.</span></span>



| <span data-ttu-id="75d60-110">Zugriffsrecht</span><span class="sxs-lookup"><span data-stu-id="75d60-110">Access right</span></span>                                   | <span data-ttu-id="75d60-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75d60-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d60-112">**SC \_ Manager für \_ alle \_ Zugriffe** (0xF 003F)</span><span class="sxs-lookup"><span data-stu-id="75d60-112">**SC\_MANAGER\_ALL\_ACCESS** (0xF003F)</span></span>         | <span data-ttu-id="75d60-113">Beinhaltet zusätzlich zu allen Zugriffsrechten in dieser Tabelle die **\_ \_ erforderlichen Standard Rechte**.</span><span class="sxs-lookup"><span data-stu-id="75d60-113">Includes **STANDARD\_RIGHTS\_REQUIRED**, in addition to all access rights in this table.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="75d60-114">**SC \_ Manager \_ - \_ Dienst erstellen** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="75d60-114">**SC\_MANAGER\_CREATE\_SERVICE** (0x0002)</span></span>      | <span data-ttu-id="75d60-115">Erforderlich, um die [**Funktion "**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) -Funktion" aufzurufen, um ein Dienst Objekt zu erstellen und es der Datenbank hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="75d60-115">Required to call the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to create a service object and add it to the database.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="75d60-116">**SC \_ Manager \_ Connect** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="75d60-116">**SC\_MANAGER\_CONNECT** (0x0001)</span></span>              | <span data-ttu-id="75d60-117">Ist erforderlich, um eine Verbindung mit dem Dienststeuerungs-Manager herzustellen.</span><span class="sxs-lookup"><span data-stu-id="75d60-117">Required to connect to the service control manager.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="75d60-118">**SC \_ Manager \_ Enumerate \_ Service** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="75d60-118">**SC\_MANAGER\_ENUMERATE\_SERVICE** (0x0004)</span></span>   | <span data-ttu-id="75d60-119">Erforderlich, um die Funktion " [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) " oder " [**enumservicesstatusex**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) " aufzurufen, um die Dienste aufzulisten, die in der Datenbank enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="75d60-119">Required to call the [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) or [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) function to list the services that are in the database.</span></span><br/> <span data-ttu-id="75d60-120">Muss die [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) -Funktion aufrufen, um Benachrichtigungen zu empfangen, wenn ein Dienst erstellt oder gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="75d60-120">Required to call the [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) function to receive notification when any service is created or deleted.</span></span><br/> |
| <span data-ttu-id="75d60-121">**SC \_ Manager \_ Sperre** (0x0008)</span><span class="sxs-lookup"><span data-stu-id="75d60-121">**SC\_MANAGER\_LOCK** (0x0008)</span></span>                 | <span data-ttu-id="75d60-122">Erforderlich, um die [**lockservicedatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) -Funktion aufzurufen, um eine Sperre für die Datenbank zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="75d60-122">Required to call the [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) function to acquire a lock on the database.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="75d60-123">**SC \_ Manager \_ Ändern der \_ Start \_ Konfiguration** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="75d60-123">**SC\_MANAGER\_MODIFY\_BOOT\_CONFIG** (0x0020)</span></span> | <span data-ttu-id="75d60-124">Erforderlich, um die [**notifybootconfigstatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) -Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="75d60-124">Required to call the [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) function.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="75d60-125">**SC \_ Status der Manager- \_ Abfrage \_ Sperre \_** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="75d60-125">**SC\_MANAGER\_QUERY\_LOCK\_STATUS** (0x0010)</span></span>  | <span data-ttu-id="75d60-126">Ist erforderlich, um die [**queryservicelockstatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) -Funktion zum Abrufen der Sperr Statusinformationen für die Datenbank aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="75d60-126">Required to call the [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) function to retrieve the lock status information for the database.</span></span>                                                                                                                                                                                                                         |



 

<span data-ttu-id="75d60-127">Im folgenden finden Sie die [allgemeinen Zugriffsrechte](/windows/desktop/SecAuthZ/generic-access-rights) für den SCM.</span><span class="sxs-lookup"><span data-stu-id="75d60-127">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for the SCM.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="75d60-128">Zugriffsrecht</span><span class="sxs-lookup"><span data-stu-id="75d60-128">Access right</span></span></th>
<th><span data-ttu-id="75d60-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75d60-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="75d60-130"><strong>GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-130"><strong>GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="75d60-131"><strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-131"><strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="75d60-132">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-132">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="75d60-133">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-133">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75d60-134"><strong>GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-134"><strong>GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="75d60-135"><strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-135"><strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="75d60-136">
<strong>SC_MANAGER_CREATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-136">
<strong>SC_MANAGER_CREATE_SERVICE</strong></span></span><br /><span data-ttu-id="75d60-137">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-137">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75d60-138"><strong>GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-138"><strong>GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="75d60-139"><strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-139"><strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="75d60-140">
<strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-140">
<strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="75d60-141">
<strong>SC_MANAGER_LOCK</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-141">
<strong>SC_MANAGER_LOCK</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75d60-142"><strong>GENERIC_ALL</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-142"><strong>GENERIC_ALL</strong></span></span></td>
<td><dl> <span data-ttu-id="75d60-143"><strong>SC_MANAGER_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-143"><strong>SC_MANAGER_ALL_ACCESS</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="75d60-144">Ein Prozess mit den richtigen Zugriffsrechten kann ein Handle für den SCM öffnen, das in den Funktionen [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**enumservicesstatusex**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)und [**queryservicelockstatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="75d60-144">A process with the correct access rights can open a handle to the SCM that can be used in the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa), and [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) functions.</span></span> <span data-ttu-id="75d60-145">Nur Prozesse mit Administrator Rechten können Handles für den SCM öffnen, der von den Funktionen "up Service [**Service**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) " und " [**lockservicedatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) " verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="75d60-145">Only processes with Administrator privileges are able to open handles to the SCM that can be used by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) functions.</span></span>

<span data-ttu-id="75d60-146">Das System erstellt die Sicherheits Beschreibung für den SCM.</span><span class="sxs-lookup"><span data-stu-id="75d60-146">The system creates the security descriptor for the SCM.</span></span> <span data-ttu-id="75d60-147">Um die Sicherheits Beschreibung für den SCM abzurufen oder festzulegen, verwenden Sie die Funktionen [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) und [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) mit einem Handle für das scmanager-Objekt.</span><span class="sxs-lookup"><span data-stu-id="75d60-147">To get or set the security descriptor for the SCM, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) and [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) functions with a handle to the SCManager object.</span></span>

<span data-ttu-id="75d60-148">**Windows Server 2003 und Windows XP:** Im Gegensatz zu den meisten anderen Sicherungs fähigen Objekten kann die Sicherheits Beschreibung für den SCM nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="75d60-148">**Windows Server 2003 and Windows XP:** Unlike most other securable objects, the security descriptor for the SCM cannot be modified.</span></span> <span data-ttu-id="75d60-149">Dieses Verhalten hat sich seit Windows Server 2003 mit Service Pack 1 (SP1) geändert.</span><span class="sxs-lookup"><span data-stu-id="75d60-149">This behavior has changed as of Windows Server 2003 with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="75d60-150">Die folgenden Zugriffsrechte werden gewährt.</span><span class="sxs-lookup"><span data-stu-id="75d60-150">The following access rights are granted.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="75d60-151">Konto</span><span class="sxs-lookup"><span data-stu-id="75d60-151">Account</span></span></th>
<th><span data-ttu-id="75d60-152">Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="75d60-152">Access rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="75d60-153">Remote authentifizierte Benutzer</span><span class="sxs-lookup"><span data-stu-id="75d60-153">Remote authenticated users</span></span></td>
<td><dl> <span data-ttu-id="75d60-154"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-154"><strong>SC_MANAGER_CONNECT</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75d60-155">Lokale authentifizierte Benutzer (einschließlich "LocalService" und "Network Service")</span><span class="sxs-lookup"><span data-stu-id="75d60-155">Local authenticated users (including LocalService and NetworkService)</span></span></td>
<td><dl> <span data-ttu-id="75d60-156"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-156"><strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="75d60-157">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-157">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="75d60-158">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-158">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br /><span data-ttu-id="75d60-159">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-159">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75d60-160">LocalSystem</span><span class="sxs-lookup"><span data-stu-id="75d60-160">LocalSystem</span></span></td>
<td><dl> <span data-ttu-id="75d60-161"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-161"><strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="75d60-162">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-162">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="75d60-163">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-163">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span></span><br /><span data-ttu-id="75d60-164">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-164">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br /><span data-ttu-id="75d60-165">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-165">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75d60-166">Administratoren</span><span class="sxs-lookup"><span data-stu-id="75d60-166">Administrators</span></span></td>
<td><dl> <span data-ttu-id="75d60-167"><strong>SC_MANAGER_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-167"><strong>SC_MANAGER_ALL_ACCESS</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="75d60-168">Beachten Sie, dass sich Remote Benutzer, die über das Netzwerk authentifiziert, aber nicht interaktiv angemeldet sind, mit dem SCM verbinden, aber keine Vorgänge ausführen müssen, die andere Zugriffsrechte erfordern.</span><span class="sxs-lookup"><span data-stu-id="75d60-168">Notice that remote users authenticated over the network but not interactively logged on can connect to the SCM but not perform operations that require other access rights.</span></span> <span data-ttu-id="75d60-169">Um diese Vorgänge auszuführen, muss der Benutzer interaktiv angemeldet sein, oder der Dienst muss eines der Dienst Konten verwenden.</span><span class="sxs-lookup"><span data-stu-id="75d60-169">To perform these operations, the user must be logged on interactively or the service must use one of the service accounts.</span></span>

<span data-ttu-id="75d60-170">**Windows Server 2003 und Windows XP:** Remote authentifizierte Benutzer erhalten den **SC \_ Manager \_ Connect**-, **SC \_ Manager- \_ enumerationsdienst \_**, **SC-Manager- \_ \_ Abfrage \_ Sperr \_ Status** und **Standard \_ Rechte \_ Lese** Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="75d60-170">**Windows Server 2003 and Windows XP:** Remote authenticated users are granted the **SC\_MANAGER\_CONNECT**, **SC\_MANAGER\_ENUMERATE\_SERVICE**, **SC\_MANAGER\_QUERY\_LOCK\_STATUS**, and **STANDARD\_RIGHTS\_READ** access rights.</span></span> <span data-ttu-id="75d60-171">Diese Zugriffsrechte werden wie in der vorherigen Tabelle unter Windows Server 2003 mit SP1 beschrieben eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="75d60-171">These access rights are restricted as described in the previous table as of Windows Server 2003 with SP1</span></span>

<span data-ttu-id="75d60-172">Wenn ein Prozess die [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) -Funktion verwendet, um ein Handle für eine Datenbank installierter Dienste zu öffnen, kann er Zugriffsrechte anfordern.</span><span class="sxs-lookup"><span data-stu-id="75d60-172">When a process uses the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to open a handle to a database of installed services, it can request access rights.</span></span> <span data-ttu-id="75d60-173">Das System führt vor dem Erteilen der angeforderten Zugriffsrechte eine Sicherheitsüberprüfung für die Sicherheits Beschreibung für den SCM aus.</span><span class="sxs-lookup"><span data-stu-id="75d60-173">The system performs a security check against the security descriptor for the SCM before granting the requested access rights.</span></span>

## <a name="access-rights-for-a-service"></a><span data-ttu-id="75d60-174">Zugriffsrechte für einen Dienst</span><span class="sxs-lookup"><span data-stu-id="75d60-174">Access Rights for a Service</span></span>

<span data-ttu-id="75d60-175">Im folgenden finden Sie die spezifischen Zugriffsrechte für einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="75d60-175">The following are the specific access rights for a service.</span></span>



| <span data-ttu-id="75d60-176">Zugriffsrecht</span><span class="sxs-lookup"><span data-stu-id="75d60-176">Access right</span></span>                                | <span data-ttu-id="75d60-177">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75d60-177">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d60-178">**Dienst \_ Sämtlicher \_ Zugriff** (0xF 01FF)</span><span class="sxs-lookup"><span data-stu-id="75d60-178">**SERVICE\_ALL\_ACCESS** (0xF01FF)</span></span>          | <span data-ttu-id="75d60-179">Enthält die Standard Rechte, die zusätzlich zu allen Zugriffsrechten in dieser Tabelle **\_ \_ erforderlich** sind.</span><span class="sxs-lookup"><span data-stu-id="75d60-179">Includes **STANDARD\_RIGHTS\_REQUIRED** in addition to all access rights in this table.</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="75d60-180">**Dienst \_ Ändern der \_ Konfiguration** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="75d60-180">**SERVICE\_CHANGE\_CONFIG** (0x0002)</span></span>        | <span data-ttu-id="75d60-181">Erforderlich, um die [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) -oder [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) -Funktion aufzurufen, um die Dienst Konfiguration zu ändern.</span><span class="sxs-lookup"><span data-stu-id="75d60-181">Required to call the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) or [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function to change the service configuration.</span></span> <span data-ttu-id="75d60-182">Da dem Aufrufer das Recht erteilt wird, die ausführbare Datei zu ändern, die das System ausführt, sollte er nur Administratoren gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="75d60-182">Because this grants the caller the right to change the executable file that the system runs, it should be granted only to administrators.</span></span>                                                              |
| <span data-ttu-id="75d60-183">**Dienst \_ \_Abhängige Elemente aufzählen** (0x0008)</span><span class="sxs-lookup"><span data-stu-id="75d60-183">**SERVICE\_ENUMERATE\_DEPENDENTS** (0x0008)</span></span> | <span data-ttu-id="75d60-184">Ist erforderlich, um die [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) -Funktion aufzurufen, um alle vom Dienst abhängigen Dienste aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="75d60-184">Required to call the [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) function to enumerate all the services dependent on the service.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="75d60-185">**Dienst \_ Abfrage** (0x0080)</span><span class="sxs-lookup"><span data-stu-id="75d60-185">**SERVICE\_INTERROGATE** (0x0080)</span></span>           | <span data-ttu-id="75d60-186">Erforderlich, um die [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) -Funktion aufzurufen, um den Dienst aufzufordern, seinen Status sofort zu melden.</span><span class="sxs-lookup"><span data-stu-id="75d60-186">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to ask the service to report its status immediately.</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="75d60-187">**Dienst \_ \_Anhalten Fortsetzen** (0x0040)</span><span class="sxs-lookup"><span data-stu-id="75d60-187">**SERVICE\_PAUSE\_CONTINUE** (0x0040)</span></span>       | <span data-ttu-id="75d60-188">Erforderlich, um die [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) -Funktion aufzurufen, um den Dienst anzuhalten oder fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="75d60-188">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to pause or continue the service.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="75d60-189">**Dienst \_ Abfrage \_ Konfiguration** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="75d60-189">**SERVICE\_QUERY\_CONFIG** (0x0001)</span></span>         | <span data-ttu-id="75d60-190">Erforderlich, um die [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) -Funktion und die [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) -Funktion zum Abfragen der Dienst Konfiguration aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="75d60-190">Required to call the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) functions to query the service configuration.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="75d60-191">**Dienst \_ Abfrage \_ Status** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="75d60-191">**SERVICE\_QUERY\_STATUS** (0x0004)</span></span>         | <span data-ttu-id="75d60-192">Ist erforderlich, um die Funktion [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) oder [**queryservicestatusex**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) aufzurufen, um den Dienststeuerungs-Manager über den Status des Dienstanbieter zu Fragen.</span><span class="sxs-lookup"><span data-stu-id="75d60-192">Required to call the [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) or [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function to ask the service control manager about the status of the service.</span></span><br/> <span data-ttu-id="75d60-193">Muss die [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) -Funktion aufrufen, um Benachrichtigungen zu empfangen, wenn der Status eines Diensts geändert wird.</span><span class="sxs-lookup"><span data-stu-id="75d60-193">Required to call the [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) function to receive notification when a service changes status.</span></span><br/> |
| <span data-ttu-id="75d60-194">**Dienst \_ Start** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="75d60-194">**SERVICE\_START** (0x0010)</span></span>                 | <span data-ttu-id="75d60-195">Erforderlich zum Aufrufen der [**Start Service**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) -Funktion zum Starten des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="75d60-195">Required to call the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function to start the service.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="75d60-196">**Dienst \_ Beendigung** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="75d60-196">**SERVICE\_STOP** (0x0020)</span></span>                  | <span data-ttu-id="75d60-197">Erforderlich, um die [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) -Funktion zum Abbrechen des dienstandens aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="75d60-197">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to stop the service.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="75d60-198">**Dienst \_ Benutzer \_ definiertes \_ Steuer** Element (0x0100)</span><span class="sxs-lookup"><span data-stu-id="75d60-198">**SERVICE\_USER\_DEFINED\_CONTROL**(0x0100)</span></span> | <span data-ttu-id="75d60-199">Erforderlich, um die [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) -Funktion aufzurufen, um einen benutzerdefinierten Steuerelement Code anzugeben.</span><span class="sxs-lookup"><span data-stu-id="75d60-199">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to specify a user-defined control code.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="75d60-200">Im folgenden finden Sie die [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) für einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="75d60-200">The following are the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) for a service.</span></span>



| <span data-ttu-id="75d60-201">Zugriffsrecht</span><span class="sxs-lookup"><span data-stu-id="75d60-201">Access right</span></span>                 | <span data-ttu-id="75d60-202">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75d60-202">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d60-203">**Zugreifen auf die \_ System \_ Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="75d60-203">**ACCESS\_SYSTEM\_SECURITY**</span></span> | <span data-ttu-id="75d60-204">Erforderlich, um die [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) -oder [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) -Funktion für den Zugriff auf die SACL aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="75d60-204">Required to call the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) or [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to access the SACL.</span></span> <span data-ttu-id="75d60-205">Die richtige Möglichkeit, um diesen Zugriff zu erhalten, besteht darin, die [**Berechtigung**](/windows/desktop/SecAuthZ/privileges) " **SE \_ Security \_ Name**" im aktuellen Zugriffs Token des Aufrufers zu aktivieren, das Handle für den **Zugriff auf \_ System \_ Sicherheits** Zugriff zu öffnen und die Berechtigung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="75d60-205">The proper way to obtain this access is to enable the **SE\_SECURITY\_NAME**[**privilege**](/windows/desktop/SecAuthZ/privileges) in the caller's current access token, open the handle for **ACCESS\_SYSTEM\_SECURITY** access, and then disable the privilege.</span></span> |
| <span data-ttu-id="75d60-206">**Löschen**   (0x10000)</span><span class="sxs-lookup"><span data-stu-id="75d60-206">**DELETE**   (0x10000)</span></span>       | <span data-ttu-id="75d60-207">Zum Aufrufen der Funktion " [**Delta**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) Service" erforderlich, um den Dienst zu löschen.</span><span class="sxs-lookup"><span data-stu-id="75d60-207">Required to call the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to delete the service.</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="75d60-208">**Lesen Sie \_ Steuer**  Element (0x20000)</span><span class="sxs-lookup"><span data-stu-id="75d60-208">**READ\_CONTROL**  (0x20000)</span></span>    | <span data-ttu-id="75d60-209">Erforderlich, um die Funktion [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) aufzurufen, um die Sicherheits Beschreibung des Dienst Objekts abzufragen.</span><span class="sxs-lookup"><span data-stu-id="75d60-209">Required to call the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function to query the security descriptor of the service object.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="75d60-210">**Schreiben \_ DAC**  (0x40000)</span><span class="sxs-lookup"><span data-stu-id="75d60-210">**WRITE\_DAC**  (0x40000)</span></span>    | <span data-ttu-id="75d60-211">Zum Aufrufen der [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) -Funktion erforderlich, um den **DACL** -Member der Sicherheits Beschreibung des Dienst Objekts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="75d60-211">Required to call the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to modify the **Dacl** member of the service object's security descriptor.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="75d60-212">**Schreiben \_ Besitzer** (0x80000)</span><span class="sxs-lookup"><span data-stu-id="75d60-212">**WRITE\_OWNER** (0x80000)</span></span>   | <span data-ttu-id="75d60-213">Erforderlich zum Aufrufen der [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) -Funktion zum Ändern des **Besitzers** und der **Gruppen** Mitglieder der Sicherheits Beschreibung des Dienst Objekts.</span><span class="sxs-lookup"><span data-stu-id="75d60-213">Required to call the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to modify the **Owner** and **Group** members of the service object's security descriptor.</span></span>                                                                                                                                                                                                                                                   |



 

<span data-ttu-id="75d60-214">Im folgenden finden Sie die [allgemeinen Zugriffsrechte](/windows/desktop/SecAuthZ/generic-access-rights) für einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="75d60-214">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a service.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="75d60-215">Zugriffsrecht</span><span class="sxs-lookup"><span data-stu-id="75d60-215">Access right</span></span></th>
<th><span data-ttu-id="75d60-216">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75d60-216">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="75d60-217"><strong>GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-217"><strong>GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="75d60-218"><strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-218"><strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="75d60-219">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-219">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="75d60-220">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-220">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="75d60-221">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-221">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="75d60-222">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-222">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75d60-223"><strong>GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-223"><strong>GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="75d60-224"><strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-224"><strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="75d60-225">
<strong>SERVICE_CHANGE_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-225">
<strong>SERVICE_CHANGE_CONFIG</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75d60-226"><strong>GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-226"><strong>GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="75d60-227"><strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-227"><strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="75d60-228">
<strong>SERVICE_START</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-228">
<strong>SERVICE_START</strong></span></span><br /><span data-ttu-id="75d60-229">
<strong>SERVICE_STOP</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-229">
<strong>SERVICE_STOP</strong></span></span><br /><span data-ttu-id="75d60-230">
<strong>SERVICE_PAUSE_CONTINUE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-230">
<strong>SERVICE_PAUSE_CONTINUE</strong></span></span><br /><span data-ttu-id="75d60-231">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-231">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="75d60-232">Der SCM erstellt die Sicherheits Beschreibung eines Dienst Objekts, wenn der Dienst von der Funktion "| [**ateservice**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) " installiert wird.</span><span class="sxs-lookup"><span data-stu-id="75d60-232">The SCM creates a service object's security descriptor when the service is installed by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function.</span></span> <span data-ttu-id="75d60-233">Die Standard Sicherheits Beschreibung eines Dienst Objekts gewährt den folgenden Zugriff.</span><span class="sxs-lookup"><span data-stu-id="75d60-233">The default security descriptor of a service object grants the following access.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="75d60-234">Konto</span><span class="sxs-lookup"><span data-stu-id="75d60-234">Account</span></span></th>
<th><span data-ttu-id="75d60-235">Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="75d60-235">Access rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="75d60-236">Remote authentifizierte Benutzer</span><span class="sxs-lookup"><span data-stu-id="75d60-236">Remote authenticated users</span></span></td>
<td><span data-ttu-id="75d60-237">Standardmäßig nicht erteilt. <strong>Windows Server 2003 mit SP1: SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-237">Not granted by default.<strong>Windows Server 2003 with SP1:  SERVICE_USER_DEFINED_CONTROL</strong></span></span><br/> <span data-ttu-id="75d60-238"><strong>Windows Server 2003 und Windows XP:</strong> Die Zugriffsrechte für Remote authentifizierte Benutzer sind identisch mit denen für lokale authentifizierte Benutzer.</span><span class="sxs-lookup"><span data-stu-id="75d60-238"><strong>Windows Server 2003 and Windows XP:</strong> The access rights for remote authenticated users are the same as for local authenticated users.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75d60-239">Lokale authentifizierte Benutzer (einschließlich "LocalService" und "Network Service")</span><span class="sxs-lookup"><span data-stu-id="75d60-239">Local authenticated users (including LocalService and NetworkService)</span></span></td>
<td><dl> <span data-ttu-id="75d60-240"><strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-240"><strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="75d60-241">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-241">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br /><span data-ttu-id="75d60-242">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-242">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="75d60-243">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-243">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="75d60-244">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-244">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="75d60-245">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-245">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75d60-246">LocalSystem</span><span class="sxs-lookup"><span data-stu-id="75d60-246">LocalSystem</span></span></td>
<td><dl> <span data-ttu-id="75d60-247"><strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-247"><strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="75d60-248">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-248">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br /><span data-ttu-id="75d60-249">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-249">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="75d60-250">
<strong>SERVICE_PAUSE_CONTINUE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-250">
<strong>SERVICE_PAUSE_CONTINUE</strong></span></span><br /><span data-ttu-id="75d60-251">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-251">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="75d60-252">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-252">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="75d60-253">
<strong>SERVICE_START</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-253">
<strong>SERVICE_START</strong></span></span><br /><span data-ttu-id="75d60-254">
<strong>SERVICE_STOP</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-254">
<strong>SERVICE_STOP</strong></span></span><br /><span data-ttu-id="75d60-255">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-255">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75d60-256">Administratoren</span><span class="sxs-lookup"><span data-stu-id="75d60-256">Administrators</span></span></td>
<td><dl> <span data-ttu-id="75d60-257"><strong>DELETE</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-257"><strong>DELETE</strong></span></span><br /><span data-ttu-id="75d60-258">
<strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-258">
<strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="75d60-259">
<strong>SERVICE_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-259">
<strong>SERVICE_ALL_ACCESS</strong></span></span><br /><span data-ttu-id="75d60-260">
<strong>WRITE_DAC</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-260">
<strong>WRITE_DAC</strong></span></span><br /><span data-ttu-id="75d60-261">
<strong>WRITE_OWNER</strong></span><span class="sxs-lookup"><span data-stu-id="75d60-261">
<strong>WRITE_OWNER</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="75d60-262">Zum Ausführen von Vorgängen muss der Benutzer interaktiv angemeldet sein, oder der Dienst muss eines der Dienst Konten verwenden.</span><span class="sxs-lookup"><span data-stu-id="75d60-262">To perform any operations, the user must be logged on interactively or the service must use one of the service accounts.</span></span>

<span data-ttu-id="75d60-263">Um die Sicherheits Beschreibung für ein Dienst Objekt abzurufen oder festzulegen, verwenden Sie die Funktionen [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) und [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="75d60-263">To get or set the security descriptor for a service object, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) and [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) functions.</span></span> <span data-ttu-id="75d60-264">Weitere Informationen finden Sie unter [Ändern der DACL für einen Dienst](modifying-the-dacl-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="75d60-264">For more information, see [Modifying the DACL for a Service](modifying-the-dacl-for-a-service.md).</span></span>

<span data-ttu-id="75d60-265">Wenn ein Prozess die [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) -Funktion verwendet, prüft das System die angeforderten Zugriffsrechte auf die Sicherheits Beschreibung des Dienst Objekts.</span><span class="sxs-lookup"><span data-stu-id="75d60-265">When a process uses the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) function, the system checks the requested access rights against the security descriptor for the service object.</span></span>

<span data-ttu-id="75d60-266">Das erteilen bestimmter Zugriffsrechte für nicht vertrauenswürdige Benutzer (z. b. **\_ \_ Konfiguration von Dienst Änderungen** oder **Dienst \_ Stopps**) kann es Ihnen ermöglichen, die Ausführung des Dienstanbieter zu beeinträchtigen und möglicherweise das Ausführen von Anwendungen unter dem LocalSystem-Konto zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="75d60-266">Granting certain access rights to untrusted users (such as **SERVICE\_CHANGE\_CONFIG** or **SERVICE\_STOP**) can allow them to interfere with the execution of your service, and possibly allow them to run applications under the LocalSystem account.</span></span>

<span data-ttu-id="75d60-267">Wenn die [**enumservicesstatusex-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) aufgerufen wird und der Aufrufer nicht über das Zugriffsrecht des **Dienst \_ Abfrage \_ Status** für einen Dienst verfügt, wird der Dienst aus der Liste der an den Client zurückgegebenen Dienste im Hintergrund weggelassen.</span><span class="sxs-lookup"><span data-stu-id="75d60-267">When [**EnumServicesStatusEx function**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) is called, if the caller does not have the **SERVICE\_QUERY\_STATUS** access right to a service, the service is silently omitted from the list of services returned to the client.</span></span>

 


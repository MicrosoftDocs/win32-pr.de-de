---
title: Win32_TSLicenseServer-Klasse
description: Stellt Methoden und Eigenschaften zum Anzeigen und konfigurieren Remotedesktop Lizenzierung (RD-Lizenzierung) auf einem Remotedesktop Lizenzserver bereit.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseServer-Klasse Remotedesktopdienste
- Win32_TSLicenseServer Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer
- Win32_TSLicenseServer.FirstName
- Win32_TSLicenseServer.LastName
- Win32_TSLicenseServer.Company
- Win32_TSLicenseServer.CountryRegion
- Win32_TSLicenseServer.eMail
- Win32_TSLicenseServer.OrgUnit
- Win32_TSLicenseServer.Address
- Win32_TSLicenseServer.City
- Win32_TSLicenseServer.State
- Win32_TSLicenseServer.PostalCode
- Win32_TSLicenseServer.ServerRole
- Win32_TSLicenseServer.DatabasePath
- Win32_TSLicenseServer.ProductId
- Win32_TSLicenseServer.Version
- Win32_TSLicenseServer.VersionNumber
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31951b943723e620414b2f714327db8c786f9ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956746"
---
# <a name="win32_tslicenseserver-class"></a><span data-ttu-id="30ec9-105">Win32-Klasse "-Klasse (Klasse)" \_</span><span class="sxs-lookup"><span data-stu-id="30ec9-105">Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="30ec9-106">Stellt Methoden und Eigenschaften zum Anzeigen und konfigurieren Remotedesktop Lizenzierung (RD-Lizenzierung) auf einem Remotedesktop Lizenzserver bereit.</span><span class="sxs-lookup"><span data-stu-id="30ec9-106">Provides methods and properties to view and configure Remote Desktop Licensing (RD Licensing) on a Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ec9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="30ec9-107">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseServer
{
  string FirstName;
  string LastName;
  string Company;
  string CountryRegion;
  string eMail;
  string OrgUnit;
  string Address;
  string City;
  string State;
  string PostalCode;
  uint32 ServerRole;
  string DatabasePath;
  string ProductId;
  string Version;
  string VersionNumber;
};
```

## <a name="members"></a><span data-ttu-id="30ec9-108">Member</span><span class="sxs-lookup"><span data-stu-id="30ec9-108">Members</span></span>

<span data-ttu-id="30ec9-109">Die Win32-Klasse " **\_ zlicenseserver** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="30ec9-109">The **Win32\_TSLicenseServer** class has these types of members:</span></span>

-   [<span data-ttu-id="30ec9-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="30ec9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="30ec9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="30ec9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="30ec9-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="30ec9-112">Methods</span></span>

<span data-ttu-id="30ec9-113">Die Win32-Klasse " **\_ zlicenseserver** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="30ec9-113">The **Win32\_TSLicenseServer** class has these methods.</span></span>



| <span data-ttu-id="30ec9-114">Methode</span><span class="sxs-lookup"><span data-stu-id="30ec9-114">Method</span></span>                                                                                   | <span data-ttu-id="30ec9-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30ec9-115">Description</span></span>                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30ec9-116">**Activateserver**</span><span class="sxs-lookup"><span data-stu-id="30ec9-116">**ActivateServer**</span></span>](activateserver-win32-tslicenseserver.md)                           | <span data-ttu-id="30ec9-117">Aktiviert den Remotedesktop Lizenzserver mit einer Remotedesktop Lizenzserver-ID, die über das Telefon oder das Internet abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="30ec9-117">Activates the Remote Desktop license server by using a Remote Desktop license server ID that is obtained over the phone or the Internet.</span></span><br/>                                                                                           |
| [<span data-ttu-id="30ec9-118">**Activateserverautomatic**</span><span class="sxs-lookup"><span data-stu-id="30ec9-118">**ActivateServerAutomatic**</span></span>](activateserverautomatic-win32-tslicenseserver.md)         | <span data-ttu-id="30ec9-119">Aktiviert den Remotedesktop Lizenzserver automatisch über das Internet.</span><span class="sxs-lookup"><span data-stu-id="30ec9-119">Activates the Remote Desktop license server automatically over the Internet.</span></span> <span data-ttu-id="30ec9-120">Die Eigenschaften " **FirstName**", " **LastName**", " **Company**" und " **CountryRegion** " dürfen nicht leer sein, wenn diese Methode aufgerufen wird, oder die Methode schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="30ec9-120">The **FirstName**, **LastName**, **Company**, and **CountryRegion** properties must not be empty when this method is called, or the method will fail.</span></span><br/> |
| [<span data-ttu-id="30ec9-121">**Addlstozlsgroup**</span><span class="sxs-lookup"><span data-stu-id="30ec9-121">**AddLStoTSLSGroup**</span></span>](addlstotslsgroup-win32-tslicenseserver.md)                       | <span data-ttu-id="30ec9-122">Fügt den Remotedesktop-Lizenzserver der Gruppe Remotedesktop Lizenzserver auf einem Domänen Controller in derselben Domäne wie der Lizenzserver hinzu.</span><span class="sxs-lookup"><span data-stu-id="30ec9-122">Adds the Remote Desktop license server to the Remote Desktop License Servers group on a domain controller in the same domain as the license server.</span></span><br/>                                                                                |
| [<span data-ttu-id="30ec9-123">**ChangeRole**</span><span class="sxs-lookup"><span data-stu-id="30ec9-123">**ChangeRole**</span></span>](changerole-win32-tslicenseserver.md)                                   | <span data-ttu-id="30ec9-124">Ändert den Ermittlungs Bereich des Remotedesktop Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="30ec9-124">Changes the discovery scope of the Remote Desktop license server.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="30ec9-125">**"Kreatetscgroup"**</span><span class="sxs-lookup"><span data-stu-id="30ec9-125">**CreateTSCGroup**</span></span>](createtscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="30ec9-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30ec9-126">This method is not supported.</span></span><br/> <span data-ttu-id="30ec9-127">**Windows Server 2008 R2 und Windows Server 2008:** Erstellt die lokale Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenz Server.</span><span class="sxs-lookup"><span data-stu-id="30ec9-127">**Windows Server 2008 R2 and Windows Server 2008:** Creates the Terminal Server Computers local group on the Remote Desktop license server.</span></span><br/>                                               |
| [<span data-ttu-id="30ec9-128">**Geräteserver**</span><span class="sxs-lookup"><span data-stu-id="30ec9-128">**DeactivateServer**</span></span>](deactivateserver-win32-tslicenseserver.md)                       | <span data-ttu-id="30ec9-129">Deaktiviert den Remotedesktop Lizenzserver mithilfe eines Bestätigungs Codes, der über das Telefon empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="30ec9-129">Deactivates the Remote Desktop license server by using a confirmation code that is received over the phone.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="30ec9-130">**"Deaktiviert"**</span><span class="sxs-lookup"><span data-stu-id="30ec9-130">**DeactivateServerAutomatic**</span></span>](deactivateserverautomatic-win32-tslicenseserver.md)     | <span data-ttu-id="30ec9-131">Deaktiviert den Remotedesktop Lizenzserver über das Internet.</span><span class="sxs-lookup"><span data-stu-id="30ec9-131">Deactivates the Remote Desktop license server over the Internet.</span></span> <span data-ttu-id="30ec9-132">Die Eigenschaften " **FirstName** " und " **LastName** " dürfen nicht leer sein, wenn diese Methode aufgerufen wird, oder die Methode schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="30ec9-132">The **FirstName** and **LastName** properties must not be empty when this method is called, or the method will fail.</span></span><br/>                                              |
| [<span data-ttu-id="30ec9-133">**Getactivationstatus**</span><span class="sxs-lookup"><span data-stu-id="30ec9-133">**GetActivationStatus**</span></span>](getactivationstatus-win32-tslicenseserver.md)                 | <span data-ttu-id="30ec9-134">Ruft den aktuellen Aktivierungs Status ab.</span><span class="sxs-lookup"><span data-stu-id="30ec9-134">Retrieves the current activation status.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="30ec9-135">**Getlicenseserverid**</span><span class="sxs-lookup"><span data-stu-id="30ec9-135">**GetLicenseServerId**</span></span>](getlicenseserverid-win32-tslicenseserver.md)                   | <span data-ttu-id="30ec9-136">Ruft eine Remotedesktop Lizenzserver-ID ab, wenn der Server zurzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="30ec9-136">Retrieves a Remote Desktop license server ID if the server is currently activated.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="30ec9-137">**Islsinzlsgroup**</span><span class="sxs-lookup"><span data-stu-id="30ec9-137">**IsLSinTSLSGroup**</span></span>](islsintslsgroup-win32-tslicenseserver.md)                         | <span data-ttu-id="30ec9-138">Ruft ab, ob der Remotedesktop Lizenzserver Mitglied der Gruppe Remotedesktop Lizenzserver auf einem Domänen Controller in einer bestimmten Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="30ec9-138">Retrieves whether the Remote Desktop license server is a member of the Remote Desktop License Servers group on a domain controller in a given domain.</span></span><br/>                                                                              |
| [<span data-ttu-id="30ec9-139">**Islsondc**</span><span class="sxs-lookup"><span data-stu-id="30ec9-139">**IsLSonDC**</span></span>](islsondc-win32-tslicenseserver.md)                                       | <span data-ttu-id="30ec9-140">Ruft ab, ob RD-Lizenzierung auf einem Domänen Controller installiert ist.</span><span class="sxs-lookup"><span data-stu-id="30ec9-140">Retrieves whether RD Licensing is installed on a domain controller.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="30ec9-141">**Isllexventupgradegpabled**</span><span class="sxs-lookup"><span data-stu-id="30ec9-141">**IsLSPreventUpgradeGPEnabled**</span></span>](islspreventupgradegpenabled-win32-tslicenseserver.md) | <span data-ttu-id="30ec9-142">Ruft ab, ob die Gruppenrichtlinien Einstellung "Lizenz Upgrade verhindern" auf dem Remotedesktop-Lizenzserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="30ec9-142">Retrieves whether the "prevent license upgrade" group policy setting is enabled on the Remote Desktop license server.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="30ec9-143">**Islspublished**</span><span class="sxs-lookup"><span data-stu-id="30ec9-143">**IsLSPublished**</span></span>](islspublished-win32-tslicenseserver.md)                             | <span data-ttu-id="30ec9-144">Ruft ab, ob der Remotedesktop Lizenzserver in Active Directory Domain Services (AD DS) veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="30ec9-144">Retrieves whether the Remote Desktop license server is published in Active Directory Domain Services (AD DS).</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="30ec9-145">**Islsregistereddescp**</span><span class="sxs-lookup"><span data-stu-id="30ec9-145">**IsLSRegisteredToSCP**</span></span>](win32-tslicenseserver-islsregisteredtoscp.md)                 | <span data-ttu-id="30ec9-146">Ruft ab, ob der Remotedesktop Lizenzserver als Dienst Verbindungspunkt in Active Directory Domain Services registriert ist.</span><span class="sxs-lookup"><span data-stu-id="30ec9-146">Retrieves whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                               |
| [<span data-ttu-id="30ec9-147">**Islssecgrpgpabled**</span><span class="sxs-lookup"><span data-stu-id="30ec9-147">**IsLSSecGrpGPEnabled**</span></span>](islssecgrpgpenabled-win32-tslicenseserver.md)                 | <span data-ttu-id="30ec9-148">Ruft ab, ob die Gruppenrichtlinien Einstellung "Lizenzserver-Sicherheitsgruppe" auf dem Remotedesktop-Lizenzserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="30ec9-148">Retrieves whether the "license server security group" group policy setting is enabled on the Remote Desktop license server.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="30ec9-149">**Issecureaccessallowed**</span><span class="sxs-lookup"><span data-stu-id="30ec9-149">**IsSecureAccessAllowed**</span></span>](issecureaccessallowed-win32-tslicenseserver.md)             | <span data-ttu-id="30ec9-150">Ruft ab, ob ein RD-Sitzungshost Server Remotedesktopdienste Client Zugriffs Lizenzen (RDS-CALs) vom Remotedesktop Lizenzserver anfordern darf.</span><span class="sxs-lookup"><span data-stu-id="30ec9-150">Retrieves whether an RD Session Host server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from the Remote Desktop license server.</span></span><br/>                                                                |
| [<span data-ttu-id="30ec9-151">**Istscgrouppresent**</span><span class="sxs-lookup"><span data-stu-id="30ec9-151">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)                     | <span data-ttu-id="30ec9-152">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30ec9-152">This method is not supported.</span></span><br/> <span data-ttu-id="30ec9-153">**Windows Server 2008 R2 und Windows Server 2008:** Ruft ab, ob die lokale Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenz Server vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="30ec9-153">**Windows Server 2008 R2 and Windows Server 2008:** Retrieves whether the Terminal Server Computers local group exists on the Remote Desktop license server.</span></span><br/>                              |
| [<span data-ttu-id="30ec9-154">**Istsintscgroup**</span><span class="sxs-lookup"><span data-stu-id="30ec9-154">**IsTSinTSCGroup**</span></span>](istsintscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="30ec9-155">Ruft ab, ob ein RD-Sitzungshost Server Mitglied der lokalen Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenzserver ist.</span><span class="sxs-lookup"><span data-stu-id="30ec9-155">Retrieves whether an RD Session Host server is a member of the Terminal Server Computers local group on the Remote Desktop license server.</span></span><br/>                                                                                         |
| [<span data-ttu-id="30ec9-156">**Publishls**</span><span class="sxs-lookup"><span data-stu-id="30ec9-156">**PublishLS**</span></span>](publishls-win32-tslicenseserver.md)                                     | <span data-ttu-id="30ec9-157">Veröffentlicht den Remotedesktop Lizenzserver in AD DS.</span><span class="sxs-lookup"><span data-stu-id="30ec9-157">Publishes the Remote Desktop license server in AD DS.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="30ec9-158">**Reactivateserver**</span><span class="sxs-lookup"><span data-stu-id="30ec9-158">**ReactivateServer**</span></span>](reactivateserver-win32-tslicenseserver.md)                       | <span data-ttu-id="30ec9-159">Reaktiviert den Remotedesktop Lizenzserver, indem eine neue Remotedesktop Lizenzserver-ID verwendet wird, die über das Telefon oder das Internet abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="30ec9-159">Reactivates the Remote Desktop license server by using a new Remote Desktop license server ID that is obtained over the phone or the Internet.</span></span><br/>                                                                                     |
| [<span data-ttu-id="30ec9-160">**Reactivateserverautomatic**</span><span class="sxs-lookup"><span data-stu-id="30ec9-160">**ReactivateServerAutomatic**</span></span>](reactivateserverautomatic-win32-tslicenseserver.md)     | <span data-ttu-id="30ec9-161">Aktiviert den Remotedesktop Lizenzserver über das Internet erneut.</span><span class="sxs-lookup"><span data-stu-id="30ec9-161">Reactivates the Remote Desktop license server over the Internet.</span></span> <span data-ttu-id="30ec9-162">Die Eigenschaften " **FirstName** " und " **LastName** " dürfen nicht leer sein, wenn diese Methode aufgerufen wird, oder die Methode schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="30ec9-162">The **FirstName** and **LastName** properties must not be empty when this method is called, or the method will fail.</span></span><br/>                                              |
| [<span data-ttu-id="30ec9-163">**Registerlstoscp**</span><span class="sxs-lookup"><span data-stu-id="30ec9-163">**RegisterLSToSCP**</span></span>](win32-tslicenseserver-registerlstoscp.md)                         | <span data-ttu-id="30ec9-164">Registriert den Remotedesktop-Lizenzserver als Dienst Verbindungspunkt in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="30ec9-164">Registers the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="30ec9-165">**Removelsfromzlsgroup**</span><span class="sxs-lookup"><span data-stu-id="30ec9-165">**RemoveLSfromTSLSGroup**</span></span>](removelsfromtslsgroup-win32-tslicenseserver.md)             | <span data-ttu-id="30ec9-166">Hierdurch wird der Remotedesktop Lizenzserver aus der Gruppe Remotedesktop Lizenzserver auf einem Domänen Controller in derselben Domäne wie der Lizenzserver entfernt.</span><span class="sxs-lookup"><span data-stu-id="30ec9-166">Removes the Remote Desktop license server from the Remote Desktop License Servers group on a domain controller in the same domain as the license server.</span></span><br/>                                                                           |
| [<span data-ttu-id="30ec9-167">**Removetscgroup**</span><span class="sxs-lookup"><span data-stu-id="30ec9-167">**RemoveTSCGroup**</span></span>](removetscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="30ec9-168">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30ec9-168">This method is not supported.</span></span><br/> <span data-ttu-id="30ec9-169">**Windows Server 2008 R2 und Windows Server 2008:** Entfernt die lokale Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenz Server.</span><span class="sxs-lookup"><span data-stu-id="30ec9-169">**Windows Server 2008 R2 and Windows Server 2008:** Removes the Terminal Server Computers local group from the Remote Desktop license server.</span></span><br/>                                             |
| [<span data-ttu-id="30ec9-170">**Nicht publishls**</span><span class="sxs-lookup"><span data-stu-id="30ec9-170">**UnpublishLS**</span></span>](unpublishls-win32-tslicenseserver.md)                                 | <span data-ttu-id="30ec9-171">Veröffentlichung eines Remotedesktop Lizenzservers aus AD DS.</span><span class="sxs-lookup"><span data-stu-id="30ec9-171">Unpublishes a Remote Desktop license server from AD DS.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="30ec9-172">**Unregisterlsfromscp**</span><span class="sxs-lookup"><span data-stu-id="30ec9-172">**UnRegisterLSFromSCP**</span></span>](win32-tslicenseserver-unregisterlsfromscp.md)                 | <span data-ttu-id="30ec9-173">Entfernt den Remotedesktop-Lizenzserver als Dienst Verbindungspunkt in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="30ec9-173">Removes the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="30ec9-174">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="30ec9-174">Properties</span></span>

<span data-ttu-id="30ec9-175">Die Win32-Klasse "Klasse- **\_ licenseserver** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="30ec9-175">The **Win32\_TSLicenseServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30ec9-176">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="30ec9-176">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30ec9-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30ec9-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-179">Die Adresse des Kontakts für RD-Lizenzierung.</span><span class="sxs-lookup"><span data-stu-id="30ec9-179">Street address of the contact for RD Licensing.</span></span> <span data-ttu-id="30ec9-180">Diese Eigenschaft wird verwendet, wenn die [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="30ec9-180">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="30ec9-181">(Diese Eigenschaft ist optional, wenn die **activateserverautomatic** -Methode verwendet wird.)</span><span class="sxs-lookup"><span data-stu-id="30ec9-181">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-182">**City (Ort)**</span><span class="sxs-lookup"><span data-stu-id="30ec9-182">**City**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30ec9-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30ec9-184">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-185">Stadt des Kontakts für RD-Lizenzierung.</span><span class="sxs-lookup"><span data-stu-id="30ec9-185">City of the contact for RD Licensing.</span></span> <span data-ttu-id="30ec9-186">Diese Eigenschaft wird verwendet, wenn die [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="30ec9-186">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="30ec9-187">(Diese Eigenschaft ist optional, wenn die **activateserverautomatic** -Methode verwendet wird.)</span><span class="sxs-lookup"><span data-stu-id="30ec9-187">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-188">**Company**</span><span class="sxs-lookup"><span data-stu-id="30ec9-188">**Company**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30ec9-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30ec9-190">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-191">Unternehmen des Kontakts für RD-Lizenzierung.</span><span class="sxs-lookup"><span data-stu-id="30ec9-191">Company of the contact for RD Licensing.</span></span> <span data-ttu-id="30ec9-192">Diese Eigenschaft wird verwendet (und erforderlich), wenn die [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="30ec9-192">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-193">**CountryRegion**</span><span class="sxs-lookup"><span data-stu-id="30ec9-193">**CountryRegion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30ec9-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-195">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30ec9-195">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-196">Land/Region des Kontakts für RD-Lizenzierung.</span><span class="sxs-lookup"><span data-stu-id="30ec9-196">Country/region of the contact for RD Licensing.</span></span> <span data-ttu-id="30ec9-197">Diese Eigenschaft wird verwendet (und erforderlich), wenn die [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="30ec9-197">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-198">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="30ec9-198">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30ec9-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30ec9-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-201">Der Pfad der RDS-Lizenzierungs Datenbank.</span><span class="sxs-lookup"><span data-stu-id="30ec9-201">Path of the RDS Licensing database.</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-202">**E-Mail**</span><span class="sxs-lookup"><span data-stu-id="30ec9-202">**eMail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30ec9-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-204">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30ec9-204">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-205">E-Mail-Adresse des Kontakts für RD-Lizenzierung.</span><span class="sxs-lookup"><span data-stu-id="30ec9-205">Email address of the contact for RD Licensing.</span></span> <span data-ttu-id="30ec9-206">Diese Eigenschaft wird verwendet, wenn die Methoden [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md), [**reactivateserverautomatic**](reactivateserverautomatic-win32-tslicenseserver.md)oder [**deactivateserverautomatic**](deactivateserverautomatic-win32-tslicenseserver.md) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="30ec9-206">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span> <span data-ttu-id="30ec9-207">(Diese Eigenschaft ist für diese Methodenaufrufe optional.)</span><span class="sxs-lookup"><span data-stu-id="30ec9-207">(This property is optional for these method calls.)</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-208">**Vorname**</span><span class="sxs-lookup"><span data-stu-id="30ec9-208">**FirstName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-209">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30ec9-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-210">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30ec9-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-211">Der Vorname des Kontakts für RD-Lizenzierung.</span><span class="sxs-lookup"><span data-stu-id="30ec9-211">First name of the contact for RD Licensing.</span></span> <span data-ttu-id="30ec9-212">Diese Eigenschaft wird (und erforderlich) verwendet, wenn die Methoden [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md), [**reactivateserverautomatic**](reactivateserverautomatic-win32-tslicenseserver.md)oder [**deactivateserverautomatic**](deactivateserverautomatic-win32-tslicenseserver.md) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="30ec9-212">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-213">**Nachname**</span><span class="sxs-lookup"><span data-stu-id="30ec9-213">**LastName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-214">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30ec9-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-215">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30ec9-215">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-216">Nachname des Kontakts für RD-Lizenzierung.</span><span class="sxs-lookup"><span data-stu-id="30ec9-216">Last name of the contact for RD Licensing.</span></span> <span data-ttu-id="30ec9-217">Diese Eigenschaft wird (und erforderlich) verwendet, wenn die Methoden [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md), [**reactivateserverautomatic**](reactivateserverautomatic-win32-tslicenseserver.md)oder [**deactivateserverautomatic**](deactivateserverautomatic-win32-tslicenseserver.md) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="30ec9-217">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-218">**Organisationseinheit**</span><span class="sxs-lookup"><span data-stu-id="30ec9-218">**OrgUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30ec9-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30ec9-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-221">Organisationseinheit des Kontakts für RD-Lizenzierung.</span><span class="sxs-lookup"><span data-stu-id="30ec9-221">Organizational unit of the contact for RD Licensing.</span></span> <span data-ttu-id="30ec9-222">Diese Eigenschaft wird verwendet, wenn [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="30ec9-222">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) is called.</span></span> <span data-ttu-id="30ec9-223">(Diese Eigenschaft ist optional, wenn die **activateserverautomatic** -Methode verwendet wird.)</span><span class="sxs-lookup"><span data-stu-id="30ec9-223">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-224">**PostalCode**</span><span class="sxs-lookup"><span data-stu-id="30ec9-224">**PostalCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30ec9-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30ec9-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-227">Postleitzahl des Kontakts für RD-Lizenzierung.</span><span class="sxs-lookup"><span data-stu-id="30ec9-227">Postal code of the contact for RD Licensing.</span></span> <span data-ttu-id="30ec9-228">Diese Eigenschaft wird verwendet, wenn die [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="30ec9-228">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="30ec9-229">(Diese Eigenschaft ist optional, wenn die **activateserverautomatic** -Methode verwendet wird.)</span><span class="sxs-lookup"><span data-stu-id="30ec9-229">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-230">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="30ec9-230">**ProductId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-231">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30ec9-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30ec9-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-233">Produkt-ID des Remotedesktop Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="30ec9-233">Product ID of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-234">**ServerRole**</span><span class="sxs-lookup"><span data-stu-id="30ec9-234">**ServerRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-235">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="30ec9-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30ec9-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-237">Beschreibt den Lizenzierungs Bereich für den Remotedesktop Lizenzserver innerhalb der Organisation.</span><span class="sxs-lookup"><span data-stu-id="30ec9-237">Describes the licensing scope for the Remote Desktop license server within the organization.</span></span>

<dt>

<span data-ttu-id="30ec9-238">0</span><span class="sxs-lookup"><span data-stu-id="30ec9-238">0</span></span>
</dt> <dd>

<span data-ttu-id="30ec9-239">RD-Sitzungshost Server in derselben Arbeitsgruppe können den Lizenzserver ermitteln.</span><span class="sxs-lookup"><span data-stu-id="30ec9-239">RD Session Host servers in the same workgroup can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-240">1</span><span class="sxs-lookup"><span data-stu-id="30ec9-240">1</span></span>
</dt> <dd>

<span data-ttu-id="30ec9-241">RD-Sitzungshost Server in derselben Domäne können den Lizenzserver ermitteln.</span><span class="sxs-lookup"><span data-stu-id="30ec9-241">RD Session Host servers in the same domain can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-242">2</span><span class="sxs-lookup"><span data-stu-id="30ec9-242">2</span></span>
</dt> <dd>

<span data-ttu-id="30ec9-243">RD-Sitzungshost Server aus mehreren Domänen in derselben Gesamtstruktur können den Lizenzserver ermitteln.</span><span class="sxs-lookup"><span data-stu-id="30ec9-243">RD Session Host servers from multiple domains in the same forest can discover the license server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="30ec9-244">**State**</span><span class="sxs-lookup"><span data-stu-id="30ec9-244">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-245">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30ec9-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-246">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="30ec9-246">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-247">Der Status des Kontakts für RD-Lizenzierung.</span><span class="sxs-lookup"><span data-stu-id="30ec9-247">State of the contact for RD Licensing.</span></span> <span data-ttu-id="30ec9-248">Diese Eigenschaft wird verwendet, wenn die [**activateserverautomatic**](activateserverautomatic-win32-tslicenseserver.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="30ec9-248">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="30ec9-249">(Diese Eigenschaft ist optional, wenn die **activateserverautomatic** -Methode verwendet wird.)</span><span class="sxs-lookup"><span data-stu-id="30ec9-249">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-250">**Version**</span><span class="sxs-lookup"><span data-stu-id="30ec9-250">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30ec9-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30ec9-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-253">Die Version des Remotedesktop Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="30ec9-253">Version of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="30ec9-254">**VersionNumber**</span><span class="sxs-lookup"><span data-stu-id="30ec9-254">**VersionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ec9-255">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30ec9-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ec9-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30ec9-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30ec9-257">Die Versionsnummer des Remotedesktop Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="30ec9-257">Version number of the Remote Desktop license server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30ec9-258">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30ec9-258">Remarks</span></span>

<span data-ttu-id="30ec9-259">Bei dieser Klasse handelt es sich um eine [Singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) -Klasse, die nur eine Instanz aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="30ec9-259">This class is a [singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) class and can have only one instance.</span></span> <span data-ttu-id="30ec9-260">Alle in dieser Klasse enthaltenen Methoden sind statisch.</span><span class="sxs-lookup"><span data-stu-id="30ec9-260">All of the methods contained within this class are static.</span></span>

<span data-ttu-id="30ec9-261">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="30ec9-261">You must be a member of the Administrators group to use this class.</span></span> <span data-ttu-id="30ec9-262">Wenn der Aufrufer kein Mitglied der Gruppe "Administratoren" ist, sind die zurückgegebenen Eigenschaften leer.</span><span class="sxs-lookup"><span data-stu-id="30ec9-262">If the caller is not a member of the Administrators group, the properties returned will be empty.</span></span>

<span data-ttu-id="30ec9-263">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="30ec9-263">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="30ec9-264">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="30ec9-264">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="30ec9-265">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="30ec9-265">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="30ec9-266">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="30ec9-266">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="30ec9-267">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30ec9-267">Requirements</span></span>



| <span data-ttu-id="30ec9-268">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30ec9-268">Requirement</span></span> | <span data-ttu-id="30ec9-269">Wert</span><span class="sxs-lookup"><span data-stu-id="30ec9-269">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="30ec9-270">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30ec9-270">Minimum supported client</span></span><br/> | <span data-ttu-id="30ec9-271">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="30ec9-271">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="30ec9-272">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30ec9-272">Minimum supported server</span></span><br/> | <span data-ttu-id="30ec9-273">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30ec9-273">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="30ec9-274">Namespace</span><span class="sxs-lookup"><span data-stu-id="30ec9-274">Namespace</span></span><br/>                | <span data-ttu-id="30ec9-275">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="30ec9-275">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="30ec9-276">MOF</span><span class="sxs-lookup"><span data-stu-id="30ec9-276">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30ec9-277"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="30ec9-277"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="30ec9-278">DLL</span><span class="sxs-lookup"><span data-stu-id="30ec9-278">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30ec9-279"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30ec9-279"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30ec9-280">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30ec9-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ec9-281">**Win32-" \_ tsissuedlicense"**</span><span class="sxs-lookup"><span data-stu-id="30ec9-281">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="30ec9-282">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="30ec9-282">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="30ec9-283">**Win32-Datei- \_ /licensereport**</span><span class="sxs-lookup"><span data-stu-id="30ec9-283">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="30ec9-284">**Win32-Wert für "- \_ Lizenzserver"**</span><span class="sxs-lookup"><span data-stu-id="30ec9-284">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> </dl>

 


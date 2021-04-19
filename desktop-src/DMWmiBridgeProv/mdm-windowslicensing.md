---
title: MDM_WindowsLicensing-Klasse
description: Die MDM- \_ windowslicensing-Klasse ist für Lizenzierungs bezogene Verwaltungs Szenarien konzipiert.
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- MDM_WindowsLicensing-Klasse
- MDM_WindowsLicensing-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing
- MDM_WindowsLicensing.InstanceID
- MDM_WindowsLicensing.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd77bbdb1a7e5c708ebcd955a0c8854c7c7404b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341791"
---
# <a name="mdm_windowslicensing-class"></a><span data-ttu-id="91fba-105">MDM- \_ windowslicensing-Klasse</span><span class="sxs-lookup"><span data-stu-id="91fba-105">MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="91fba-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="91fba-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="91fba-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="91fba-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="91fba-108">Die **MDM- \_ windowslicensing** -Klasse ist für Lizenzierungs bezogene Verwaltungs Szenarien konzipiert.</span><span class="sxs-lookup"><span data-stu-id="91fba-108">The **MDM\_WindowsLicensing** class is designed for licensing related management scenarios.</span></span> <span data-ttu-id="91fba-109">Derzeit ist der Bereich auf Editions Upgrades von Windows 10-Desktop Computern und mobilen Geräten wie Windows 10 pro auf Windows 10 Enterprise beschränkt.</span><span class="sxs-lookup"><span data-stu-id="91fba-109">Currently the scope is limited to edition upgrades of Windows 10 desktop and mobile devices, such as Windows 10 Pro to Windows 10 Enterprise.</span></span> <span data-ttu-id="91fba-110">Außerdem bietet dieser CSP die Möglichkeit, die Product Key von Windows 10-Desktop Geräten zu aktivieren oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="91fba-110">In addition, this CSP provides the capability to activate or change the product key of Windows 10 desktop devices.</span></span>

<span data-ttu-id="91fba-111">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="91fba-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="91fba-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="91fba-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing
{
  string InstanceID;
  string ParentID;
  sint32 Edition;
  sint32 Status;
  string LicenseKeyType;
};
```

## <a name="members"></a><span data-ttu-id="91fba-113">Member</span><span class="sxs-lookup"><span data-stu-id="91fba-113">Members</span></span>

<span data-ttu-id="91fba-114">Die **MDM \_ windowslicensing** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="91fba-114">The **MDM\_WindowsLicensing** class has these types of members:</span></span>

-   [<span data-ttu-id="91fba-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="91fba-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="91fba-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91fba-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="91fba-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="91fba-117">Methods</span></span>

<span data-ttu-id="91fba-118">Die **MDM \_ windowslicensing** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="91fba-118">The **MDM\_WindowsLicensing** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="91fba-119">Methode</span><span class="sxs-lookup"><span data-stu-id="91fba-119">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="91fba-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91fba-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="91fba-121"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>Changeproductkeymethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="91fba-121"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="91fba-122">Installiert eine Product Key für Windows 10 Desktop-Geräte.</span><span class="sxs-lookup"><span data-stu-id="91fba-122">Installs a product key for Windows 10 desktop devices.</span></span> <span data-ttu-id="91fba-123">Wird nicht neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="91fba-123">Does not reboot.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="91fba-124"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>Checkapplicabilitymethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="91fba-124"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="91fba-125">Methode, um zu überprüfen, ob der eingegebene Product Key für ein Editions Upgrade, eine Aktivierung oder Änderung eines Product Key von Windows 10 für Desktop Geräte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="91fba-125">Method to check if the entered product key can be used for an edition upgrade, activation or changing a product key of Windows 10 for desktop devices.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="91fba-126"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>Upgradeeditionwithlicenermethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="91fba-126"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="91fba-127">Stellen Sie eine Lizenz für ein Editions Upgrade von Windows 10 Mobile-Geräten bereit.</span><span class="sxs-lookup"><span data-stu-id="91fba-127">Provide a license for an edition upgrade of Windows 10 mobile devices.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="91fba-128">Für diesen Upgradevorgang ist kein Systemneustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="91fba-128">This upgrade process does not require a system restart.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="91fba-129">Der Date-Typ ist "XML".</span><span class="sxs-lookup"><span data-stu-id="91fba-129">The date type is XML.</span></span><br/> <span data-ttu-id="91fba-130">Der unterstützte Vorgang ist "Execute".</span><span class="sxs-lookup"><span data-stu-id="91fba-130">The supported operation is Execute.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="91fba-131">Der Inhalt der XML-Lizenzdatei muss ordnungsgemäß mit Escapezeichen versehen werden (d. h. es sollte nicht einfach ein kopierter XML-Code sein). andernfalls tritt bei der Editions Aktualisierung auf Windows 10 Mobile-Geräten</span><span class="sxs-lookup"><span data-stu-id="91fba-131">The XML license file contents must be properly escaped (that is, it should not simply be a copied XML), otherwise the edition upgrade on Windows 10 mobile devices will fail.</span></span> <span data-ttu-id="91fba-132">Weitere Informationen zum ordnungsgemäßen Escapezeichen der XML-Lizenzdatei finden Sie im Abschnitt 2,4 der <a href="https://www.w3.org/TR/xml/">W3C-XML-Spezifikation</a>. Die XML-Lizenzdatei wird vom Microsoft Volume Licensing Service Center abgerufen.</span><span class="sxs-lookup"><span data-stu-id="91fba-132">For more information on proper escaping of the XML license file, see Section 2.4 of the <a href="https://www.w3.org/TR/xml/">W3C XML spec</a>. The XML license file is acquired from the Microsoft Volume Licensing Service Center.</span></span> <span data-ttu-id="91fba-133">Ihre Organisation muss über einen Volumenlizenzvertrag mit Microsoft verfügen, um auf das Portal zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="91fba-133">Your organization must have a Volume Licensing contract with Microsoft to access the portal.</span></span>
</blockquote>
<br/> <span data-ttu-id="91fba-134">Im folgenden sind gültige Editions Upgradepfade aufgeführt, wenn dieser Knoten über ein MDM-oder Bereitstellungs Paket verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="91fba-134">The following are valid edition upgrade paths when using this node through an MDM or provisioning package:</span></span>
<ul>
<li><span data-ttu-id="91fba-135">Windows 10 mobileto Windows 10 Mobile Enterprise</span><span class="sxs-lookup"><span data-stu-id="91fba-135">Windows 10 Mobileto Windows 10 Mobile Enterprise</span></span><br/></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="91fba-136"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>Upgradeeditionwithproductkeymethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="91fba-136"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="91fba-137">Hiermit wird das Gerät ausgelöst, um die Product Key zu übernehmen und die Edition des Clients zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="91fba-137">Triggers the device to take the product key and upgrade the edition of the client.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="91fba-138">Dieser Upgradevorgang erfordert einen Systemneustart.</span><span class="sxs-lookup"><span data-stu-id="91fba-138">This upgrade process requires a system restart.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="91fba-139">Der unterstützte Vorgang ist "Execute".</span><span class="sxs-lookup"><span data-stu-id="91fba-139">The supported operation is Execute.</span></span><br/> <span data-ttu-id="91fba-140">Wenn ein Product Key von einem MDM-Server an das Gerät eines Benutzers übermittelt wird, wird <strong>changepk.exe</strong> mithilfe der Product Key ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91fba-140">When a product key is pushed from an MDM server to a user's device, <strong>changepk.exe</strong> runs using the product key.</span></span> <span data-ttu-id="91fba-141">Nachdem der Vorgang abgeschlossen ist, wird dem Benutzer eine Benachrichtigung angezeigt, dass eine neue Edition von Windows 10 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="91fba-141">After it completes, a notification is shown to the user that a new edition of Windows 10 is available.</span></span> <span data-ttu-id="91fba-142">Der Benutzer kann dann das System manuell neu starten, oder nach zwei Stunden wird das Gerät automatisch neu gestartet, um das Upgrade abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="91fba-142">The user can then restart their system manually or, after two hours, the device will restart automatically to complete the upgrade.</span></span> <span data-ttu-id="91fba-143">Der Benutzer erhält eine Erinnerungs Benachrichtigung 10 Minuten vor dem automatischen Neustart.</span><span class="sxs-lookup"><span data-stu-id="91fba-143">The user will receive a reminder notification 10 minutes before the automatic restart.</span></span><br/> <span data-ttu-id="91fba-144">Nachdem das Gerät neu gestartet wurde, wird der Editions Upgradevorgang abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="91fba-144">After the device restarts, the edition upgrade process completes.</span></span> <span data-ttu-id="91fba-145">Der Benutzer erhält eine Benachrichtigung über das erfolgreiche Upgrade.</span><span class="sxs-lookup"><span data-stu-id="91fba-145">The user will receive a notification of the successful upgrade.</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="91fba-146">Wenn eine andere Richtlinie einen Systemneustart erfordert, der auftritt, wenn <strong>changepk.exe</strong> ausgeführt wird, kann das Editions Upgrade nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="91fba-146">If another policy requires a system reboot that occurs when <strong>changepk.exe</strong> is running, the edition upgrade will fail.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="91fba-147">Wenn ein Product Key in einem Bereitstellungs Paket eingegeben wird und der Benutzer mit der Installation des Pakets beginnt, wird dem Benutzer eine Benachrichtigung angezeigt, dass das System neu gestartet wird, um die Paketinstallation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="91fba-147">If a product key is entered in a provisioning package and the user begins installation of the package, a notification is shown to the user that their system will restart to complete the package installation.</span></span> <span data-ttu-id="91fba-148">Nach der expliziten Zustimmung des Benutzers, um den Vorgang fortzusetzen, setzt das Paket die Installation fort und <strong>changepk.exe</strong> mithilfe des Product Key ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91fba-148">Upon explicit consent from the user to proceed, the package continues installation and <strong>changepk.exe</strong> runs using the product key.</span></span> <span data-ttu-id="91fba-149">Der Benutzer erhält eine Erinnerungs Benachrichtigung 30 Sekunden vor dem automatischen Neustart.</span><span class="sxs-lookup"><span data-stu-id="91fba-149">The user will receive a reminder notification 30 seconds before the automatic restart.</span></span> <br/> <span data-ttu-id="91fba-150">Nachdem das Gerät neu gestartet wurde, wird der Editions Upgradevorgang abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="91fba-150">After the device restarts, the edition upgrade process completes.</span></span> <span data-ttu-id="91fba-151">Der Benutzer erhält eine Benachrichtigung über das erfolgreiche Upgrade.</span><span class="sxs-lookup"><span data-stu-id="91fba-151">The user will receive a notification of the successful upgrade.</span></span> <br/> <span data-ttu-id="91fba-152">Dieser Knoten kann auch verwendet werden, um eine Product Key einer bestimmten Edition des Windows 10-Desktop Geräts zu aktivieren oder zu ändern, indem Sie eine Product Key eingeben.</span><span class="sxs-lookup"><span data-stu-id="91fba-152">This node can also be used to activate or change a product key on a particular edition of Windows 10 desktop device by entering a product key.</span></span> <span data-ttu-id="91fba-153">Für das Aktivieren oder Ändern einer Product Key ist kein Neustart erforderlich, und es handelt sich um einen unbeaufsichtigten Prozess für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="91fba-153">Activation or changing a product key does not require a reboot and is a silent process for the user.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="91fba-154">Der eingegebene Product Key muss 29 Zeichen umfassen (d. h., er sollte Bindestriche enthalten), andernfalls tritt bei der Aktivierung, dem Editions Upgrade oder der Product Key Änderung auf Windows 10-Desktop Geräten ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="91fba-154">The product key entered must be 29 characters (that is, it should include dashes), otherwise the activation, edition upgrade, or product key change on Windows 10 desktop devices will fail.</span></span> <span data-ttu-id="91fba-155">Der Product Key wird von Microsoft Volume Licensing Service Center abgerufen.</span><span class="sxs-lookup"><span data-stu-id="91fba-155">The product key is acquired from Microsoft Volume Licensing Service Center.</span></span> <span data-ttu-id="91fba-156">Ihre Organisation muss über einen Volumenlizenzvertrag mit Microsoft verfügen, um auf das Portal zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="91fba-156">Your organization must have a Volume Licensing contract with Microsoft to access the portal.</span></span>
</blockquote>
<br/> <span data-ttu-id="91fba-157">Im folgenden finden Sie gültige Editions Upgradepfade, wenn dieser Knoten über eine MDM verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="91fba-157">The following are valid edition upgrade paths when using this node through an MDM:</span></span>
<ul>
<li><span data-ttu-id="91fba-158">Windows 10 Enterprise zu Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="91fba-158">Windows 10 Enterprise to Windows 10 Education</span></span></li>
<li><span data-ttu-id="91fba-159">Windows 10 Home zu Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="91fba-159">Windows 10 Home to Windows 10 Education</span></span></li>
<li><span data-ttu-id="91fba-160">Windows 10 pro zu Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="91fba-160">Windows 10 Pro to Windows 10 Education</span></span></li>
<li><span data-ttu-id="91fba-161">Windows 10 pro zu Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="91fba-161">Windows 10 Pro to Windows 10 Enterprise</span></span></li>
</ul>
<br/> <span data-ttu-id="91fba-162">Die Aktivierung oder Änderung einer Product Key kann für die folgenden Editionen ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="91fba-162">Activation or changing a product key can be carried out on the following editions:</span></span>
<ul>
<li><span data-ttu-id="91fba-163">Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="91fba-163">Windows 10 Education</span></span></li>
<li><span data-ttu-id="91fba-164">Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="91fba-164">Windows 10 Enterprise</span></span></li>
<li><span data-ttu-id="91fba-165">Windows 10 Home</span><span class="sxs-lookup"><span data-stu-id="91fba-165">Windows 10 Home</span></span></li>
<li><span data-ttu-id="91fba-166">Windows 10 Pro</span><span class="sxs-lookup"><span data-stu-id="91fba-166">Windows 10 Pro</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="91fba-167">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91fba-167">Properties</span></span>

<span data-ttu-id="91fba-168">Die **MDM- \_ windowslicensing** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="91fba-168">The **MDM\_WindowsLicensing** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="91fba-169">Edition</span><span class="sxs-lookup"><span data-stu-id="91fba-169">Edition</span></span>](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91fba-170">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91fba-170">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91fba-171">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91fba-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="91fba-172">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="91fba-172">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91fba-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91fba-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91fba-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91fba-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91fba-175">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="91fba-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="91fba-176">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="91fba-176">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="91fba-177">Licentkeytype</span><span class="sxs-lookup"><span data-stu-id="91fba-177">LicenseKeyType</span></span>](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91fba-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91fba-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91fba-179">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91fba-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="91fba-180">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="91fba-180">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91fba-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91fba-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91fba-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91fba-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91fba-183">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="91fba-183">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="91fba-184">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="91fba-184">Describes the full path to the parent node.</span></span> <span data-ttu-id="91fba-185">Für diese Klasse ist die Zeichenfolge "./Vendor/msft/".</span><span class="sxs-lookup"><span data-stu-id="91fba-185">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="91fba-186">Status</span><span class="sxs-lookup"><span data-stu-id="91fba-186">Status</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91fba-187">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="91fba-187">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="91fba-188">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="91fba-188">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91fba-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91fba-189">Requirements</span></span>



| <span data-ttu-id="91fba-190">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91fba-190">Requirement</span></span> | <span data-ttu-id="91fba-191">Wert</span><span class="sxs-lookup"><span data-stu-id="91fba-191">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91fba-192">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91fba-192">Minimum supported client</span></span><br/> | <span data-ttu-id="91fba-193">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91fba-193">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="91fba-194">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91fba-194">Minimum supported server</span></span><br/> | <span data-ttu-id="91fba-195">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="91fba-195">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="91fba-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="91fba-196">Namespace</span></span><br/>                | <span data-ttu-id="91fba-197">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="91fba-197">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="91fba-198">MOF</span><span class="sxs-lookup"><span data-stu-id="91fba-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91fba-199"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="91fba-199"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="91fba-200">DLL</span><span class="sxs-lookup"><span data-stu-id="91fba-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91fba-201"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91fba-201"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91fba-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91fba-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91fba-203">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="91fba-203">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


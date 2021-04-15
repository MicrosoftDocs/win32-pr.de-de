---
title: Win32_TSLogonSetting-Klasse
description: Definiert Konfigurationseinstellungen für die Win32- \_ Terminal Klasse im Zusammenhang mit der Client Anmeldung.
ms.assetid: a2ccb419-da1a-44d1-8a7a-4d0266fc1be8
ms.tgt_platform: multiple
keywords:
- Win32_TSLogonSetting-Klasse Remotedesktopdienste
- Win32_TSLogonSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting
- Win32_TSLogonSetting.Caption
- Win32_TSLogonSetting.Description
- Win32_TSLogonSetting.InstallDate
- Win32_TSLogonSetting.Name
- Win32_TSLogonSetting.Status
- Win32_TSLogonSetting.TerminalName
- Win32_TSLogonSetting.ClientLogonInfoPolicy
- Win32_TSLogonSetting.Domain
- Win32_TSLogonSetting.Password
- Win32_TSLogonSetting.PolicySourceDomain
- Win32_TSLogonSetting.PolicySourcePromptForPassword
- Win32_TSLogonSetting.PolicySourceUserName
- Win32_TSLogonSetting.PromptForPassword
- Win32_TSLogonSetting.UserName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e656f3913bb7320253dc9dbca6710f37e0cbdded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392061"
---
# <a name="win32_tslogonsetting-class"></a><span data-ttu-id="8dacc-105">Win32- \_ Klasse "Klasse-logonsetting"</span><span class="sxs-lookup"><span data-stu-id="8dacc-105">Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="8dacc-106">Die Win32-Klasse "t- **\_ logonsetting** " definiert Konfigurationseinstellungen für die [**Win32- \_ Terminal**](win32-terminal.md) Klasse, die sich auf die Client Anmeldung bezieht.</span><span class="sxs-lookup"><span data-stu-id="8dacc-106">The **Win32\_TSLogonSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to client logon.</span></span>

<span data-ttu-id="8dacc-107">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="8dacc-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="8dacc-108">Referenzinformationen zu-Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="8dacc-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dacc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dacc-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSLOGONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSLogonSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientLogonInfoPolicy;
  string   Domain;
  string   Password;
  uint32   PolicySourceDomain;
  uint32   PolicySourcePromptForPassword;
  uint32   PolicySourceUserName;
  uint32   PromptForPassword;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="8dacc-110">Member</span><span class="sxs-lookup"><span data-stu-id="8dacc-110">Members</span></span>

<span data-ttu-id="8dacc-111">Die Win32-Klasse " **\_ tylogonsetting** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8dacc-111">The **Win32\_TSLogonSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="8dacc-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="8dacc-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="8dacc-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8dacc-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8dacc-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="8dacc-114">Methods</span></span>

<span data-ttu-id="8dacc-115">Die Win32-Klasse " **\_ zlogonsetting** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8dacc-115">The **Win32\_TSLogonSetting** class has these methods.</span></span>



| <span data-ttu-id="8dacc-116">Methode</span><span class="sxs-lookup"><span data-stu-id="8dacc-116">Method</span></span>                                                                    | <span data-ttu-id="8dacc-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8dacc-117">Description</span></span>                                                                    |
|:--------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="8dacc-118">**Explitlogon**</span><span class="sxs-lookup"><span data-stu-id="8dacc-118">**ExplicitLogon**</span></span>](win32-tslogonsetting-explicitlogon.md)               | <span data-ttu-id="8dacc-119">Legt die Anmelde Informationen für Benutzername, Kennwort und Domäne fest.</span><span class="sxs-lookup"><span data-stu-id="8dacc-119">Sets the UserName, Password, and Domain authentication credentials.</span></span><br/> |
| [<span data-ttu-id="8dacc-120">**Setpromptforpassword**</span><span class="sxs-lookup"><span data-stu-id="8dacc-120">**SetPromptForPassword**</span></span>](win32-tslogonsetting-setpromptforpassword.md) | <span data-ttu-id="8dacc-121">Legt die **PromptForPassword** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="8dacc-121">Sets the **PromptForPassword** property.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="8dacc-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8dacc-122">Properties</span></span>

<span data-ttu-id="8dacc-123">Die Win32-Klasse "t- **\_ logonsetting** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8dacc-123">The **Win32\_TSLogonSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8dacc-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8dacc-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dacc-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dacc-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dacc-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-127">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8dacc-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8dacc-128">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8dacc-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="8dacc-129">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dacc-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dacc-130">**ClientLogonInfoPolicy**</span><span class="sxs-lookup"><span data-stu-id="8dacc-130">**ClientLogonInfoPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dacc-131">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8dacc-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dacc-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8dacc-133">Die Richtlinie, die der Server zum Bestimmen der Verbindungseinstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8dacc-133">The policy the server uses to determine connection settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="8dacc-134"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Pro Benutzer** (0)</span><span class="sxs-lookup"><span data-stu-id="8dacc-134"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8dacc-135">Die einzelnen Benutzer Verbindungseinstellungen sind in Kraft.</span><span class="sxs-lookup"><span data-stu-id="8dacc-135">Individual user connection settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="8dacc-136"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-override** (1)</span><span class="sxs-lookup"><span data-stu-id="8dacc-136"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8dacc-137">Die einzelnen Benutzer Verbindungseinstellungen werden vom Server überschrieben.</span><span class="sxs-lookup"><span data-stu-id="8dacc-137">Individual user connection settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8dacc-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8dacc-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dacc-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dacc-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dacc-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dacc-141">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8dacc-141">Description of the object.</span></span>

<span data-ttu-id="8dacc-142">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dacc-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dacc-143">**Domäne**</span><span class="sxs-lookup"><span data-stu-id="8dacc-143">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dacc-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dacc-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dacc-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dacc-146">Anmelde Informationen für die Domänen Anmelde Authentifizierung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="8dacc-146">The user's domain logon authentication credential.</span></span> <span data-ttu-id="8dacc-147">Dies ist die Domäne, in der sich der Computer des Benutzers befindet.</span><span class="sxs-lookup"><span data-stu-id="8dacc-147">This is the domain in which the user's computer resides.</span></span> <span data-ttu-id="8dacc-148">Diese Eigenschaft darf nicht länger als 17 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="8dacc-148">This property cannot be longer than 17 characters.</span></span>

</dd> <dt>

<span data-ttu-id="8dacc-149">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8dacc-149">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dacc-150">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8dacc-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dacc-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-152">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="8dacc-152">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="8dacc-153">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8dacc-153">The date the object was installed.</span></span> <span data-ttu-id="8dacc-154">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8dacc-154">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8dacc-155">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dacc-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dacc-156">**Name**</span><span class="sxs-lookup"><span data-stu-id="8dacc-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dacc-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dacc-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dacc-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dacc-159">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8dacc-159">The name of the object.</span></span>

<span data-ttu-id="8dacc-160">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dacc-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dacc-161">**Kennwort**</span><span class="sxs-lookup"><span data-stu-id="8dacc-161">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dacc-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dacc-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dacc-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dacc-164">Anmelde Informationen für die Authentifizierung der Anmelde Informationen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="8dacc-164">The user's password logon authentication credential.</span></span> <span data-ttu-id="8dacc-165">Diese Eigenschaft darf nicht länger als 14 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="8dacc-165">This property cannot be longer than 14 characters.</span></span> <span data-ttu-id="8dacc-166">Es wird empfohlen, die Sicherheitsstufe auf Paket Datenschutz (wbemauthenticationlevelpktprivacy = 6) festzulegen, wenn Sie diese Eigenschaft Abfragen.</span><span class="sxs-lookup"><span data-stu-id="8dacc-166">It is recommended that you set the security level to packet privacy (wbemAuthenticationLevelPktPrivacy = 6) if you query this property.</span></span> <span data-ttu-id="8dacc-167">Dies liegt daran, dass das Kennwort nicht über das Netzwerk verschlüsselt wird, ohne diese Sicherheitsebene zu haben.</span><span class="sxs-lookup"><span data-stu-id="8dacc-167">This is because the password is not encrypted on the wire without this level of security.</span></span> <span data-ttu-id="8dacc-168">Weitere Informationen zum Festlegen von Sicherheitsstufen finden Sie unter [Festlegen der Prozesssicherheit für Client Anwendungen](/windows/desktop/WmiSdk/setting-client-application-process-security) in der WMI SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="8dacc-168">For more information about setting security levels, see [Setting Client Application Process Security](/windows/desktop/WmiSdk/setting-client-application-process-security) in the WMI SDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="8dacc-169">**Policysourcedomain**</span><span class="sxs-lookup"><span data-stu-id="8dacc-169">**PolicySourceDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dacc-170">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8dacc-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dacc-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dacc-172">Gibt an, ob die **Domänen** Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="8dacc-172">Indicates whether the **Domain** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8dacc-173">0</span><span class="sxs-lookup"><span data-stu-id="8dacc-173">0</span></span>
</dt> <dd>

<span data-ttu-id="8dacc-174">Server</span><span class="sxs-lookup"><span data-stu-id="8dacc-174">Server</span></span>

</dd> <dt>

<span data-ttu-id="8dacc-175">1</span><span class="sxs-lookup"><span data-stu-id="8dacc-175">1</span></span>
</dt> <dd>

<span data-ttu-id="8dacc-176">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="8dacc-176">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8dacc-177">2</span><span class="sxs-lookup"><span data-stu-id="8dacc-177">2</span></span>
</dt> <dd>

<span data-ttu-id="8dacc-178">Standard</span><span class="sxs-lookup"><span data-stu-id="8dacc-178">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8dacc-179">**PolicySourcePromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="8dacc-179">**PolicySourcePromptForPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dacc-180">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8dacc-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dacc-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dacc-182">Gibt an, ob die **PromptForPassword** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="8dacc-182">Indicates whether the **PromptForPassword** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8dacc-183">0</span><span class="sxs-lookup"><span data-stu-id="8dacc-183">0</span></span>
</dt> <dd>

<span data-ttu-id="8dacc-184">Server</span><span class="sxs-lookup"><span data-stu-id="8dacc-184">Server</span></span>

</dd> <dt>

<span data-ttu-id="8dacc-185">1</span><span class="sxs-lookup"><span data-stu-id="8dacc-185">1</span></span>
</dt> <dd>

<span data-ttu-id="8dacc-186">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="8dacc-186">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8dacc-187">2</span><span class="sxs-lookup"><span data-stu-id="8dacc-187">2</span></span>
</dt> <dd>

<span data-ttu-id="8dacc-188">Standard</span><span class="sxs-lookup"><span data-stu-id="8dacc-188">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8dacc-189">**Policysourceusername**</span><span class="sxs-lookup"><span data-stu-id="8dacc-189">**PolicySourceUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dacc-190">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8dacc-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dacc-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dacc-192">Gibt an, ob die **username** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="8dacc-192">Indicates whether the **UserName** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8dacc-193">0</span><span class="sxs-lookup"><span data-stu-id="8dacc-193">0</span></span>
</dt> <dd>

<span data-ttu-id="8dacc-194">Server</span><span class="sxs-lookup"><span data-stu-id="8dacc-194">Server</span></span>

</dd> <dt>

<span data-ttu-id="8dacc-195">1</span><span class="sxs-lookup"><span data-stu-id="8dacc-195">1</span></span>
</dt> <dd>

<span data-ttu-id="8dacc-196">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="8dacc-196">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8dacc-197">2</span><span class="sxs-lookup"><span data-stu-id="8dacc-197">2</span></span>
</dt> <dd>

<span data-ttu-id="8dacc-198">Standard</span><span class="sxs-lookup"><span data-stu-id="8dacc-198">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8dacc-199">**PromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="8dacc-199">**PromptForPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dacc-200">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8dacc-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dacc-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dacc-202">Gibt an, ob der Benutzer bei der Anmeldung am Server immer zur Eingabe eines Kennworts aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="8dacc-202">Specifies whether the user is always prompted for a password while logging into the server.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8dacc-203"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8dacc-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8dacc-204">Der Benutzer wird nicht zur Eingabe eines Kennworts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8dacc-204">The user is not prompted for a password.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8dacc-205"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8dacc-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8dacc-206">Der Benutzer wird zur Eingabe eines Kennworts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8dacc-206">The user is prompted for a password.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8dacc-207">**Status**</span><span class="sxs-lookup"><span data-stu-id="8dacc-207">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dacc-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dacc-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dacc-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-210">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="8dacc-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="8dacc-211">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8dacc-211">Current status of the object.</span></span> <span data-ttu-id="8dacc-212">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="8dacc-212">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8dacc-213">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="8dacc-213">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8dacc-214">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="8dacc-214">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8dacc-215">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8dacc-215">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8dacc-216">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="8dacc-216">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8dacc-217">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dacc-217">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="8dacc-218">("OK")</span><span class="sxs-lookup"><span data-stu-id="8dacc-218">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8dacc-219">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="8dacc-219">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8dacc-220">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="8dacc-220">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8dacc-221">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="8dacc-221">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8dacc-222">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8dacc-222">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8dacc-223">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="8dacc-223">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8dacc-224">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="8dacc-224">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8dacc-225">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="8dacc-225">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8dacc-226">**Terminal Name**</span><span class="sxs-lookup"><span data-stu-id="8dacc-226">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dacc-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dacc-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dacc-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dacc-229">Der Name des Terminals.</span><span class="sxs-lookup"><span data-stu-id="8dacc-229">The name of the terminal.</span></span>

<span data-ttu-id="8dacc-230">Diese Eigenschaft wird von [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8dacc-230">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dacc-231">**UserName**</span><span class="sxs-lookup"><span data-stu-id="8dacc-231">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dacc-232">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dacc-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dacc-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dacc-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dacc-234">Anmelde Informationen für die Anmelde Authentifizierung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="8dacc-234">The user's user name logon authentication credential.</span></span> <span data-ttu-id="8dacc-235">Diese Eigenschaft darf nicht länger als 20 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="8dacc-235">This property cannot be longer than 20 characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8dacc-236">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8dacc-236">Remarks</span></span>

<span data-ttu-id="8dacc-237">Beachten Sie, dass die der Konsolen Sitzung zugeordneten Winstations nicht auf die Methoden und Eigenschaften dieser Klasse zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="8dacc-237">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="8dacc-238">Wenn ein Versuch unternommen wird, indem "Console" als Wert der Terminalname-Eigenschaft angegeben wird, geben die Methoden dieses Objekts **WBEM \_ E \_ nicht \_ unterstützt** zurück.</span><span class="sxs-lookup"><span data-stu-id="8dacc-238">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="8dacc-239">Dieser Fehlercode wird zurückgegeben, wenn eine Fenster Station versucht, Methoden dieses Objekts aufzurufen, um die Sicherheitseigenschaften der Konten "LocalSystem", "LocalService" oder "Network Service" hinzuzufügen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8dacc-239">This error code is returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="8dacc-240">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="8dacc-240">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="8dacc-241">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="8dacc-241">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="8dacc-242">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="8dacc-242">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="8dacc-243">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8dacc-243">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="8dacc-244">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="8dacc-244">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8dacc-245">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="8dacc-245">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8dacc-246">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8dacc-246">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8dacc-247">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8dacc-247">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8dacc-248">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8dacc-248">Requirements</span></span>



| <span data-ttu-id="8dacc-249">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8dacc-249">Requirement</span></span> | <span data-ttu-id="8dacc-250">Wert</span><span class="sxs-lookup"><span data-stu-id="8dacc-250">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8dacc-251">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8dacc-251">Minimum supported client</span></span><br/> | <span data-ttu-id="8dacc-252">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8dacc-252">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8dacc-253">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8dacc-253">Minimum supported server</span></span><br/> | <span data-ttu-id="8dacc-254">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8dacc-254">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8dacc-255">Namespace</span><span class="sxs-lookup"><span data-stu-id="8dacc-255">Namespace</span></span><br/>                | <span data-ttu-id="8dacc-256">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8dacc-256">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8dacc-257">MOF</span><span class="sxs-lookup"><span data-stu-id="8dacc-257">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8dacc-258"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8dacc-258"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8dacc-259">DLL</span><span class="sxs-lookup"><span data-stu-id="8dacc-259">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8dacc-260"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8dacc-260"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dacc-261">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dacc-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dacc-262">**Win32- \_ Terminal**</span><span class="sxs-lookup"><span data-stu-id="8dacc-262">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="8dacc-263">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="8dacc-263">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 


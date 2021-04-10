---
title: Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Beschreibt eine Remotedesktop Ressourcen Autorisierungs Richtlinie (RD \ 160; Rap). A RD \ 160; Rap wird verwendet, um zu entscheiden, ob ein Benutzer autorisiert ist, über Remotedesktop Gateway (RD-Gateway) eine Verbindung mit einer angegebenen Ressource herzustellen.
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceAuthorizationPolicy-Klasse Remotedesktopdienste
- Win32_TSGatewayResourceAuthorizationPolicy Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy.Name
- Win32_TSGatewayResourceAuthorizationPolicy.Description
- Win32_TSGatewayResourceAuthorizationPolicy.Enabled
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupType
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupName
- Win32_TSGatewayResourceAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayResourceAuthorizationPolicy.ProtocolNames
- Win32_TSGatewayResourceAuthorizationPolicy.PortNumbers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c262cb1ce3351c89dc5d7edf3b0d106116e83b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040530"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="e3778-106">Win32-Klasse "t- \_ gatewayresourceauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="e3778-106">Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="e3778-107">Beschreibt eine Remotedesktop-Ressourcen Autorisierungs Richtlinie (RD-RAP).</span><span class="sxs-lookup"><span data-stu-id="e3778-107">Describes a Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="e3778-108">Eine RD-RAP wird verwendet, um zu entscheiden, ob ein Benutzer autorisiert ist, über Remotedesktop Gateway (RD-Gateway) eine Verbindung mit einer angegebenen Ressource herzustellen.</span><span class="sxs-lookup"><span data-stu-id="e3778-108">An RD RAP is used to decide whether a user is authorized to connect to a specified resource through Remote Desktop Gateway (RD Gateway).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3778-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3778-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceAuthorizationPolicy
{
  string  Name;
  string  Description;
  boolean Enabled;
  string  ResourceGroupType;
  string  ResourceGroupName;
  string  UserGroupNames;
  string  ProtocolNames;
  string  PortNumbers;
};
```

## <a name="members"></a><span data-ttu-id="e3778-110">Member</span><span class="sxs-lookup"><span data-stu-id="e3778-110">Members</span></span>

<span data-ttu-id="e3778-111">Die Win32-Klasse " **\_ zgatewayresourceauthorizationpolicy** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e3778-111">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these types of members:</span></span>

-   [<span data-ttu-id="e3778-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="e3778-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="e3778-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3778-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e3778-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="e3778-114">Methods</span></span>

<span data-ttu-id="e3778-115">Die Win32-Klasse " **\_ zgatewayresourceauthorizationpolicy** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e3778-115">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these methods.</span></span>



| <span data-ttu-id="e3778-116">Methode</span><span class="sxs-lookup"><span data-stu-id="e3778-116">Method</span></span>                                                                                          | <span data-ttu-id="e3778-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3778-117">Description</span></span>                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3778-118">**Addusergroupnames**</span><span class="sxs-lookup"><span data-stu-id="e3778-118">**AddUserGroupNames**</span></span>](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | <span data-ttu-id="e3778-119">Fügt die angegebenen Benutzergruppen Namen den vorhandenen Benutzergruppen in der **usergroupnames** -Eigenschaft hinzu.</span><span class="sxs-lookup"><span data-stu-id="e3778-119">Adds the specified user group names to the existing user groups in the **UserGroupNames** property.</span></span><br/>      |
| [<span data-ttu-id="e3778-120">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="e3778-120">**Create**</span></span>](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="e3778-121">Erstellt eine RD-RAP.</span><span class="sxs-lookup"><span data-stu-id="e3778-121">Creates an RD RAP.</span></span><br/>                                                                                       |
| [<span data-ttu-id="e3778-122">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="e3778-122">**Delete**</span></span>](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="e3778-123">Löscht die aktuelle RD-RAP.</span><span class="sxs-lookup"><span data-stu-id="e3778-123">Deletes the current RD RAP.</span></span><br/>                                                                              |
| [<span data-ttu-id="e3778-124">**Removeusergroupnames**</span><span class="sxs-lookup"><span data-stu-id="e3778-124">**RemoveUserGroupNames**</span></span>](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | <span data-ttu-id="e3778-125">Entfernt die angegebenen Benutzergruppen Namen aus den vorhandenen Benutzergruppen in der **usergroupnames** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e3778-125">Removes the specified user group names from the existing user groups in the **UserGroupNames** property.</span></span><br/> |
| [<span data-ttu-id="e3778-126">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="e3778-126">**SetDescription**</span></span>](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | <span data-ttu-id="e3778-127">Legt die **Description** -Eigenschaft für die RD-RAP fest.</span><span class="sxs-lookup"><span data-stu-id="e3778-127">Sets the **Description** property for the RD RAP.</span></span><br/>                                                        |
| [<span data-ttu-id="e3778-128">**Abgeleitete**</span><span class="sxs-lookup"><span data-stu-id="e3778-128">**SetEnabled**</span></span>](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | <span data-ttu-id="e3778-129">Aktiviert oder deaktiviert die RD-RAP durch Festlegen der **aktivierten** Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e3778-129">Enables or disables the RD RAP by setting the **Enabled** property.</span></span><br/>                                      |
| [<span data-ttu-id="e3778-130">**SetName**</span><span class="sxs-lookup"><span data-stu-id="e3778-130">**SetName**</span></span>](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | <span data-ttu-id="e3778-131">Legt die **Name** -Eigenschaft für die RD-RAP fest.</span><span class="sxs-lookup"><span data-stu-id="e3778-131">Sets the **Name** property for the RD RAP.</span></span><br/>                                                               |
| [<span data-ttu-id="e3778-132">**Setportnumbers**</span><span class="sxs-lookup"><span data-stu-id="e3778-132">**SetPortNumbers**</span></span>](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | <span data-ttu-id="e3778-133">Legt die **portnumbers** -Eigenschaft für die RD-RAP fest.</span><span class="sxs-lookup"><span data-stu-id="e3778-133">Sets the **PortNumbers** property for the RD RAP.</span></span><br/>                                                        |
| [<span data-ttu-id="e3778-134">**"Abtresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="e3778-134">**SetResourceGroup**</span></span>](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | <span data-ttu-id="e3778-135">Legt die Eigenschaften **resourcegrouptype** und **resourcegroupname** fest.</span><span class="sxs-lookup"><span data-stu-id="e3778-135">Sets the **ResourceGroupType** and **ResourceGroupName** properties.</span></span><br/>                                     |
| [<span data-ttu-id="e3778-136">**Setusergroupnames**</span><span class="sxs-lookup"><span data-stu-id="e3778-136">**SetUserGroupNames**</span></span>](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | <span data-ttu-id="e3778-137">Legt die **usergroupnames** -Eigenschaft für die RD-RAP fest.</span><span class="sxs-lookup"><span data-stu-id="e3778-137">Sets the **UserGroupNames** property for the RD RAP.</span></span><br/>                                                     |
| [<span data-ttu-id="e3778-138">**Aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="e3778-138">**Update**</span></span>](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="e3778-139">Aktualisiert die aktuelle RD-RAP.</span><span class="sxs-lookup"><span data-stu-id="e3778-139">Updates the current RD RAP.</span></span><br/>                                                                              |



 

### <a name="properties"></a><span data-ttu-id="e3778-140">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3778-140">Properties</span></span>

<span data-ttu-id="e3778-141">Die Win32-Klasse "t- **\_ gatewayresourceauthorizationpolicy** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e3778-141">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3778-142">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e3778-142">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3778-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e3778-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3778-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3778-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3778-145">Beschreibung der RD-RAP.</span><span class="sxs-lookup"><span data-stu-id="e3778-145">Description of the RD RAP.</span></span> <span data-ttu-id="e3778-146">Diese Eigenschaft wird mit der [**setDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) -Methode geändert.</span><span class="sxs-lookup"><span data-stu-id="e3778-146">This property is changed with the [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e3778-147">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="e3778-147">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3778-148">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e3778-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e3778-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3778-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3778-150">Gibt an, ob diese RD-RAP aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e3778-150">Indicates whether this RD RAP is enabled.</span></span> <span data-ttu-id="e3778-151">Diese Eigenschaft wird [**mit der Methode**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) "" der Methode "\*" geändert.</span><span class="sxs-lookup"><span data-stu-id="e3778-151">This property is changed with the [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e3778-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="e3778-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3778-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e3778-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3778-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3778-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3778-155">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e3778-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e3778-156">Name der RD-RAP.</span><span class="sxs-lookup"><span data-stu-id="e3778-156">Name of the RD RAP.</span></span> <span data-ttu-id="e3778-157">Diese Eigenschaft wird mit der [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) -Methode geändert.</span><span class="sxs-lookup"><span data-stu-id="e3778-157">This property is changed with the [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e3778-158">**Portnummern**</span><span class="sxs-lookup"><span data-stu-id="e3778-158">**PortNumbers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3778-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e3778-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3778-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3778-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3778-161">Liste von durch Semikolons getrennten Portnummern, die für diese Richtlinie zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e3778-161">List of semicolon-separated port numbers that are allowed for this policy.</span></span> <span data-ttu-id="e3778-162">Um eine beliebige Portnummer zuzulassen, legen Sie " \* " fest.</span><span class="sxs-lookup"><span data-stu-id="e3778-162">To allow any port number, set "\*".</span></span>

</dd> <dt>

<span data-ttu-id="e3778-163">**Protocolnames**</span><span class="sxs-lookup"><span data-stu-id="e3778-163">**ProtocolNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3778-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e3778-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3778-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3778-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3778-166">Liste von durch Semikolons getrennten Protokollnamen, die für diese Richtlinie aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="e3778-166">List of semicolon-separated protocol names that are enabled for this policy.</span></span> <span data-ttu-id="e3778-167">Namen müssen mit der Rückgabe der [**getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md) -Methode der Win32-Klasse " [**\_ tgatewayserversettings**](win32-tsgatewayserversettings.md) " identisch sein.</span><span class="sxs-lookup"><span data-stu-id="e3778-167">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e3778-168">**ResourceGroupName**</span><span class="sxs-lookup"><span data-stu-id="e3778-168">**ResourceGroupName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3778-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e3778-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3778-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3778-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3778-171">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="e3778-171">Resource group name.</span></span> <span data-ttu-id="e3778-172">Diese Eigenschaft wird [**mit der Methode**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) "" der Methode "\*" geändert.</span><span class="sxs-lookup"><span data-stu-id="e3778-172">This property is changed with the [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e3778-173">**Resourcegrouptype**</span><span class="sxs-lookup"><span data-stu-id="e3778-173">**ResourceGroupType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3778-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e3778-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3778-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3778-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3778-176">Identifiziert den Typ der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e3778-176">Identifies the type of the resource group.</span></span> <span data-ttu-id="e3778-177">Diese Eigenschaft wird [**mit der Methode**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) "" der Methode "\*" geändert.</span><span class="sxs-lookup"><span data-stu-id="e3778-177">This property is changed with the [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

<dt>

<span data-ttu-id="e3778-178">Sorgte</span><span class="sxs-lookup"><span data-stu-id="e3778-178">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="e3778-179">Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e3778-179">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="e3778-180">Gewöhnt</span><span class="sxs-lookup"><span data-stu-id="e3778-180">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="e3778-181">Computer Gruppe, wie in Active Directory Domain Services gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e3778-181">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="e3778-182">Allen</span><span class="sxs-lookup"><span data-stu-id="e3778-182">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="e3778-183">Alle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e3778-183">All resources.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e3778-184">**Usergroupnames**</span><span class="sxs-lookup"><span data-stu-id="e3778-184">**UserGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3778-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e3778-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3778-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3778-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3778-187">Durch Semikolons getrennte Liste von Benutzergruppen Namen.</span><span class="sxs-lookup"><span data-stu-id="e3778-187">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="e3778-188">Wenn der Benutzer zu einer dieser Benutzergruppen gehört, wird der Zugriff zugelassen.</span><span class="sxs-lookup"><span data-stu-id="e3778-188">If the user belongs to any of these user groups, access will be permitted.</span></span> <span data-ttu-id="e3778-189">Diese Eigenschaft wird mit den Methoden [**setusergroupnames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**addusergroupnames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)und [**removeusergroupnames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) geändert.</span><span class="sxs-lookup"><span data-stu-id="e3778-189">This property is changed with the [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), and [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3778-190">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3778-190">Remarks</span></span>

<span data-ttu-id="e3778-191">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="e3778-191">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="e3778-192">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="e3778-192">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e3778-193">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="e3778-193">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e3778-194">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e3778-194">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e3778-195">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e3778-195">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3778-196">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3778-196">Requirements</span></span>



| <span data-ttu-id="e3778-197">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3778-197">Requirement</span></span> | <span data-ttu-id="e3778-198">Wert</span><span class="sxs-lookup"><span data-stu-id="e3778-198">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3778-199">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3778-199">Minimum supported client</span></span><br/> | <span data-ttu-id="e3778-200">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e3778-200">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e3778-201">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3778-201">Minimum supported server</span></span><br/> | <span data-ttu-id="e3778-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3778-202">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e3778-203">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3778-203">Namespace</span></span><br/>                | <span data-ttu-id="e3778-204">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e3778-204">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e3778-205">MOF</span><span class="sxs-lookup"><span data-stu-id="e3778-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3778-206"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="e3778-206"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3778-207">DLL</span><span class="sxs-lookup"><span data-stu-id="e3778-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3778-208"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3778-208"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e3778-209">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3778-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3778-210">**Win32-"- \_ gatewayconnection"**</span><span class="sxs-lookup"><span data-stu-id="e3778-210">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="e3778-211">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="e3778-211">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="e3778-212">**Win32-"t- \_ gatewayloadbalancer"**</span><span class="sxs-lookup"><span data-stu-id="e3778-212">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="e3778-213">**Win32-"t- \_ gatewayradiusserver"**</span><span class="sxs-lookup"><span data-stu-id="e3778-213">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="e3778-214">**Win32-Datei " \_ zgatewayresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="e3778-214">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="e3778-215">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="e3778-215">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 


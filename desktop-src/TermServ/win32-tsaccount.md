---
title: Win32_TSAccount-Klasse
description: Ermöglicht das Löschen eines Kontos, das im Win32-Terminal vorhanden ist, \_ sowie das Ändern vorhandener Berechtigungen.
ms.assetid: fd4d8a0f-685b-4619-84f1-faefbabd04ba
ms.tgt_platform: multiple
keywords:
- Win32_TSAccount-Klasse Remotedesktopdienste
- Win32_TSAccount Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSAccount
- Win32_TSAccount.Caption
- Win32_TSAccount.Description
- Win32_TSAccount.InstallDate
- Win32_TSAccount.Name
- Win32_TSAccount.Status
- Win32_TSAccount.TerminalName
- Win32_TSAccount.AccountName
- Win32_TSAccount.AuditFail
- Win32_TSAccount.AuditSuccess
- Win32_TSAccount.PermissionsAllowed
- Win32_TSAccount.PermissionsDenied
- Win32_TSAccount.SID
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fed32943cf89728081e2443dfffe2e3762298d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345327"
---
# <a name="win32_tsaccount-class"></a><span data-ttu-id="43bf2-105">Win32-Klasse "- \_ Konto"</span><span class="sxs-lookup"><span data-stu-id="43bf2-105">Win32\_TSAccount class</span></span>

<span data-ttu-id="43bf2-106">Die WMI-Klasse für das **Win32- \_ Konto** ermöglicht das Löschen eines Kontos, das im [**Win32- \_ Terminal**](win32-terminal.md) vorhanden ist, und das Ändern vorhandener Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="43bf2-106">The **Win32\_TSAccount** WMI class allows deletion of an account that exists on the [**Win32\_Terminal**](win32-terminal.md) and modification of existing permissions.</span></span>

<span data-ttu-id="43bf2-107">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="43bf2-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="43bf2-108">Referenzinformationen zu-Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="43bf2-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="43bf2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="43bf2-109">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSACCOUNT_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSAccount : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   AccountName;
  uint32   AuditFail;
  uint32   AuditSuccess;
  uint32   PermissionsAllowed;
  uint32   PermissionsDenied;
  string   SID;
};
```

## <a name="members"></a><span data-ttu-id="43bf2-110">Member</span><span class="sxs-lookup"><span data-stu-id="43bf2-110">Members</span></span>

<span data-ttu-id="43bf2-111">Die Win32-Klasse " **\_ zaccount** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="43bf2-111">The **Win32\_TSAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="43bf2-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="43bf2-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="43bf2-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43bf2-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="43bf2-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="43bf2-114">Methods</span></span>

<span data-ttu-id="43bf2-115">Die Win32-Klasse " **\_ zaccount** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="43bf2-115">The **Win32\_TSAccount** class has these methods.</span></span>



| <span data-ttu-id="43bf2-116">Methode</span><span class="sxs-lookup"><span data-stu-id="43bf2-116">Method</span></span>                                                                   | <span data-ttu-id="43bf2-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43bf2-117">Description</span></span>                                                                                  |
|:-------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43bf2-118">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="43bf2-118">**Delete**</span></span>](win32-tsaccount-delete.md)                                 | <span data-ttu-id="43bf2-119">Löscht den angegebenen Benutzer, die angegebene Gruppe oder das angegebene Computer Konto.</span><span class="sxs-lookup"><span data-stu-id="43bf2-119">Deletes the specified user, group, or computer account.</span></span><br/>                           |
| [<span data-ttu-id="43bf2-120">**Modifyauditberechtigungs-**</span><span class="sxs-lookup"><span data-stu-id="43bf2-120">**ModifyAuditPermissions**</span></span>](win32-tsaccount-modifyauditpermissions.md) | <span data-ttu-id="43bf2-121">Ändert die Granularität des Satzes von Überwachungs Berechtigungen für das angegebene Konto.</span><span class="sxs-lookup"><span data-stu-id="43bf2-121">Changes the granularity of the set of audit permissions of the specified account.</span></span><br/> |
| [<span data-ttu-id="43bf2-122">**Modify-Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="43bf2-122">**ModifyPermissions**</span></span>](win32-tsaccount-modifypermissions.md)           | <span data-ttu-id="43bf2-123">Legt einen präziseteren Berechtigungs Satz für das angegebene Konto fest.</span><span class="sxs-lookup"><span data-stu-id="43bf2-123">Sets a more granular permission set to the specified account.</span></span><br/>                     |



 

### <a name="properties"></a><span data-ttu-id="43bf2-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43bf2-124">Properties</span></span>

<span data-ttu-id="43bf2-125">Die **Win32 \_** -Klasse "-Konto" verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="43bf2-125">The **Win32\_TSAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43bf2-126">**AccountName**</span><span class="sxs-lookup"><span data-stu-id="43bf2-126">**AccountName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bf2-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="43bf2-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43bf2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="43bf2-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="43bf2-130">Der aktuelle Name des Kontos.</span><span class="sxs-lookup"><span data-stu-id="43bf2-130">The current name of the account.</span></span> <span data-ttu-id="43bf2-131">Der Domänen Name ist enthalten.</span><span class="sxs-lookup"><span data-stu-id="43bf2-131">The domain name is included.</span></span>

</dd> <dt>

<span data-ttu-id="43bf2-132">**Auditfail**</span><span class="sxs-lookup"><span data-stu-id="43bf2-132">**AuditFail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bf2-133">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43bf2-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43bf2-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bf2-135">Gibt die [Remotedesktop-Sitzungshost Services-Berechtigungen](terminal-services-permissions.md) an, die auf eine Fehlerbedingung überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="43bf2-135">Specifies the [Remote Desktop Session Host Services Permissions](terminal-services-permissions.md) that are audited for a failure condition.</span></span> <span data-ttu-id="43bf2-136">Der Wert dieser Eigenschaft ist eine Bitmaske, die auf einen oder mehrere Werte der **permissionsallowed** -Eigenschaft festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="43bf2-136">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="43bf2-137">**WinStation \_ Abfrage = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="43bf2-137">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="43bf2-138">**WinStation \_ Set = 0x2** (1)</span><span class="sxs-lookup"><span data-stu-id="43bf2-138">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

<span data-ttu-id="43bf2-139">**WinStation \_ Abmeldung = 0x4** (2)</span><span class="sxs-lookup"><span data-stu-id="43bf2-139">**WINSTATION\_LOGOFF=0x4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="43bf2-140">**WinStation \_ \| Erforderliche virtuelle Standard \_ Rechte \_ = 0xF 008** (3)</span><span class="sxs-lookup"><span data-stu-id="43bf2-140">**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="43bf2-141">**WinStation \_ Shadow = 0x10** (4)</span><span class="sxs-lookup"><span data-stu-id="43bf2-141">**WINSTATION\_SHADOW=0x10** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="43bf2-142">**WinStation \_ Login = 0x20** (5)</span><span class="sxs-lookup"><span data-stu-id="43bf2-142">**WINSTATION\_LOGON=0x20** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="43bf2-143">**WinStation \_ MSG = 0x80** (6)</span><span class="sxs-lookup"><span data-stu-id="43bf2-143">**WINSTATION\_MSG=0x80** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="43bf2-144">**WinStation \_ Connect = 0x100** (7)</span><span class="sxs-lookup"><span data-stu-id="43bf2-144">**WINSTATION\_CONNECT=0x100** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="43bf2-145">**WinStation \_ Disconnect = 0x200** (8)</span><span class="sxs-lookup"><span data-stu-id="43bf2-145">**WINSTATION\_DISCONNECT=0x200** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43bf2-146">**AuditSuccess**</span><span class="sxs-lookup"><span data-stu-id="43bf2-146">**AuditSuccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bf2-147">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43bf2-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43bf2-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bf2-149">Gibt die RD-Sitzungshost serverspezifischen Berechtigungen an, die auf eine Erfolgs Bedingung überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="43bf2-149">Specifies the RD Session Host server-specific permissions that are audited for a success condition.</span></span> <span data-ttu-id="43bf2-150">Der Wert dieser Eigenschaft ist eine Bitmaske, die auf einen oder mehrere Werte der **permissionsallowed** -Eigenschaft festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="43bf2-150">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="43bf2-151">**WinStation \_ Abfrage = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="43bf2-151">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="43bf2-152">**WinStation \_ Set = 0x2** (1)</span><span class="sxs-lookup"><span data-stu-id="43bf2-152">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_logoff_0x4winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_LOGOFF_0X4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="43bf2-153">**WinStation \_ Abmeldung = 0x4winstation \_ virtuelle \| Standard \_ Rechte \_ erforderlich = 0xF 008** (2)</span><span class="sxs-lookup"><span data-stu-id="43bf2-153">**WINSTATION\_LOGOFF=0x4WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="43bf2-154">**WinStation \_ Shadow = 0x10** (3)</span><span class="sxs-lookup"><span data-stu-id="43bf2-154">**WINSTATION\_SHADOW=0x10** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="43bf2-155">**WinStation \_ Login = 0x20** (4)</span><span class="sxs-lookup"><span data-stu-id="43bf2-155">**WINSTATION\_LOGON=0x20** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="43bf2-156">**WinStation \_ MSG = 0x80** (5)</span><span class="sxs-lookup"><span data-stu-id="43bf2-156">**WINSTATION\_MSG=0x80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="43bf2-157">**WinStation \_ Connect = 0x100** (6)</span><span class="sxs-lookup"><span data-stu-id="43bf2-157">**WINSTATION\_CONNECT=0x100** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="43bf2-158">**WinStation \_ Disconnect = 0x200** (7)</span><span class="sxs-lookup"><span data-stu-id="43bf2-158">**WINSTATION\_DISCONNECT=0x200** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43bf2-159">**Caption**</span><span class="sxs-lookup"><span data-stu-id="43bf2-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bf2-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="43bf2-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43bf2-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-162">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="43bf2-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="43bf2-163">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="43bf2-163">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="43bf2-164">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="43bf2-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43bf2-165">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="43bf2-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bf2-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="43bf2-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43bf2-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bf2-168">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="43bf2-168">Description of the object.</span></span>

<span data-ttu-id="43bf2-169">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="43bf2-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43bf2-170">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="43bf2-170">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bf2-171">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="43bf2-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43bf2-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-173">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="43bf2-173">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="43bf2-174">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="43bf2-174">The date the object was installed.</span></span> <span data-ttu-id="43bf2-175">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="43bf2-175">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="43bf2-176">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="43bf2-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43bf2-177">**Name**</span><span class="sxs-lookup"><span data-stu-id="43bf2-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bf2-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="43bf2-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43bf2-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bf2-180">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="43bf2-180">The name of the object.</span></span>

<span data-ttu-id="43bf2-181">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="43bf2-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43bf2-182">**Permissionsallowed**</span><span class="sxs-lookup"><span data-stu-id="43bf2-182">**PermissionsAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bf2-183">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43bf2-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43bf2-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bf2-185">Gibt die für das Konto zulässigen [Remotedesktopdienste Berechtigungen](terminal-services-permissions.md) an.</span><span class="sxs-lookup"><span data-stu-id="43bf2-185">Specifies the [Remote Desktop Services Permissions](terminal-services-permissions.md) allowed for the account.</span></span> <span data-ttu-id="43bf2-186">Der Wert dieser Eigenschaft ist eine Bitmaske, die auf einen oder mehrere der folgenden Werte festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="43bf2-186">The value of this property is a bitmask, which can be set to one or more of the following values.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="43bf2-187"><span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**WinStation \_ Abfrage = 0x1** (1)</span><span class="sxs-lookup"><span data-stu-id="43bf2-187"><span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**WINSTATION\_QUERY=0x1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="43bf2-188">Berechtigung zum Abfragen von Informationen über eine Sitzung.</span><span class="sxs-lookup"><span data-stu-id="43bf2-188">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="43bf2-189"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WinStation \_ Set** (2)</span><span class="sxs-lookup"><span data-stu-id="43bf2-189"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (2)</span></span>


</dt> <dd>

<span data-ttu-id="43bf2-190">Berechtigung zum Ändern von Verbindungsparametern.</span><span class="sxs-lookup"><span data-stu-id="43bf2-190">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="43bf2-191"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WinStation \_ Zurücksetzen** (64)</span><span class="sxs-lookup"><span data-stu-id="43bf2-191"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (64)</span></span>


</dt> <dd>

<span data-ttu-id="43bf2-192">Berechtigung zum Zurücksetzen oder Beenden einer Sitzung oder einer Verbindung.</span><span class="sxs-lookup"><span data-stu-id="43bf2-192">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="43bf2-193"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WinStation \_ \| \_ \_ Erforderliche virtuelle Standard Rechte** (983048)</span><span class="sxs-lookup"><span data-stu-id="43bf2-193"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (983048)</span></span>


</dt> <dd>

<span data-ttu-id="43bf2-194">Berechtigung zum Verwenden von virtuellen Kanälen.</span><span class="sxs-lookup"><span data-stu-id="43bf2-194">Permission to use virtual channels.</span></span> <span data-ttu-id="43bf2-195">Virtuelle Kanäle ermöglichen den Zugriff von einem Serverprogramm auf Client Geräte.</span><span class="sxs-lookup"><span data-stu-id="43bf2-195">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="43bf2-196"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WinStation \_ Schatten** (16)</span><span class="sxs-lookup"><span data-stu-id="43bf2-196"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (16)</span></span>


</dt> <dd>

<span data-ttu-id="43bf2-197">Berechtigung, um die Sitzung eines anderen Benutzers zu überschatten oder Remote zu steuern.</span><span class="sxs-lookup"><span data-stu-id="43bf2-197">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="43bf2-198"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WinStation \_ Anmelden** (32)</span><span class="sxs-lookup"><span data-stu-id="43bf2-198"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (32)</span></span>


</dt> <dd>

<span data-ttu-id="43bf2-199">Berechtigung zum Anmelden bei einer Sitzung auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="43bf2-199">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="43bf2-200"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WinStation \_ Abmeldung (4** )</span><span class="sxs-lookup"><span data-stu-id="43bf2-200"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (4)</span></span>


</dt> <dd>

<span data-ttu-id="43bf2-201">Berechtigung zum Abmelden eines Benutzers von einer Sitzung.</span><span class="sxs-lookup"><span data-stu-id="43bf2-201">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="43bf2-202"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WinStation \_ Meldung (128** )</span><span class="sxs-lookup"><span data-stu-id="43bf2-202"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (128)</span></span>


</dt> <dd>

<span data-ttu-id="43bf2-203">Die Berechtigung zum Senden einer Nachricht an die Sitzung eines anderen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="43bf2-203">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="43bf2-204"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WinStation \_ Verbinden** (256)</span><span class="sxs-lookup"><span data-stu-id="43bf2-204"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (256)</span></span>


</dt> <dd>

<span data-ttu-id="43bf2-205">Berechtigung zum Herstellen einer Verbindung mit einer anderen Sitzung.</span><span class="sxs-lookup"><span data-stu-id="43bf2-205">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="43bf2-206"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WinStation \_ Verbindung trennen** (512)</span><span class="sxs-lookup"><span data-stu-id="43bf2-206"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (512)</span></span>


</dt> <dd>

<span data-ttu-id="43bf2-207">Berechtigung zum Trennen einer Sitzung.</span><span class="sxs-lookup"><span data-stu-id="43bf2-207">Permission to disconnect a session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="43bf2-208">**Permissionsverweigert**</span><span class="sxs-lookup"><span data-stu-id="43bf2-208">**PermissionsDenied**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bf2-209">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43bf2-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43bf2-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bf2-211">Gibt die RD-Sitzungshost serverspezifischen Berechtigungen an, die für das Konto nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="43bf2-211">Specifies the RD Session Host server-specific permissions disallowed for the account.</span></span> <span data-ttu-id="43bf2-212">Der Wert dieser Eigenschaft ist eine Bitmaske, die auf einen oder mehrere Werte der **permissionsallowed** -Eigenschaft festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="43bf2-212">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="43bf2-213">**WinStation \_ Abfrage = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="43bf2-213">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="43bf2-214">**WinStation \_ Set = 0x2** (1)</span><span class="sxs-lookup"><span data-stu-id="43bf2-214">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

<span data-ttu-id="43bf2-215">**WinStation \_ Abmeldung = 0x4** (2)</span><span class="sxs-lookup"><span data-stu-id="43bf2-215">**WINSTATION\_LOGOFF=0x4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="43bf2-216">**WinStation \_ \| Erforderliche virtuelle Standard \_ Rechte \_ = 0xF 008** (3)</span><span class="sxs-lookup"><span data-stu-id="43bf2-216">**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="43bf2-217">**WinStation \_ Shadow = 0x10** (4)</span><span class="sxs-lookup"><span data-stu-id="43bf2-217">**WINSTATION\_SHADOW=0x10** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="43bf2-218">**WinStation \_ Login = 0x20** (5)</span><span class="sxs-lookup"><span data-stu-id="43bf2-218">**WINSTATION\_LOGON=0x20** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="43bf2-219">**WinStation \_ MSG = 0x80** (6)</span><span class="sxs-lookup"><span data-stu-id="43bf2-219">**WINSTATION\_MSG=0x80** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="43bf2-220">**WinStation \_ Connect = 0x100** (7)</span><span class="sxs-lookup"><span data-stu-id="43bf2-220">**WINSTATION\_CONNECT=0x100** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="43bf2-221">**WinStation \_ Disconnect = 0x200** (8)</span><span class="sxs-lookup"><span data-stu-id="43bf2-221">**WINSTATION\_DISCONNECT=0x200** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43bf2-222">**SID**</span><span class="sxs-lookup"><span data-stu-id="43bf2-222">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bf2-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="43bf2-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43bf2-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bf2-225">Gibt die [Sicherheits](/windows/desktop/SecAuthZ/security-identifiers) -IDs des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="43bf2-225">Specifies the [Security Identifiers](/windows/desktop/SecAuthZ/security-identifiers) of the account.</span></span>

</dd> <dt>

<span data-ttu-id="43bf2-226">**Status**</span><span class="sxs-lookup"><span data-stu-id="43bf2-226">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bf2-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="43bf2-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43bf2-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-229">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="43bf2-229">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="43bf2-230">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="43bf2-230">Current status of the object.</span></span> <span data-ttu-id="43bf2-231">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="43bf2-231">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="43bf2-232">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="43bf2-232">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="43bf2-233">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="43bf2-233">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="43bf2-234">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="43bf2-234">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="43bf2-235">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="43bf2-235">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="43bf2-236">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="43bf2-236">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="43bf2-237">("OK")</span><span class="sxs-lookup"><span data-stu-id="43bf2-237">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43bf2-238">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="43bf2-238">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43bf2-239">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="43bf2-239">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43bf2-240">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="43bf2-240">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43bf2-241">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="43bf2-241">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43bf2-242">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="43bf2-242">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43bf2-243">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="43bf2-243">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43bf2-244">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="43bf2-244">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43bf2-245">**Terminal Name**</span><span class="sxs-lookup"><span data-stu-id="43bf2-245">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bf2-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="43bf2-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bf2-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43bf2-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bf2-248">Der Name des Terminals.</span><span class="sxs-lookup"><span data-stu-id="43bf2-248">The name of the terminal.</span></span>

<span data-ttu-id="43bf2-249">Diese Eigenschaft wird von [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="43bf2-249">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43bf2-250">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43bf2-250">Remarks</span></span>

<span data-ttu-id="43bf2-251">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="43bf2-251">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="43bf2-252">Bei C/C++-aufrufen wäre dies eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt- \_ Datenschutz**.</span><span class="sxs-lookup"><span data-stu-id="43bf2-252">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="43bf2-253">Bei Visual Basic-und Skript aufrufen wäre dies eine Authentifizierungs Ebene von **wbemauthenticationlevelpktprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="43bf2-253">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="43bf2-254">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="43bf2-254">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="43bf2-255">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="43bf2-255">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="43bf2-256">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="43bf2-256">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="43bf2-257">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="43bf2-257">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="43bf2-258">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="43bf2-258">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="43bf2-259">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43bf2-259">Requirements</span></span>



| <span data-ttu-id="43bf2-260">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43bf2-260">Requirement</span></span> | <span data-ttu-id="43bf2-261">Wert</span><span class="sxs-lookup"><span data-stu-id="43bf2-261">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43bf2-262">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43bf2-262">Minimum supported client</span></span><br/> | <span data-ttu-id="43bf2-263">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43bf2-263">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43bf2-264">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43bf2-264">Minimum supported server</span></span><br/> | <span data-ttu-id="43bf2-265">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43bf2-265">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43bf2-266">Namespace</span><span class="sxs-lookup"><span data-stu-id="43bf2-266">Namespace</span></span><br/>                | <span data-ttu-id="43bf2-267">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="43bf2-267">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="43bf2-268">MOF</span><span class="sxs-lookup"><span data-stu-id="43bf2-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43bf2-269"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="43bf2-269"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="43bf2-270">DLL</span><span class="sxs-lookup"><span data-stu-id="43bf2-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43bf2-271"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43bf2-271"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43bf2-272">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43bf2-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43bf2-273">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="43bf2-273">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 


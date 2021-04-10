---
description: Das Win32- \_ Benutzerkonto&\# 32; Die WMI-Klasse enthält Informationen zu einem Benutzerkonto auf einem Computersystem, auf dem Windows ausgeführt wird.
ms.assetid: 747b2ce2-ae38-47de-bf3a-97058df56a7a
ms.tgt_platform: multiple
title: Win32_UserAccount-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount
- Win32_UserAccount.AccountType
- Win32_UserAccount.Caption
- Win32_UserAccount.Description
- Win32_UserAccount.Disabled
- Win32_UserAccount.Domain
- Win32_UserAccount.FullName
- Win32_UserAccount.InstallDate
- Win32_UserAccount.LocalAccount
- Win32_UserAccount.Lockout
- Win32_UserAccount.Name
- Win32_UserAccount.PasswordChangeable
- Win32_UserAccount.PasswordExpires
- Win32_UserAccount.PasswordRequired
- Win32_UserAccount.SID
- Win32_UserAccount.SIDType
- Win32_UserAccount.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5af83f7a52e9f3db9dbaa4a959bfe01ae740746
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041373"
---
# <a name="win32_useraccount-class"></a><span data-ttu-id="4fb43-103">Win32 \_ User Account-Klasse</span><span class="sxs-lookup"><span data-stu-id="4fb43-103">Win32\_UserAccount class</span></span>

<span data-ttu-id="4fb43-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für das **Win32- \_ Benutzerkonto** enthält Informationen zu einem Benutzerkonto auf einem Computersystem, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4fb43-104">The **Win32\_UserAccount** [WMI class](../wmisdk/retrieving-a-class.md) contains information about a user account on a computer system running Windows.</span></span>

> [!Note]  
> <span data-ttu-id="4fb43-105">Da sowohl der **Name** als auch die **Domäne** Schlüsseleigenschaften sind, kann das Auflisten von **Win32 \_ Useraccount** in einem großen Netzwerk die Leistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="4fb43-105">Because both the **Name** and **Domain** are key properties, enumerating **Win32\_UserAccount** on a large network can negatively affect performance.</span></span> <span data-ttu-id="4fb43-106">Das Aufrufen von **GetObject** oder Abfragen für eine bestimmte Instanz hat weniger Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="4fb43-106">Calling **GetObject** or querying for a specific instance has less impact.</span></span>

 

<span data-ttu-id="4fb43-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4fb43-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4fb43-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4fb43-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb43-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fb43-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserAccount : Win32_Account
{
  uint32   AccountType;
  string   Caption;
  string   Description;
  boolean  Disabled;
  string   Domain;
  string   FullName;
  datetime InstallDate;
  boolean  LocalAccount;
  boolean  Lockout;
  string   Name;
  boolean  PasswordChangeable;
  boolean  PasswordExpires;
  boolean  PasswordRequired;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="4fb43-110">Member</span><span class="sxs-lookup"><span data-stu-id="4fb43-110">Members</span></span>

<span data-ttu-id="4fb43-111">Die **Win32 \_ User Account** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4fb43-111">The **Win32\_UserAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="4fb43-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="4fb43-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4fb43-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4fb43-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4fb43-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="4fb43-114">Methods</span></span>

<span data-ttu-id="4fb43-115">Die **Win32 \_ User Account** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4fb43-115">The **Win32\_UserAccount** class has these methods.</span></span>



| <span data-ttu-id="4fb43-116">Methode</span><span class="sxs-lookup"><span data-stu-id="4fb43-116">Method</span></span>                                                     | <span data-ttu-id="4fb43-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4fb43-117">Description</span></span>                                             |
|:-----------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="4fb43-118">**Benen**</span><span class="sxs-lookup"><span data-stu-id="4fb43-118">**Rename**</span></span>](rename-method-in-class-win32-useraccount.md) | <span data-ttu-id="4fb43-119">Ermöglicht das Umbenennen des Benutzerkontos.</span><span class="sxs-lookup"><span data-stu-id="4fb43-119">Allows for the renaming of the user account.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4fb43-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4fb43-120">Properties</span></span>

<span data-ttu-id="4fb43-121">Die **Win32 \_ User Account** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4fb43-121">The **Win32\_UserAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4fb43-122">**AccountType**</span><span class="sxs-lookup"><span data-stu-id="4fb43-122">**AccountType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-123">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4fb43-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fb43-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-125">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| usri2 \_ Flags")</span><span class="sxs-lookup"><span data-stu-id="4fb43-125">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|usri2\_flags")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-126">Flags, die die Merkmale eines Windows-Benutzerkontos beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4fb43-126">Flags that describe the characteristics of a Windows user account.</span></span>

<dt>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>

<span data-ttu-id="4fb43-127"><span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Temporäres doppeltes Konto** (256)</span><span class="sxs-lookup"><span data-stu-id="4fb43-127"><span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Temporary duplicate account** (256)</span></span>


</dt> <dd>

<span data-ttu-id="4fb43-128">**\_Konto für Temp Temp- \_ Duplizierung \_**</span><span class="sxs-lookup"><span data-stu-id="4fb43-128">**UF\_TEMP\_DUPLICATE\_ACCOUNT**</span></span>

<span data-ttu-id="4fb43-129">Lokales Benutzerkonto für Benutzer, die über ein primäres Konto in einer anderen Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="4fb43-129">Local user account for users who have a primary account in another domain.</span></span> <span data-ttu-id="4fb43-130">Dieses Konto ermöglicht nur den Benutzer Zugriff auf diese Domäne – nicht auf eine Domäne, die dieser Domäne vertraut.</span><span class="sxs-lookup"><span data-stu-id="4fb43-130">This account provides user access to this domain only—not to any domain that trusts this domain.</span></span>

</dd> <dt>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span data-ttu-id="4fb43-131"><span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Normales Konto** (512)</span><span class="sxs-lookup"><span data-stu-id="4fb43-131"><span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Normal account** (512)</span></span>


</dt> <dd>

<span data-ttu-id="4fb43-132">**\_normales \_ Konto**</span><span class="sxs-lookup"><span data-stu-id="4fb43-132">**UF\_NORMAL\_ACCOUNT**</span></span>

<span data-ttu-id="4fb43-133">Der Standard Kontotyp, der einen typischen Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="4fb43-133">Default account type that represents a typical user.</span></span>

</dd> <dt>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span data-ttu-id="4fb43-134"><span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Domänen Vertrauensstellungs Konto** (2048)</span><span class="sxs-lookup"><span data-stu-id="4fb43-134"><span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Interdomain trust account** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="4fb43-135">**Konto für die Vertrauensstellung der \_ Verbindungs Domäne \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4fb43-135">**UF\_INTERDOMAIN\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="4fb43-136">Konto für eine System Domäne, die anderen Domänen vertraut.</span><span class="sxs-lookup"><span data-stu-id="4fb43-136">Account for a system domain that trusts other domains.</span></span>

</dd> <dt>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span data-ttu-id="4fb43-137"><span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>Arbeitsstations- **Vertrauensstellungs Konto** (4096)</span><span class="sxs-lookup"><span data-stu-id="4fb43-137"><span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Workstation trust account** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="4fb43-138">**Konto der Vertrauensstellung der \_ \_ Vertrauensstellung \_**</span><span class="sxs-lookup"><span data-stu-id="4fb43-138">**UF\_WORKSTATION\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="4fb43-139">Computer Konto für ein Computersystem, auf dem Windows ausgeführt wird, das Mitglied dieser Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="4fb43-139">Computer account for a computer system running Windows that is a member of this domain.</span></span>

</dd> <dt>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span data-ttu-id="4fb43-140"><span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Server Vertrauensstellungs Konto** (8192)</span><span class="sxs-lookup"><span data-stu-id="4fb43-140"><span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Server trust account** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="4fb43-141">**\_ \_ \_ Konto Vertrauens Konto für den Server**</span><span class="sxs-lookup"><span data-stu-id="4fb43-141">**UF\_SERVER\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="4fb43-142">Konto für einen Domänen Controller der Systemsicherung, der Mitglied dieser Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="4fb43-142">Account for a system backup domain controller that is a member of this domain.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4fb43-143">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4fb43-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4fb43-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fb43-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-146">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4fb43-146">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-147">Domäne und Benutzername des Kontos.</span><span class="sxs-lookup"><span data-stu-id="4fb43-147">Domain and username of the account.</span></span>

<span data-ttu-id="4fb43-148">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4fb43-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fb43-149">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4fb43-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4fb43-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fb43-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-152">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="4fb43-152">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-153">Die Beschreibung des Kontos.</span><span class="sxs-lookup"><span data-stu-id="4fb43-153">Description of the account.</span></span>

<span data-ttu-id="4fb43-154">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4fb43-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fb43-155">**Deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="4fb43-155">**Disabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-156">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4fb43-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4fb43-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-158">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| Benutzer \_ Info \| UF \_ accountdeaktivieren")</span><span class="sxs-lookup"><span data-stu-id="4fb43-158">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|USER\_INFO\|UF\_ACCOUNTDISABLE")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-159">Das Windows-Benutzerkonto ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4fb43-159">Windows user account is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="4fb43-160">**Domäne**</span><span class="sxs-lookup"><span data-stu-id="4fb43-160">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4fb43-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fb43-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-163">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Domäne"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Functions \| Domain Name")</span><span class="sxs-lookup"><span data-stu-id="4fb43-163">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-164">Der Name der Windows-Domäne, zu der ein Benutzerkonto gehört, z. b.: "na-Sales".</span><span class="sxs-lookup"><span data-stu-id="4fb43-164">Name of the Windows domain to which a user account belongs, for example: "NA-SALES".</span></span>

</dd> <dt>

<span data-ttu-id="4fb43-165">**FullName**</span><span class="sxs-lookup"><span data-stu-id="4fb43-165">**FullName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4fb43-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-167">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4fb43-167">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-168">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **usri2 \_ Full \_ Name**")</span><span class="sxs-lookup"><span data-stu-id="4fb43-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**usri2\_full\_name**")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-169">Der vollständige Name eines lokalen Benutzers, z. b.: "Dan Wilson".</span><span class="sxs-lookup"><span data-stu-id="4fb43-169">Full name of a local user, for example: "Dan Wilson".</span></span>

</dd> <dt>

<span data-ttu-id="4fb43-170">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4fb43-170">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-171">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4fb43-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fb43-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-173">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="4fb43-173">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-174">Das Datum, an dem das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4fb43-174">Date the object is installed.</span></span> <span data-ttu-id="4fb43-175">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4fb43-175">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4fb43-176">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4fb43-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fb43-177">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="4fb43-177">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-178">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4fb43-178">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fb43-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-180">Qualifizierer: [ **korrigiert**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="4fb43-180">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-181">**True** gibt an, dass das Konto auf dem lokalen Computer definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4fb43-181">If **true**, the account is defined on the local computer.</span></span>

<span data-ttu-id="4fb43-182">Diese Eigenschaft wird vom [**Win32- \_ Konto**](win32-account.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4fb43-182">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fb43-183">**Sperrung**</span><span class="sxs-lookup"><span data-stu-id="4fb43-183">**Lockout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-184">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4fb43-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-185">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4fb43-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-186">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ Lockout**")</span><span class="sxs-lookup"><span data-stu-id="4fb43-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_LOCKOUT**")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-187">**True** gibt an, dass das Benutzerkonto aus dem Windows-Betriebssystem gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="4fb43-187">If **true**, the user account is locked out of the Windows operating system.</span></span>

</dd> <dt>

<span data-ttu-id="4fb43-188">**Name**</span><span class="sxs-lookup"><span data-stu-id="4fb43-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4fb43-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fb43-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-191">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Name"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| Name")</span><span class="sxs-lookup"><span data-stu-id="4fb43-191">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-192">Der Name des Windows-Benutzerkontos in der Domäne, die von der **Domänen** Eigenschaft dieser Klasse angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4fb43-192">Name of the Windows user account on the domain that the **Domain** property of this class specifies.</span></span>

<span data-ttu-id="4fb43-193">Beispiel: "danwilson".</span><span class="sxs-lookup"><span data-stu-id="4fb43-193">Example: "danwilson".</span></span>

<span data-ttu-id="4fb43-194">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4fb43-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fb43-195">**Passwordänderbar**</span><span class="sxs-lookup"><span data-stu-id="4fb43-195">**PasswordChangeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-196">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4fb43-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-197">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4fb43-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-198">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ passwd \_ cant \_ Change**")</span><span class="sxs-lookup"><span data-stu-id="4fb43-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_PASSWD\_CANT\_CHANGE**")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-199">**True** gibt an, dass das Kennwort für dieses Benutzerkonto geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4fb43-199">If **true**, the password on this user account can be changed.</span></span>

</dd> <dt>

<span data-ttu-id="4fb43-200">**PasswordExpires**</span><span class="sxs-lookup"><span data-stu-id="4fb43-200">**PasswordExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-201">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4fb43-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-202">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4fb43-202">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-203">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ 't \_ expire \_ passwd**")</span><span class="sxs-lookup"><span data-stu-id="4fb43-203">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_DONT\_EXPIRE\_PASSWD**")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-204">**True** gibt an, dass das Kennwort für dieses Benutzerkonto abläuft.</span><span class="sxs-lookup"><span data-stu-id="4fb43-204">If **true**, the password on this user account expires.</span></span>

</dd> <dt>

<span data-ttu-id="4fb43-205">**PasswordRequired**</span><span class="sxs-lookup"><span data-stu-id="4fb43-205">**PasswordRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-206">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4fb43-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-207">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4fb43-207">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-208">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ passwd \_ notreqd**")</span><span class="sxs-lookup"><span data-stu-id="4fb43-208">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_PASSWD\_NOTREQD**")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-209">**True** gibt an, dass ein Kennwort für ein Windows-Benutzerkonto erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4fb43-209">If **true**, a password is required on a Windows user account.</span></span> <span data-ttu-id="4fb43-210">**False** gibt an, dass für dieses Konto kein Kennwort erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4fb43-210">If **false**, this account does not require a password.</span></span>

</dd> <dt>

<span data-ttu-id="4fb43-211">**SID**</span><span class="sxs-lookup"><span data-stu-id="4fb43-211">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-212">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4fb43-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fb43-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-214">Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Security IDs (SIDs)")</span><span class="sxs-lookup"><span data-stu-id="4fb43-214">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-215">Sicherheits-ID (SID) für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="4fb43-215">Security identifier (SID) for this account.</span></span> <span data-ttu-id="4fb43-216">Eine SID ist ein Zeichen folgen Wert variabler Länge, der zum Identifizieren eines Vertrauens nehmers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4fb43-216">A SID is a string value of variable length that is used to identify a trustee.</span></span> <span data-ttu-id="4fb43-217">Jedes Konto verfügt über eine eindeutige SID, die eine Zertifizierungsstelle, z. b. eine Windows-Domäne, ausgibt.</span><span class="sxs-lookup"><span data-stu-id="4fb43-217">Each account has a unique SID that an authority, such as a Windows domain, issues.</span></span> <span data-ttu-id="4fb43-218">Die SID wird in der Sicherheitsdatenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4fb43-218">The SID is stored in the security database.</span></span> <span data-ttu-id="4fb43-219">Wenn sich ein Benutzer anmeldet, ruft das System die Benutzer-SID aus der Datenbank ab, platziert die SID im Benutzer Zugriffs Token und verwendet dann die SID im Benutzer Zugriffs Token, um den Benutzer bei allen nachfolgenden Interaktionen mit der Windows-Sicherheit zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4fb43-219">When a user logs on, the system retrieves the user SID from the database, places the SID in the user access token, and then uses the SID in the user access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="4fb43-220">Jede sid ist ein eindeutiger Bezeichner für einen Benutzer oder eine Gruppe, und ein anderer Benutzer oder eine andere Gruppe kann nicht dieselbe SID haben.</span><span class="sxs-lookup"><span data-stu-id="4fb43-220">Each SID is a unique identifier for a user or group, and a different user or group cannot have the same SID.</span></span>

<span data-ttu-id="4fb43-221">Diese Eigenschaft wird vom [**Win32- \_ Konto**](win32-account.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4fb43-221">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fb43-222">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="4fb43-222">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-223">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="4fb43-223">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fb43-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-225">Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Access Control Enumerationstypen- \| [**sid- \_ Name \_ verwenden**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")</span><span class="sxs-lookup"><span data-stu-id="4fb43-225">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Access Control Enumeration Types\|[**SID\_NAME\_USE**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-226">Enumerationswert, der den Typ der SID angibt.</span><span class="sxs-lookup"><span data-stu-id="4fb43-226">Enumerated value that specifies the type of SID.</span></span>

<span data-ttu-id="4fb43-227">Diese Eigenschaft wird vom [**Win32- \_ Konto**](win32-account.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4fb43-227">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="4fb43-228">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="4fb43-228">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="4fb43-229">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="4fb43-229">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="4fb43-230">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="4fb43-230">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="4fb43-231">**Sidtypealias** (4)</span><span class="sxs-lookup"><span data-stu-id="4fb43-231">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="4fb43-232">**Sidtypewellknowngroup** (5)</span><span class="sxs-lookup"><span data-stu-id="4fb43-232">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="4fb43-233">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="4fb43-233">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="4fb43-234">**Sidtypeingabe valid** (7)</span><span class="sxs-lookup"><span data-stu-id="4fb43-234">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="4fb43-235">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="4fb43-235">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="4fb43-236">**Sidtypecomputer** (9)</span><span class="sxs-lookup"><span data-stu-id="4fb43-236">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4fb43-237">**Status**</span><span class="sxs-lookup"><span data-stu-id="4fb43-237">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb43-238">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4fb43-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fb43-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb43-240">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="4fb43-240">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4fb43-241">Aktueller Status eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="4fb43-241">Current status of an object.</span></span> <span data-ttu-id="4fb43-242">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="4fb43-242">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="4fb43-243">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail". dabei handelt es sich um ein Element, z. b. ein intelligent-fähiges Festplattenlaufwerk, das möglicherweise ordnungsgemäß funktioniert, aber in naher Zukunft einen Fehler vorhersagt.</span><span class="sxs-lookup"><span data-stu-id="4fb43-243">Operational statuses include: "OK", "Degraded", and "Pred Fail", which is an element such as a SMART-enabled hard disk drive that may be functioning properly, but predicts a failure in the near future.</span></span> <span data-ttu-id="4fb43-244">Nicht operative Status sind: "Error", "Starting", "Stop" und "Service". Diese können während der Spiegelung von Spiegelung eines Datenträgers, erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="4fb43-244">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service", which can apply during mirror resilvering of a disk, reloading a user permissions list, or other administrative work.</span></span>

<span data-ttu-id="4fb43-245">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4fb43-245">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4fb43-246">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="4fb43-246">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4fb43-247">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="4fb43-247">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4fb43-248">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="4fb43-248">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4fb43-249">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="4fb43-249">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4fb43-250">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="4fb43-250">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4fb43-251">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="4fb43-251">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4fb43-252">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="4fb43-252">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4fb43-253">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="4fb43-253">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4fb43-254">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="4fb43-254">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4fb43-255">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="4fb43-255">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4fb43-256">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="4fb43-256">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4fb43-257">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="4fb43-257">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4fb43-258">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="4fb43-258">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="4fb43-259"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4fb43-259"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="4fb43-260">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fb43-260">Remarks</span></span>

<span data-ttu-id="4fb43-261">Die **Win32 \_ User Account** -Klasse wird vom [**Win32- \_ Konto**](win32-account.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4fb43-261">The **Win32\_UserAccount** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

> [!Note]  
> <span data-ttu-id="4fb43-262">Bei dem Versuch, in eine schreibgeschützte Eigenschaft zu schreiben, wird kein Fehler zurückgegeben, und der Wert der Eigenschaft bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="4fb43-262">An error is not returned for an attempt to write to a read-only property, and the value of the property remains unchanged.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4fb43-263">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4fb43-263">Examples</span></span>

<span data-ttu-id="4fb43-264">In der [Liste lokale Benutzerkonten mit WMI](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) VBScript in der TechNet Gallery auflisten werden die Informationen zu den lokalen Benutzerkonten, die auf einem Computer gefunden werden, mithilfe des Win32-Benutzer **\_ Kontos** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4fb43-264">The [List Local User Accounts Using WMI](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) VBScript code sample on TechNet Gallery uses **Win32\_UserAccount** to Returns information about the local user accounts found on a computer.</span></span>

<span data-ttu-id="4fb43-265">[Die Übersetzung der SID in das Benutzerkonto und das Benutzerkonto in sid](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) PowerShell-Codebeispiel in der TechNet Gallery verwendet **Win32 \_ Useraccount** , um eine SID in ein Benutzerkonto und/oder ein Benutzerkonto in sid zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="4fb43-265">[The Translate SID to User Account and User Account to SID](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) PowerShell code sample on TechNet Gallery uses **Win32\_UserAccount** to translate a SID to User Account and/or a User Account to SID.</span></span>

<span data-ttu-id="4fb43-266">Im folgenden VBScript-Codebeispiel wird gezeigt, wie Sie den vollständigen Namen eines Benutzers auf einem lokalen Computer erhalten.</span><span class="sxs-lookup"><span data-stu-id="4fb43-266">The following VBScript code example shows you how to get the full name of a user on a local computer.</span></span> <span data-ttu-id="4fb43-267">Der vollständige Name ist der Name der menschlichen Sprache, z. b., wenn eine Person den Benutzernamen "kensanchez" hat und der vollständige Name "Ken Sanchez" ist, geben Sie den tatsächlichen Domänen Namen und den Benutzernamen für "MyDomainName" und "MyUserName" ein.</span><span class="sxs-lookup"><span data-stu-id="4fb43-267">The full name is the human language name, for example, a person may have the user name of "kensanchez" and the full name may be "Ken Sanchez", so you substitute the real domain name and user name for "MyDomainName" and "MyUserName".</span></span> <span data-ttu-id="4fb43-268">Für eine effiziente Abfrage müssen Sie die Eigenschaften "Domäne" und "Benutzername" angeben.</span><span class="sxs-lookup"><span data-stu-id="4fb43-268">For an efficient query, you must specify both the domain and user name properties.</span></span>

<span data-ttu-id="4fb43-269">Wenn Sie als Administrator auf einem Remote Computer angemeldet sind, können Sie den Namen des Remote Computers für den Cluster (anstelle von ".") zuweisen und dann mithilfe des folgenden Skript Typs den vollständigen Namen eines Benutzerkontos auf einem lokalen Computer – von einem Remote Computer aus erhalten.</span><span class="sxs-lookup"><span data-stu-id="4fb43-269">If you are an administrator on a remote computer, you can assign the name of the remote computer for strComputer (instead of "."), and then use the following type of script to get the full name of a user account on a local computer—from a remote computer.</span></span>


```VB
On Error Resume Next
strComputer = "."

Set objUserAccount = GetObject("winmgmts{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_UserAccount.Domain='MyDomainName',Name='MyUserName' ")

If Err = 0 Then
    WScript.Echo objUserAccount.FullName
Else
    WScript.Echo "No object found" & Err.Number
End If
```




```CSharp
using System.Management;

{
     ManagementScope mgmtScope = new ManagementScope("\\\\.\\Root\\CIMv2");
     ObjectQuery oQuery = new ObjectQuery("SELECT * FROM Win32_UserAccount Where Name=\"myUserName\"");
     ManagementObjectSearcher mgmtSearch = new ManagementObjectSearcher(mgmtScope, oQuery);
     ManagementObjectCollection objCollection = mgmtSearch.Get();
     foreach (ManagementObject mgmtObject in objCollection)
     {
          Console.WriteLine("Full Name : {0}", mgmtObject["FullName"]);
     }
}
```



## <a name="requirements"></a><span data-ttu-id="4fb43-270">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fb43-270">Requirements</span></span>



| <span data-ttu-id="4fb43-271">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fb43-271">Requirement</span></span> | <span data-ttu-id="4fb43-272">Wert</span><span class="sxs-lookup"><span data-stu-id="4fb43-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb43-273">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fb43-273">Minimum supported client</span></span><br/> | <span data-ttu-id="4fb43-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4fb43-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4fb43-275">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fb43-275">Minimum supported server</span></span><br/> | <span data-ttu-id="4fb43-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fb43-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4fb43-277">Namespace</span><span class="sxs-lookup"><span data-stu-id="4fb43-277">Namespace</span></span><br/>                | <span data-ttu-id="4fb43-278">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4fb43-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4fb43-279">MOF</span><span class="sxs-lookup"><span data-stu-id="4fb43-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fb43-280"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4fb43-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fb43-281">DLL</span><span class="sxs-lookup"><span data-stu-id="4fb43-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fb43-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fb43-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fb43-283">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fb43-283">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb43-284">**Win32- \_ Konto**</span><span class="sxs-lookup"><span data-stu-id="4fb43-284">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

[<span data-ttu-id="4fb43-285">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="4fb43-285">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

---
description: Stellt Daten zu einem Gruppenkonto dar.
ms.assetid: a53d1276-3dc9-419a-bbb8-5dd07794a971
ms.tgt_platform: multiple
title: Win32_Group-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group
- Win32_Group.Caption
- Win32_Group.Description
- Win32_Group.InstallDate
- Win32_Group.Status
- Win32_Group.LocalAccount
- Win32_Group.SID
- Win32_Group.SIDType
- Win32_Group.Domain
- Win32_Group.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8849ba149e0de570150682d3afbad3a4ee33f36
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127329"
---
# <a name="win32_group-class"></a><span data-ttu-id="78980-103">Win32- \_ Gruppenklasse</span><span class="sxs-lookup"><span data-stu-id="78980-103">Win32\_Group class</span></span>

<span data-ttu-id="78980-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) der **Win32- \_ Gruppe** stellt Daten zu einem Gruppenkonto dar.</span><span class="sxs-lookup"><span data-stu-id="78980-104">The **Win32\_Group** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents data about a group account.</span></span> <span data-ttu-id="78980-105">Mit einem Gruppenkonto können Zugriffsberechtigungen für eine Liste von Benutzern geändert werden.</span><span class="sxs-lookup"><span data-stu-id="78980-105">A group account allows access privileges to be changed for a list of users.</span></span> <span data-ttu-id="78980-106">Beispiel: Marketing2.</span><span class="sxs-lookup"><span data-stu-id="78980-106">Example: Marketing2.</span></span>

<span data-ttu-id="78980-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="78980-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="78980-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="78980-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="78980-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="78980-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Group : Win32_Account
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  LocalAccount;
  string   SID;
  uint8    SIDType;
  string   Domain;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="78980-110">Member</span><span class="sxs-lookup"><span data-stu-id="78980-110">Members</span></span>

<span data-ttu-id="78980-111">Die **Win32- \_ Gruppen** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="78980-111">The **Win32\_Group** class has these types of members:</span></span>

-   [<span data-ttu-id="78980-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="78980-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="78980-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78980-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="78980-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="78980-114">Methods</span></span>

<span data-ttu-id="78980-115">Die **Win32- \_ Gruppen** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="78980-115">The **Win32\_Group** class has these methods.</span></span>



| <span data-ttu-id="78980-116">Methode</span><span class="sxs-lookup"><span data-stu-id="78980-116">Method</span></span>                                               | <span data-ttu-id="78980-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78980-117">Description</span></span>                        |
|:-----------------------------------------------------|:-----------------------------------|
| [<span data-ttu-id="78980-118">**Benen**</span><span class="sxs-lookup"><span data-stu-id="78980-118">**Rename**</span></span>](rename-method-in-class-win32-group.md) | <span data-ttu-id="78980-119">Ändert den Gruppennamen.</span><span class="sxs-lookup"><span data-stu-id="78980-119">Changes the group name.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="78980-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78980-120">Properties</span></span>

<span data-ttu-id="78980-121">Die **Win32- \_ Gruppen** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="78980-121">The **Win32\_Group** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78980-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="78980-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78980-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78980-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78980-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78980-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78980-125">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="78980-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="78980-126">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="78980-126">A short textual description of the object.</span></span>

<span data-ttu-id="78980-127">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="78980-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78980-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78980-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78980-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78980-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78980-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78980-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78980-131">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="78980-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="78980-132">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="78980-132">A textual description of the object.</span></span>

<span data-ttu-id="78980-133">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="78980-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78980-134">**Domäne**</span><span class="sxs-lookup"><span data-stu-id="78980-134">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78980-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78980-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78980-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78980-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78980-137">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Domäne"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Functions \| Domain Name")</span><span class="sxs-lookup"><span data-stu-id="78980-137">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Domain"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="78980-138">Der Name der Windows-Domäne, zu der das Gruppenkonto gehört.</span><span class="sxs-lookup"><span data-stu-id="78980-138">Name of the Windows domain to which the group account belongs.</span></span>

<span data-ttu-id="78980-139">Beispiel: "na-Sales"</span><span class="sxs-lookup"><span data-stu-id="78980-139">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="78980-140">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="78980-140">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78980-141">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="78980-141">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="78980-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78980-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78980-143">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="78980-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="78980-144">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="78980-144">Indicates when the object was installed.</span></span> <span data-ttu-id="78980-145">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="78980-145">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="78980-146">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="78980-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78980-147">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="78980-147">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78980-148">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="78980-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78980-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78980-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78980-150">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="78980-150">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="78980-151">**True** gibt an, dass das Konto auf dem lokalen Computer definiert ist.</span><span class="sxs-lookup"><span data-stu-id="78980-151">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="78980-152">Um nur Konten abzurufen, die auf dem lokalen Computer definiert sind, entwerfen Sie eine Abfrage, die die Bedingung "LocalAccount =**true**" enthält.</span><span class="sxs-lookup"><span data-stu-id="78980-152">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

<span data-ttu-id="78980-153">Diese Eigenschaft wird vom [**Win32- \_ Konto**](win32-account.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="78980-153">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="78980-154">**Name**</span><span class="sxs-lookup"><span data-stu-id="78980-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78980-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78980-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78980-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78980-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78980-157">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Name"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| Name")</span><span class="sxs-lookup"><span data-stu-id="78980-157">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="78980-158">Der Name des Windows-Gruppen Kontos in der Domäne, die durch die **Domänen** Eigenschaft dieser Klasse angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="78980-158">Name of the Windows group account on the domain specified by the **Domain** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="78980-159">**SID**</span><span class="sxs-lookup"><span data-stu-id="78980-159">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78980-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78980-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78980-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78980-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78980-162">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Security IDs (SIDs)")</span><span class="sxs-lookup"><span data-stu-id="78980-162">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="78980-163">Sicherheits-ID (SID) für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="78980-163">Security identifier (SID) for this account.</span></span> <span data-ttu-id="78980-164">Eine SID ist ein Zeichen folgen Wert mit variabler Länge, der zum Identifizieren eines Vertrauens nehmers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78980-164">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="78980-165">Jedes Konto verfügt über eine eindeutige SID, die von einer Zertifizierungsstelle (z. b. einer Windows-Domäne) ausgestellt wurde und in einer Sicherheitsdatenbank gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="78980-165">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="78980-166">Wenn ein Benutzer sich anmeldet, ruft das System die SID des Benutzers aus der Datenbank ab und legt Sie im Zugriffs Token des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="78980-166">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="78980-167">Das System verwendet die SID im Zugriffs Token des Benutzers, um den Benutzer bei allen nachfolgenden Interaktionen mit der Windows-Sicherheit zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="78980-167">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="78980-168">Wenn eine SID als eindeutiger Bezeichner für einen Benutzer oder eine Gruppe verwendet wurde, kann Sie nicht erneut verwendet werden, um einen anderen Benutzer oder eine andere Gruppe zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="78980-168">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

<span data-ttu-id="78980-169">Diese Eigenschaft wird vom [**Win32- \_ Konto**](win32-account.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="78980-169">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="78980-170">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="78980-170">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78980-171">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="78980-171">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="78980-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78980-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78980-173">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Access Control Enumerationstypen- \| sid- \_ Name \_ verwenden")</span><span class="sxs-lookup"><span data-stu-id="78980-173">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="78980-174">Enumerationswerte, die den Typ der Sicherheits-ID (SID) angeben.</span><span class="sxs-lookup"><span data-stu-id="78980-174">Enumerated values that specify the type of security identifier (SID).</span></span>

<span data-ttu-id="78980-175">Diese Eigenschaft wird vom [**Win32- \_ Konto**](win32-account.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="78980-175">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="78980-176">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="78980-176">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="78980-177">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="78980-177">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="78980-178">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="78980-178">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="78980-179">**Sidtypealias** (4)</span><span class="sxs-lookup"><span data-stu-id="78980-179">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="78980-180">**Sidtypewellknowngroup** (5)</span><span class="sxs-lookup"><span data-stu-id="78980-180">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="78980-181">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="78980-181">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="78980-182">**Sidtypeingabe valid** (7)</span><span class="sxs-lookup"><span data-stu-id="78980-182">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="78980-183">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="78980-183">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="78980-184">**Sidtypecomputer** (9)</span><span class="sxs-lookup"><span data-stu-id="78980-184">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="78980-185">**Status**</span><span class="sxs-lookup"><span data-stu-id="78980-185">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78980-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78980-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78980-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78980-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78980-188">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="78980-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="78980-189">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="78980-189">String that indicates the current status of the object.</span></span> <span data-ttu-id="78980-190">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="78980-190">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="78980-191">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="78980-191">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="78980-192">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="78980-192">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="78980-193">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="78980-193">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="78980-194">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="78980-194">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="78980-195">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="78980-195">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="78980-196">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="78980-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="78980-197">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="78980-197">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="78980-198">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="78980-198">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="78980-199">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="78980-199">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="78980-200">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="78980-200">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78980-201">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="78980-201">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="78980-202">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="78980-202">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="78980-203">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="78980-203">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="78980-204">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="78980-204">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="78980-205">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="78980-205">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="78980-206">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="78980-206">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="78980-207">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="78980-207">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="78980-208">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="78980-208">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="78980-209">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="78980-209">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="78980-210"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="78980-210"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="78980-211">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78980-211">Remarks</span></span>

<span data-ttu-id="78980-212">Die **Win32- \_ Gruppen** Klasse wird vom [**Win32- \_ Konto**](win32-account.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="78980-212">The **Win32\_Group** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

## <a name="examples"></a><span data-ttu-id="78980-213">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78980-213">Examples</span></span>

<span data-ttu-id="78980-214">Der folgende Code, der aus der [Liste lokale Gruppen mit WMI](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) VBScript in der TechNet-Galerie stammt, verwendet die **Win32- \_ Gruppe** , um Informationen zu den lokalen Gruppen auf einem Computer zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="78980-214">The following code, taken from the [List Local Groups Using WMI](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) VBScript code example on TechNet Gallery, uses **Win32\_Group** to return information about the local groups found on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_Group  Where LocalAccount = True") 
 
For Each objItem in colItems 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Domain: " & objItem.Domain 
    Wscript.Echo "Local Account: " & objItem.LocalAccount 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "SID: " & objItem.SID 
    Wscript.Echo "SID Type: " & objItem.SIDType 
    Wscript.Echo "Status: " & objItem.Status 
    Wscript.Echo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="78980-215">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78980-215">Requirements</span></span>



| <span data-ttu-id="78980-216">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78980-216">Requirement</span></span> | <span data-ttu-id="78980-217">Wert</span><span class="sxs-lookup"><span data-stu-id="78980-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78980-218">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78980-218">Minimum supported client</span></span><br/> | <span data-ttu-id="78980-219">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78980-219">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78980-220">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78980-220">Minimum supported server</span></span><br/> | <span data-ttu-id="78980-221">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78980-221">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78980-222">Namespace</span><span class="sxs-lookup"><span data-stu-id="78980-222">Namespace</span></span><br/>                | <span data-ttu-id="78980-223">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="78980-223">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="78980-224">MOF</span><span class="sxs-lookup"><span data-stu-id="78980-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78980-225"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="78980-225"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="78980-226">DLL</span><span class="sxs-lookup"><span data-stu-id="78980-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78980-227"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78980-227"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78980-228">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78980-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78980-229">**Win32- \_ Konto**</span><span class="sxs-lookup"><span data-stu-id="78980-229">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

<span data-ttu-id="78980-230">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78980-230">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 


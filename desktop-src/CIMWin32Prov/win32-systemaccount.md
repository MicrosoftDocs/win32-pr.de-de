---
description: Das Win32- \_ Systemkonto&\# 8194; Die WMI-Klasse stellt ein Systemkonto dar.
ms.assetid: 0f745d93-cbac-428e-bf27-56f6e97d529f
ms.tgt_platform: multiple
title: Win32_SystemAccount-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemAccount
- Win32_SystemAccount.Caption
- Win32_SystemAccount.Description
- Win32_SystemAccount.InstallDate
- Win32_SystemAccount.Status
- Win32_SystemAccount.LocalAccount
- Win32_SystemAccount.SID
- Win32_SystemAccount.SIDType
- Win32_SystemAccount.Domain
- Win32_SystemAccount.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ef246a0ee372c5755aeb30980095e7f2f6ca1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343191"
---
# <a name="win32_systemaccount-class"></a><span data-ttu-id="7e9be-103">Win32- \_ SYSTEMACCOUNT-Klasse</span><span class="sxs-lookup"><span data-stu-id="7e9be-103">Win32\_SystemAccount class</span></span>

<span data-ttu-id="7e9be-104">Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) für das Win32-System **\_ Konto** stellt ein Systemkonto dar.</span><span class="sxs-lookup"><span data-stu-id="7e9be-104">The **Win32\_SystemAccount** [WMI class](../wmisdk/retrieving-a-class.md) represents a system account.</span></span> <span data-ttu-id="7e9be-105">Das Systemkonto wird vom Betriebssystem und den Diensten verwendet.</span><span class="sxs-lookup"><span data-stu-id="7e9be-105">The system account is used by the operating system and services.</span></span> <span data-ttu-id="7e9be-106">In Windows gibt es viele Dienste und Prozesse, die sich intern anmelden müssen, z. b. während einer Windows-Installation.</span><span class="sxs-lookup"><span data-stu-id="7e9be-106">There are many services and processes within Windows that need the capability to logon internally, for example, during a Windows installation.</span></span> <span data-ttu-id="7e9be-107">Das Systemkonto wurde für diesen Zweck entwickelt.</span><span class="sxs-lookup"><span data-stu-id="7e9be-107">The system account was designed for that purpose.</span></span>

<span data-ttu-id="7e9be-108">Das Systemkonto ist ein internes Konto, das nicht im Benutzer-Manager angezeigt wird, keiner Gruppe hinzugefügt werden kann und dem keine Benutzerrechte zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="7e9be-108">The system account is an internal account that does not show up in User Manager, cannot be added to any groups, and cannot have user rights assigned to it.</span></span> <span data-ttu-id="7e9be-109">Das Systemkonto wird jedoch auf einem NTFS-Dateisystem Volume im Datei-Manager angezeigt, das sich im Abschnitt "Berechtigungen" im Menü "Sicherheit" befindet.</span><span class="sxs-lookup"><span data-stu-id="7e9be-109">However, the system account does show up on an NTFS file system volume in file manager, which is located in the Permissions section of the Security menu.</span></span> <span data-ttu-id="7e9be-110">Standardmäßig wird dem Systemkonto Vollzugriff auf alle Dateien auf einem NTFS-Dateisystem Volume gewährt. Dies bedeutet, dass das Systemkonto über die gleichen funktionalen Berechtigungen wie das Administrator Konto verfügt.</span><span class="sxs-lookup"><span data-stu-id="7e9be-110">By default, the system account is granted full control to all files on an NTFS file system volume, which means that the system account has the same functional privileges as the administrator account.</span></span>

<span data-ttu-id="7e9be-111">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7e9be-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7e9be-112">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="7e9be-112">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e9be-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e9be-113">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemAccount : Win32_Account
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

## <a name="members"></a><span data-ttu-id="7e9be-114">Member</span><span class="sxs-lookup"><span data-stu-id="7e9be-114">Members</span></span>

<span data-ttu-id="7e9be-115">Die **Win32- \_ SYSTEMACCOUNT** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7e9be-115">The **Win32\_SystemAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="7e9be-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e9be-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e9be-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e9be-117">Properties</span></span>

<span data-ttu-id="7e9be-118">Die **Win32- \_ SYSTEMACCOUNT** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7e9be-118">The **Win32\_SystemAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e9be-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7e9be-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e9be-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e9be-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e9be-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-122">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7e9be-122">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7e9be-123">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7e9be-123">A short textual description of the object.</span></span>

<span data-ttu-id="7e9be-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e9be-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e9be-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e9be-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e9be-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e9be-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e9be-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-128">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="7e9be-128">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7e9be-129">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7e9be-129">A textual description of the object.</span></span>

<span data-ttu-id="7e9be-130">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e9be-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e9be-131">**Domäne**</span><span class="sxs-lookup"><span data-stu-id="7e9be-131">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e9be-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e9be-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e9be-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-134">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Domäne"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Functions \| Domain Name")</span><span class="sxs-lookup"><span data-stu-id="7e9be-134">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="7e9be-135">Der Name der Windows-Domäne, zu der das Systemkonto gehört.</span><span class="sxs-lookup"><span data-stu-id="7e9be-135">Name of the Windows domain to which the system account belongs.</span></span>

<span data-ttu-id="7e9be-136">Beispiel: "na-Sales"</span><span class="sxs-lookup"><span data-stu-id="7e9be-136">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="7e9be-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7e9be-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e9be-138">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7e9be-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e9be-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-140">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="7e9be-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7e9be-141">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7e9be-141">Indicates when the object was installed.</span></span> <span data-ttu-id="7e9be-142">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7e9be-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7e9be-143">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e9be-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e9be-144">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="7e9be-144">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e9be-145">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7e9be-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e9be-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-147">Qualifizierer: [ **korrigiert**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7e9be-147">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7e9be-148">**True** gibt an, dass das Konto auf dem lokalen Computer definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7e9be-148">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="7e9be-149">Um nur Konten abzurufen, die auf dem lokalen Computer definiert sind, entwerfen Sie eine Abfrage, die die Bedingung "LocalAccount =**true**" enthält.</span><span class="sxs-lookup"><span data-stu-id="7e9be-149">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

<span data-ttu-id="7e9be-150">Diese Eigenschaft wird vom [**Win32- \_ Konto**](win32-account.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e9be-150">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e9be-151">**Name**</span><span class="sxs-lookup"><span data-stu-id="7e9be-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e9be-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e9be-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e9be-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-154">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Name"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| Name")</span><span class="sxs-lookup"><span data-stu-id="7e9be-154">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="7e9be-155">Der Name des Windows-System Kontos in der Domäne, die durch die **Domänen** Eigenschaft dieser Klasse angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7e9be-155">Name of the Windows system account on the domain specified by the **Domain** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="7e9be-156">**SID**</span><span class="sxs-lookup"><span data-stu-id="7e9be-156">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e9be-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e9be-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e9be-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-159">Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Security IDs (SIDs)")</span><span class="sxs-lookup"><span data-stu-id="7e9be-159">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="7e9be-160">Sicherheits-ID (SID) für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="7e9be-160">Security identifier (SID) for this account.</span></span> <span data-ttu-id="7e9be-161">Eine SID ist ein Zeichen folgen Wert mit variabler Länge, der zum Identifizieren eines Vertrauens nehmers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e9be-161">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="7e9be-162">Jedes Konto verfügt über eine eindeutige SID, die von einer Zertifizierungsstelle (z. b. einer Windows-Domäne) ausgestellt wurde und in einer Sicherheitsdatenbank gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7e9be-162">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="7e9be-163">Wenn ein Benutzer sich anmeldet, ruft das System die SID des Benutzers aus der Datenbank ab und legt Sie im Zugriffs Token des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="7e9be-163">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="7e9be-164">Das System verwendet die SID im Zugriffs Token des Benutzers, um den Benutzer bei allen nachfolgenden Interaktionen mit der Windows-Sicherheit zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7e9be-164">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="7e9be-165">Wenn eine SID als eindeutiger Bezeichner für einen Benutzer oder eine Gruppe verwendet wurde, kann Sie nicht erneut verwendet werden, um einen anderen Benutzer oder eine andere Gruppe zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7e9be-165">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

<span data-ttu-id="7e9be-166">Diese Eigenschaft wird vom [**Win32- \_ Konto**](win32-account.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e9be-166">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e9be-167">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="7e9be-167">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e9be-168">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7e9be-168">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e9be-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-170">Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Access Control Enumerationstypen- \| sid- \_ Name \_ verwenden")</span><span class="sxs-lookup"><span data-stu-id="7e9be-170">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="7e9be-171">Enumerationswerte, die den Typ der Sicherheits-ID (SID) angeben.</span><span class="sxs-lookup"><span data-stu-id="7e9be-171">Enumerated values that specify the type of security identifier (SID).</span></span>

<span data-ttu-id="7e9be-172">Diese Eigenschaft wird vom [**Win32- \_ Konto**](win32-account.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e9be-172">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="7e9be-173">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="7e9be-173">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="7e9be-174">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="7e9be-174">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="7e9be-175">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="7e9be-175">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="7e9be-176">**Sidtypealias** (4)</span><span class="sxs-lookup"><span data-stu-id="7e9be-176">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="7e9be-177">**Sidtypewellknowngroup** (5)</span><span class="sxs-lookup"><span data-stu-id="7e9be-177">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="7e9be-178">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="7e9be-178">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="7e9be-179">**Sidtypeingabe valid** (7)</span><span class="sxs-lookup"><span data-stu-id="7e9be-179">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="7e9be-180">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="7e9be-180">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="7e9be-181">**Sidtypecomputer** (9)</span><span class="sxs-lookup"><span data-stu-id="7e9be-181">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e9be-182">**Status**</span><span class="sxs-lookup"><span data-stu-id="7e9be-182">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e9be-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e9be-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e9be-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e9be-185">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="7e9be-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7e9be-186">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="7e9be-186">String that indicates the current status of the object.</span></span> <span data-ttu-id="7e9be-187">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7e9be-187">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7e9be-188">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="7e9be-188">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7e9be-189">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="7e9be-189">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7e9be-190">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="7e9be-190">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7e9be-191">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="7e9be-191">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7e9be-192">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="7e9be-192">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7e9be-193">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e9be-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7e9be-194">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="7e9be-194">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7e9be-195">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="7e9be-195">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7e9be-196">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="7e9be-196">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7e9be-197">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="7e9be-197">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7e9be-198">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="7e9be-198">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7e9be-199">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="7e9be-199">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7e9be-200">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="7e9be-200">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7e9be-201">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="7e9be-201">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7e9be-202">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="7e9be-202">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7e9be-203">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="7e9be-203">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7e9be-204">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="7e9be-204">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7e9be-205">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="7e9be-205">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7e9be-206">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="7e9be-206">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="7e9be-207"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7e9be-207"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="7e9be-208">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e9be-208">Remarks</span></span>

<span data-ttu-id="7e9be-209">Die **Win32- \_ SYSTEMACCOUNT** -Klasse wird vom [**Win32- \_ Konto**](win32-account.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7e9be-209">The **Win32\_SystemAccount** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e9be-210">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e9be-210">Requirements</span></span>



| <span data-ttu-id="7e9be-211">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e9be-211">Requirement</span></span> | <span data-ttu-id="7e9be-212">Wert</span><span class="sxs-lookup"><span data-stu-id="7e9be-212">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e9be-213">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e9be-213">Minimum supported client</span></span><br/> | <span data-ttu-id="7e9be-214">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e9be-214">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7e9be-215">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e9be-215">Minimum supported server</span></span><br/> | <span data-ttu-id="7e9be-216">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e9be-216">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7e9be-217">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e9be-217">Namespace</span></span><br/>                | <span data-ttu-id="7e9be-218">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7e9be-218">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7e9be-219">MOF</span><span class="sxs-lookup"><span data-stu-id="7e9be-219">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e9be-220"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7e9be-220"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e9be-221">DLL</span><span class="sxs-lookup"><span data-stu-id="7e9be-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e9be-222"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e9be-222"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e9be-223">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e9be-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e9be-224">**Win32- \_ Konto**</span><span class="sxs-lookup"><span data-stu-id="7e9be-224">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

[<span data-ttu-id="7e9be-225">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="7e9be-225">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

---
description: Enthält Informationen zu Benutzerkonten und Gruppenkonten, die dem Computersystem bekannt sind, auf dem Windows ausgeführt wird.
ms.assetid: c0916f20-05be-4282-9642-28cec606bfd7
ms.tgt_platform: multiple
title: Win32_Account-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Account
- Win32_Account.Caption
- Win32_Account.Description
- Win32_Account.Domain
- Win32_Account.InstallDate
- Win32_Account.LocalAccount
- Win32_Account.Name
- Win32_Account.SID
- Win32_Account.SIDType
- Win32_Account.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2af601799095192d7af4ffedce0c8e0cd28bff21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127493"
---
# <a name="win32_account-class"></a><span data-ttu-id="ad7ed-103">Win32- \_ Konto Klasse</span><span class="sxs-lookup"><span data-stu-id="ad7ed-103">Win32\_Account class</span></span>

<span data-ttu-id="ad7ed-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) für das **Win32- \_ Konto** enthält Informationen zu Benutzerkonten und Gruppenkonten, die dem Computersystem bekannt sind, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-104">The **Win32\_Account** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) contains information about user accounts and group accounts known to the computer system running Windows.</span></span> <span data-ttu-id="ad7ed-105">Benutzer-oder Gruppennamen, die von einer Windows-Domäne erkannt werden, sind Nachfolger (oder Member) dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-105">User or group names recognized by a Windows domain are descendants (or members) of this class.</span></span>

<span data-ttu-id="ad7ed-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ad7ed-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad7ed-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad7ed-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4C9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Account : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   Domain;
  datetime InstallDate;
  boolean  LocalAccount;
  string   Name;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="ad7ed-109">Member</span><span class="sxs-lookup"><span data-stu-id="ad7ed-109">Members</span></span>

<span data-ttu-id="ad7ed-110">Die **Win32- \_ Konto** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ad7ed-110">The **Win32\_Account** class has these types of members:</span></span>

-   [<span data-ttu-id="ad7ed-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad7ed-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad7ed-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad7ed-112">Properties</span></span>

<span data-ttu-id="ad7ed-113">Die **Win32- \_ Konto** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-113">The **Win32\_Account** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad7ed-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad7ed-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad7ed-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-117">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ad7ed-118">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-118">Short description of the object.</span></span>

<span data-ttu-id="ad7ed-119">Diese Eigenschaft wird von der [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-119">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ad7ed-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad7ed-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad7ed-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-123">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-123">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ad7ed-124">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-124">Description of the object.</span></span>

<span data-ttu-id="ad7ed-125">Diese Eigenschaft wird von der [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-125">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ad7ed-126">**Domäne**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-126">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad7ed-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad7ed-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-129">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Functions \| Domain")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Functions\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="ad7ed-130">Der Name der Windows-Domäne, zu der eine Gruppe oder ein Benutzer gehört.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-130">Name of the Windows domain to which a group or user belongs.</span></span>

<span data-ttu-id="ad7ed-131">Beispiel: "na-Sales"</span><span class="sxs-lookup"><span data-stu-id="ad7ed-131">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="ad7ed-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad7ed-133">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad7ed-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-135">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-135">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ad7ed-136">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-136">Date and time that the object was installed.</span></span> <span data-ttu-id="ad7ed-137">Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-137">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ad7ed-138">Diese Eigenschaft wird von der [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-138">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ad7ed-139">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-139">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad7ed-140">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ad7ed-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad7ed-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-142">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ad7ed-142">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ad7ed-143">**True** gibt an, dass das Konto auf dem lokalen Computer definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-143">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="ad7ed-144">Um nur Konten abzurufen, die auf dem lokalen Computer definiert sind, entwerfen Sie eine Abfrage, die die Bedingung "LocalAccount =**true**" enthält.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-144">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

</dd> <dt>

<span data-ttu-id="ad7ed-145">**Name**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad7ed-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad7ed-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-148">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| Name")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-148">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="ad7ed-149">Der Name des Windows-System Kontos in der Domäne, die durch die **Domänen** Eigenschaft dieser Klasse angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-149">Name of the Windows system account on the domain specified by the **Domain** property of this class.</span></span> <span data-ttu-id="ad7ed-150">Diese Eigenschaft überschreibt die **Name** -Eigenschaft, die von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-150">This property overrides the **Name** property inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad7ed-151">**SID**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-151">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad7ed-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad7ed-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-154">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Security IDs (SIDs)")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-154">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="ad7ed-155">Sicherheits-ID (SID) für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-155">Security identifier (SID) for this account.</span></span> <span data-ttu-id="ad7ed-156">Eine SID ist ein Zeichen folgen Wert mit variabler Länge, der zum Identifizieren eines Vertrauens nehmers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-156">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="ad7ed-157">Jedes Konto verfügt über eine eindeutige SID, die von einer Zertifizierungsstelle (z. b. einer Windows-Domäne) ausgestellt wurde und in einer Sicherheitsdatenbank gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-157">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="ad7ed-158">Wenn ein Benutzer sich anmeldet, ruft das System die SID des Benutzers aus der Datenbank ab und legt Sie im Zugriffs Token des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-158">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="ad7ed-159">Das System verwendet die SID im Zugriffs Token des Benutzers, um den Benutzer bei allen nachfolgenden Interaktionen mit der Windows-Sicherheit zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-159">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="ad7ed-160">Wenn eine SID als eindeutiger Bezeichner für einen Benutzer oder eine Gruppe verwendet wurde, kann Sie nicht erneut verwendet werden, um einen anderen Benutzer oder eine andere Gruppe zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-160">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

</dd> <dt>

<span data-ttu-id="ad7ed-161">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-161">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad7ed-162">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-162">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad7ed-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-164">Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Access Control Enumerationstypen- \| sid- \_ Name \_ verwenden")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-164">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="ad7ed-165">Enumerationswerte, die den Typ der Sicherheits-ID (SID) angeben.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-165">Enumerated values that specify the type of security identifier (SID).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="ad7ed-166">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="ad7ed-166">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="ad7ed-167">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="ad7ed-167">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="ad7ed-168">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="ad7ed-168">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="ad7ed-169">**Sidtypealias** (4)</span><span class="sxs-lookup"><span data-stu-id="ad7ed-169">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="ad7ed-170">**Sidtypewellknowngroup** (5)</span><span class="sxs-lookup"><span data-stu-id="ad7ed-170">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="ad7ed-171">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="ad7ed-171">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="ad7ed-172">**Sidtypeingabe valid** (7)</span><span class="sxs-lookup"><span data-stu-id="ad7ed-172">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="ad7ed-173">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="ad7ed-173">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="ad7ed-174">**Sidtypecomputer** (9)</span><span class="sxs-lookup"><span data-stu-id="ad7ed-174">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad7ed-175">**Status**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-175">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad7ed-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad7ed-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad7ed-178">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ad7ed-179">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-179">Current status of the object.</span></span> <span data-ttu-id="ad7ed-180">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-180">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ad7ed-181">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein intelligent-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber prognostiziert in naher Zukunft einen Fehler.)</span><span class="sxs-lookup"><span data-stu-id="ad7ed-181">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicts a failure in the near future).</span></span> <span data-ttu-id="ad7ed-182">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="ad7ed-182">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ad7ed-183">Der letztere Dienst kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-183">The latter, "Service", can apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ad7ed-184">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-184">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ad7ed-185">Diese Eigenschaft wird von der [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-185">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

<span data-ttu-id="ad7ed-186">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="ad7ed-186">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ad7ed-187">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-187">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ad7ed-188">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-188">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ad7ed-189">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-189">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ad7ed-190">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-190">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ad7ed-191">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-191">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ad7ed-192">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-192">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ad7ed-193">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-193">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ad7ed-194">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-194">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ad7ed-195">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-195">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ad7ed-196">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-196">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ad7ed-197">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-197">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ad7ed-198">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="ad7ed-198">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="ad7ed-199"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ad7ed-199"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="ad7ed-200">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad7ed-200">Remarks</span></span>

<span data-ttu-id="ad7ed-201">Die **Win32- \_ Konto** Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-201">The **Win32\_Account** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ad7ed-202">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad7ed-202">Examples</span></span>

<span data-ttu-id="ad7ed-203">Mit dem folgenden PowerShell-Code werden die lokalen Konten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-203">The following PowerShell code retrieves the local accounts.</span></span>


```PowerShell
Get-WmiObject Win32_Account -Filter "Domain='$Env:ComputerName'"
```



<span data-ttu-id="ad7ed-204">Mit dem folgenden PowerShell-Code werden die Domänen Konten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-204">The following PowerShell code retrieves the domain accounts.</span></span>


```PowerShell
 Get-WmiObject Win32_Account -Filter "Domain='$Env:UserDomain'" 
```



## <a name="requirements"></a><span data-ttu-id="ad7ed-205">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad7ed-205">Requirements</span></span>



| <span data-ttu-id="ad7ed-206">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad7ed-206">Requirement</span></span> | <span data-ttu-id="ad7ed-207">Wert</span><span class="sxs-lookup"><span data-stu-id="ad7ed-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7ed-208">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad7ed-208">Minimum supported client</span></span><br/> | <span data-ttu-id="ad7ed-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad7ed-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ad7ed-210">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad7ed-210">Minimum supported server</span></span><br/> | <span data-ttu-id="ad7ed-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad7ed-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ad7ed-212">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad7ed-212">Namespace</span></span><br/>                | <span data-ttu-id="ad7ed-213">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ad7ed-213">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ad7ed-214">MOF</span><span class="sxs-lookup"><span data-stu-id="ad7ed-214">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad7ed-215"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ad7ed-215"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad7ed-216">DLL</span><span class="sxs-lookup"><span data-stu-id="ad7ed-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad7ed-217"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad7ed-217"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad7ed-218">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad7ed-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad7ed-219">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="ad7ed-219">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="ad7ed-220">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad7ed-220">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 


---
description: Die Win32 \_ quickfixengineering-&\# 8194; Die WMI-Klasse stellt ein kleines systemweites Update dar, das auf das aktuelle Betriebssystem normalerweise als schnelles Update für die Entwicklung (Quick fixengineering, QFE) bezeichnet wird.
ms.assetid: 84aed428-7620-4f7a-941f-f9d683020d8a
ms.tgt_platform: multiple
title: Win32_QuickFixEngineering-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_QuickFixEngineering
- Win32_QuickFixEngineering.Caption
- Win32_QuickFixEngineering.Description
- Win32_QuickFixEngineering.InstallDate
- Win32_QuickFixEngineering.Name
- Win32_QuickFixEngineering.Status
- Win32_QuickFixEngineering.CSName
- Win32_QuickFixEngineering.FixComments
- Win32_QuickFixEngineering.HotFixID
- Win32_QuickFixEngineering.InstalledBy
- Win32_QuickFixEngineering.InstalledOn
- Win32_QuickFixEngineering.ServicePackInEffect
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0e9db31dd452161a31575b6f7184a34c35dea71e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344809"
---
# <a name="win32_quickfixengineering-class"></a><span data-ttu-id="9b8ed-103">Win32 \_ Quick fixengineering-Klasse</span><span class="sxs-lookup"><span data-stu-id="9b8ed-103">Win32\_QuickFixEngineering class</span></span>

<span data-ttu-id="9b8ed-104">Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32- \_ quickfixengineering** stellt ein kleines systemweites Update dar, das auf das aktuelle Betriebssystem normalerweise als schnellfixentwicklungs-Update (QFE) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-104">The **Win32\_QuickFixEngineering** [WMI class](../wmisdk/retrieving-a-class.md) represents a small system-wide update, commonly referred to as a quick-fix engineering (QFE) update, applied to the current operating system.</span></span> <span data-ttu-id="9b8ed-105">Diese Klasse gibt nur die von der komponentenbasierten Wartung (Component based Wartung, CBS) bereitgestellten Updates zurück.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-105">This class returns only the updates supplied by Component Based Servicing (CBS).</span></span> <span data-ttu-id="9b8ed-106">Diese Updates sind nicht in der Registrierung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-106">These updates are not listed in the registry.</span></span> <span data-ttu-id="9b8ed-107">Von der Microsoft Windows Installer (MSI) oder der Windows Update-Site () bereitgestellte Updates [https://update.microsoft.com](https://update.microsoft.com/) werden von der **Win32- \_ quickfixengineering** nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-107">Updates supplied by Microsoft Windows Installer (MSI) or the Windows update site ([https://update.microsoft.com](https://update.microsoft.com/)) are not returned by **Win32\_QuickFixEngineering**.</span></span>

<span data-ttu-id="9b8ed-108">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9b8ed-109">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b8ed-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b8ed-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A1}"), AMENDMENT]
class Win32_QuickFixEngineering : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CSName;
  string   FixComments;
  string   HotFixID;
  string   InstalledBy;
  string   InstalledOn;
  string   ServicePackInEffect;
};
```

## <a name="members"></a><span data-ttu-id="9b8ed-111">Member</span><span class="sxs-lookup"><span data-stu-id="9b8ed-111">Members</span></span>

<span data-ttu-id="9b8ed-112">Die **Win32 \_ Quick fixengineering** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9b8ed-112">The **Win32\_QuickFixEngineering** class has these types of members:</span></span>

-   [<span data-ttu-id="9b8ed-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b8ed-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b8ed-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b8ed-114">Properties</span></span>

<span data-ttu-id="9b8ed-115">Die **Win32 \_ Quick fixengineering** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-115">The **Win32\_QuickFixEngineering** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b8ed-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8ed-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b8ed-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-119">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-119">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9b8ed-120">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-120">A short textual description of the object.</span></span>

<span data-ttu-id="9b8ed-121">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b8ed-122">**CSName**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-122">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8ed-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b8ed-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-125">Qualifizierer: [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**propagierter**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Computersystem**](cim-computersystem.md).**Name**"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) (" WMI ")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-125">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="9b8ed-126">Lokaler Name des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-126">Local name of the computer system.</span></span> <span data-ttu-id="9b8ed-127">Der Wert für diese Eigenschaft stammt aus der [**CIM \_ Computersystem**](cim-computersystem.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-127">The value for this property comes from the [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="9b8ed-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8ed-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b8ed-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-131">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-131">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9b8ed-132">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-132">A textual description of the object.</span></span>

<span data-ttu-id="9b8ed-133">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b8ed-134">**FixComments**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-134">**FixComments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8ed-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b8ed-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-137">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="9b8ed-138">Zusätzliche Kommentare in Bezug auf das Update.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-138">Additional comments that relate to the update.</span></span>

</dd> <dt>

<span data-ttu-id="9b8ed-139">**HotFixID auszuwählen**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-139">**HotFixID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8ed-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b8ed-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-142">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (260), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-142">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="9b8ed-143">Eindeutiger Bezeichner, der einem bestimmten Update zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-143">Unique identifier associated with a particular update.</span></span>

</dd> <dt>

<span data-ttu-id="9b8ed-144">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-144">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8ed-145">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-145">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b8ed-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-147">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9b8ed-148">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-148">Indicates when the object was installed.</span></span> <span data-ttu-id="9b8ed-149">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-149">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9b8ed-150">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b8ed-151">**InstalledBy**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-151">**InstalledBy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8ed-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b8ed-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-154">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="9b8ed-155">Person, die das Update installiert hat.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-155">Person who installed the update.</span></span> <span data-ttu-id="9b8ed-156">Wenn dieser Wert unbekannt ist, ist die Eigenschaft leer.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-156">If this value is unknown, the property is empty.</span></span>

</dd> <dt>

<span data-ttu-id="9b8ed-157">**InstalledOn**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-157">**InstalledOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8ed-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b8ed-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-160">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="9b8ed-161">Datum, an dem das Update installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-161">Date that the update was installed.</span></span> <span data-ttu-id="9b8ed-162">Wenn dieser Wert unbekannt ist, ist die Eigenschaft leer.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-162">If this value is unknown, the property is empty.</span></span>

> [!Note]  
> <span data-ttu-id="9b8ed-163">Diese Eigenschaft kann abhängig vom Zeitpunkt der Installation der schnell Korrektur verschiedene Formate verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-163">This property may use different formats, depending on when the QuickFix was installed.</span></span> <span data-ttu-id="9b8ed-164">Die meisten Systeme verwenden ein Standard Datumsformat, z. b. "23-10-2013".</span><span class="sxs-lookup"><span data-stu-id="9b8ed-164">Most systems use a standard date format, such as "23-10-2013".</span></span> <span data-ttu-id="9b8ed-165">Einige Systeme geben jedoch möglicherweise einen hexadezimalen 64-Bit-Wert im Win32- [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Format zurück.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-165">However, some systems may return a 64-bit hexidecimal value in the Win32 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) format.</span></span>

 

</dd> <dt>

<span data-ttu-id="9b8ed-166">**Name**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8ed-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b8ed-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-169">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-169">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9b8ed-170">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-170">Label by which the object is known.</span></span> <span data-ttu-id="9b8ed-171">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-171">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9b8ed-172">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b8ed-173">**Servicepackineffect**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-173">**ServicePackInEffect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8ed-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b8ed-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-176">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (260), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-176">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="9b8ed-177">Das Service Pack ist wirksam, als das Update angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-177">Service pack in effect when the update was applied.</span></span> <span data-ttu-id="9b8ed-178">Wenn keine Service Pack angewendet wurde, übernimmt die-Eigenschaft den Wert SP0.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-178">If no service pack has been applied, the property takes on the value SP0.</span></span> <span data-ttu-id="9b8ed-179">Wenn nicht bestimmt werden kann, welche Service Pack in Kraft war, ist diese Eigenschaft **null**.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-179">If it cannot be determined what service pack was in effect, this property is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9b8ed-180">**Status**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-180">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8ed-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b8ed-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8ed-183">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-183">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9b8ed-184">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-184">String that indicates the current status of the object.</span></span> <span data-ttu-id="9b8ed-185">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-185">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="9b8ed-186">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-186">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="9b8ed-187">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="9b8ed-187">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="9b8ed-188">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-188">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9b8ed-189">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-189">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9b8ed-190">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-190">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9b8ed-191">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9b8ed-192">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="9b8ed-192">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9b8ed-193">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-193">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9b8ed-194">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-194">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9b8ed-195">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-195">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b8ed-196">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-196">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9b8ed-197">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-197">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9b8ed-198">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-198">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9b8ed-199">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-199">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9b8ed-200">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-200">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9b8ed-201">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-201">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9b8ed-202">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-202">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9b8ed-203">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-203">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9b8ed-204">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="9b8ed-204">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="9b8ed-205"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9b8ed-205"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="9b8ed-206">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b8ed-206">Remarks</span></span>

<span data-ttu-id="9b8ed-207">Die **Win32- \_ quickfixengineering** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-207">The **Win32\_QuickFixEngineering** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="9b8ed-208">Da Updates an zwei Stellen gespeichert werden, kann eine Enumeration dieser Klasse zu Duplikaten führen.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-208">Because updates are stored in two places, an enumeration of this class can result in duplicates.</span></span>

<span data-ttu-id="9b8ed-209">Ein Hotfix ist ein temporäres Betriebssystem Patch, das von der Quick Fix Engineering Group bei Microsoft erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-209">A hot fix is a temporary operating system patch produced by the Quick Fix Engineering group at Microsoft.</span></span> <span data-ttu-id="9b8ed-210">Ebenso wie Service Packs stellen Hotfixes Änderungen dar, die an einer Windows-Version vorgenommen wurden, nachdem das Betriebssystem freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-210">Like service packs, hot fixes represent changes that have been made to a version of Windows after the operating system has been released.</span></span>

<span data-ttu-id="9b8ed-211">Im Gegensatz zu Service Packs sind Hotfixes nicht für die Installation auf allen Computern vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-211">Unlike service packs, hot fixes are not intended for blanket installation on all computers.</span></span> <span data-ttu-id="9b8ed-212">Stattdessen werden Sie entwickelt, um sehr spezifische Probleme zu beheben, häufig für bestimmte Computerkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-212">Instead, they are developed to address very specific problems, often for specific computer configurations.</span></span>

<span data-ttu-id="9b8ed-213">Außerdem stellen Hotfixes unabhängige Installationen dar, die nicht von anderen veröffentlichten Hotfixes abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-213">In addition, hot fixes represent independent installations that do not depend on other released hot fixes.</span></span> <span data-ttu-id="9b8ed-214">Ein hypothetischer Hotfix 4 würde z. b. nicht die Fehlerbehebungen und Funktionen enthalten, die in den Hotfixes 1, 2 und 3 enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-214">For example, a hypothetical hot fix 4 would not include the bug fixes and functionality included in hot fixes 1, 2, and 3.</span></span> <span data-ttu-id="9b8ed-215">In den meisten Fällen ist es auch nicht erforderlich, dass Sie die Hotfixes 1, 2 und 3 installieren, bevor Sie Hot Fix 4 installieren.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-215">In most cases, there would also be no requirement that you install hot fixes 1, 2, and 3 before installing hot fix 4.</span></span> <span data-ttu-id="9b8ed-216">Dadurch wird eine wichtige administrative Aufgabe durch die Enumeration einzelner Hotfixes behoben: um die genaue Konfiguration eines Computers zu ermitteln, müssen Sie nicht nur wissen, welche Service Packs installiert wurden, sondern auch, welche einzelnen Hotfixes installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-216">This makes enumeration of individual hot fixes an important administrative task: to know the exact configuration of a computer, you need to know not only which service packs have been installed but also which individual hot fixes have been installed.</span></span>

<span data-ttu-id="9b8ed-217">Die **Win32 \_ Quick fixengineering** -Klasse ermöglicht es Ihnen, alle Hotfixes aufzulisten, die auf einem Computer installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-217">The **Win32\_QuickFixEngineering** class enables you to enumerate all the hot fixes that have been installed on a computer</span></span>

## <a name="examples"></a><span data-ttu-id="9b8ed-218">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b8ed-218">Examples</span></span>

<span data-ttu-id="9b8ed-219">Das PowerShell-Beispiel [Get installierte Programme](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) gibt eine vollständige Liste der installierten Programme zurück.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-219">The [Get Installed Programs](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) PowerShell example returns a full list of installed programs.</span></span>

<span data-ttu-id="9b8ed-220">Im folgenden VBScript-Beispiel werden die installierten Hotfixes auf einem Computer aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9b8ed-220">The following VBScript sample enumerates the installed hot fixes on a computer</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colQuickFixes = objWMIService.ExecQuery("SELECT * FROM Win32_QuickFixEngineering")
For Each objQuickFix in colQuickFixes
 Wscript.Echo "Computer: " & objQuickFix.CSName
 Wscript.Echo "Description: " & objQuickFix.Description
 Wscript.Echo "Hot Fix ID: " & objQuickFix.HotFixID
 Wscript.Echo "Installation Date: " & objQuickFix.InstallDate
 Wscript.Echo "Installed By: " & objQuickFix.InstalledBy
Next
```



## <a name="requirements"></a><span data-ttu-id="9b8ed-221">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b8ed-221">Requirements</span></span>



| <span data-ttu-id="9b8ed-222">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b8ed-222">Requirement</span></span> | <span data-ttu-id="9b8ed-223">Wert</span><span class="sxs-lookup"><span data-stu-id="9b8ed-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8ed-224">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b8ed-224">Minimum supported client</span></span><br/> | <span data-ttu-id="9b8ed-225">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b8ed-225">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b8ed-226">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b8ed-226">Minimum supported server</span></span><br/> | <span data-ttu-id="9b8ed-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b8ed-227">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b8ed-228">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b8ed-228">Namespace</span></span><br/>                | <span data-ttu-id="9b8ed-229">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9b8ed-229">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b8ed-230">MOF</span><span class="sxs-lookup"><span data-stu-id="9b8ed-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b8ed-231"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9b8ed-231"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b8ed-232">DLL</span><span class="sxs-lookup"><span data-stu-id="9b8ed-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b8ed-233"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b8ed-233"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b8ed-234">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b8ed-234">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b8ed-235">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="9b8ed-235">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="9b8ed-236">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="9b8ed-236">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="9b8ed-237">WMI-Tasks: Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="9b8ed-237">WMI Tasks: Operating Systems</span></span>](../wmisdk/wmi-tasks--operating-systems.md)
</dt> </dl>

 

 

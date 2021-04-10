---
title: Win32_TSGetIcon-Klasse
description: Gibt den Inhalt des Symbols zurück, das durch den Dateipfad und den Index angegeben wird.
ms.assetid: c0ab50f1-f5a9-4f5e-8280-40c638f09e1c
ms.tgt_platform: multiple
keywords:
- Win32_TSGetIcon-Klasse Remotedesktopdienste
- Win32_TSGetIcon Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGetIcon
- Win32_TSGetIcon.Caption
- Win32_TSGetIcon.Description
- Win32_TSGetIcon.InstallDate
- Win32_TSGetIcon.Name
- Win32_TSGetIcon.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0186e158f025be8e8a5e6cf3e87f3ad5d8b296
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956566"
---
# <a name="win32_tsgeticon-class"></a><span data-ttu-id="0dac9-105">Win32-Klasse "- \_ Ticon"</span><span class="sxs-lookup"><span data-stu-id="0dac9-105">Win32\_TSGetIcon class</span></span>

<span data-ttu-id="0dac9-106">Gibt den Inhalt des Symbols zurück, das durch den Dateipfad und Index angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0dac9-106">Returns the contents of the icon specified by file path and index</span></span>

<span data-ttu-id="0dac9-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0dac9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dac9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0dac9-108">Syntax</span></span>

``` syntax
class Win32_TSGetIcon : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="0dac9-109">Member</span><span class="sxs-lookup"><span data-stu-id="0dac9-109">Members</span></span>

<span data-ttu-id="0dac9-110">Die Win32-Klasse " **\_ zgeticon** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0dac9-110">The **Win32\_TSGetIcon** class has these types of members:</span></span>

-   [<span data-ttu-id="0dac9-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="0dac9-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="0dac9-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0dac9-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0dac9-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="0dac9-113">Methods</span></span>

<span data-ttu-id="0dac9-114">Die Win32-Klasse " **\_ zgeticon** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0dac9-114">The **Win32\_TSGetIcon** class has these methods.</span></span>



| <span data-ttu-id="0dac9-115">Methode</span><span class="sxs-lookup"><span data-stu-id="0dac9-115">Method</span></span>                                     | <span data-ttu-id="0dac9-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0dac9-116">Description</span></span>                                            |
|:-------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="0dac9-117">**GetIcon**</span><span class="sxs-lookup"><span data-stu-id="0dac9-117">**GetIcon**</span></span>](geticon-win32-tsgeticon.md) | <span data-ttu-id="0dac9-118">Gibt den Inhalt des angegebenen Symbols zurück.</span><span class="sxs-lookup"><span data-stu-id="0dac9-118">Returns the contents of the specified icon.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0dac9-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0dac9-119">Properties</span></span>

<span data-ttu-id="0dac9-120">Die Win32-Klasse "- **\_ Ticon** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0dac9-120">The **Win32\_TSGetIcon** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0dac9-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0dac9-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dac9-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0dac9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dac9-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0dac9-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0dac9-124">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0dac9-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0dac9-125">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0dac9-125">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0dac9-126">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0dac9-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0dac9-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0dac9-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dac9-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0dac9-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dac9-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0dac9-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dac9-130">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="0dac9-130">Description of the object.</span></span>

<span data-ttu-id="0dac9-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0dac9-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0dac9-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0dac9-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dac9-133">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0dac9-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0dac9-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0dac9-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0dac9-135">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="0dac9-135">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0dac9-136">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0dac9-136">The date the object was installed.</span></span> <span data-ttu-id="0dac9-137">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0dac9-137">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0dac9-138">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0dac9-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0dac9-139">**Name**</span><span class="sxs-lookup"><span data-stu-id="0dac9-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dac9-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0dac9-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dac9-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0dac9-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dac9-142">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="0dac9-142">The name of the object.</span></span>

<span data-ttu-id="0dac9-143">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0dac9-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0dac9-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="0dac9-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dac9-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0dac9-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dac9-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0dac9-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0dac9-147">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0dac9-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0dac9-148">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="0dac9-148">Current status of the object.</span></span> <span data-ttu-id="0dac9-149">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0dac9-149">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0dac9-150">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="0dac9-150">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0dac9-151">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="0dac9-151">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0dac9-152">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="0dac9-152">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0dac9-153">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="0dac9-153">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0dac9-154">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0dac9-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0dac9-155">("OK")</span><span class="sxs-lookup"><span data-stu-id="0dac9-155">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0dac9-156">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="0dac9-156">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0dac9-157">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="0dac9-157">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0dac9-158">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="0dac9-158">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0dac9-159">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="0dac9-159">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0dac9-160">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="0dac9-160">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0dac9-161">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="0dac9-161">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0dac9-162">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="0dac9-162">("Service")</span></span>


<span data-ttu-id="0dac9-163"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0dac9-163"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0dac9-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0dac9-164">Requirements</span></span>



| <span data-ttu-id="0dac9-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0dac9-165">Requirement</span></span> | <span data-ttu-id="0dac9-166">Wert</span><span class="sxs-lookup"><span data-stu-id="0dac9-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dac9-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0dac9-167">Minimum supported client</span></span><br/> | <span data-ttu-id="0dac9-168">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0dac9-168">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0dac9-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0dac9-169">Minimum supported server</span></span><br/> | <span data-ttu-id="0dac9-170">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0dac9-170">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="0dac9-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="0dac9-171">Namespace</span></span><br/>                | <span data-ttu-id="0dac9-172">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0dac9-172">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0dac9-173">MOF</span><span class="sxs-lookup"><span data-stu-id="0dac9-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0dac9-174"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0dac9-174"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="0dac9-175">DLL</span><span class="sxs-lookup"><span data-stu-id="0dac9-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dac9-176"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dac9-176"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 


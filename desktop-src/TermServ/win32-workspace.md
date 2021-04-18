---
title: Win32_Workspace-Klasse
description: Gibt Remotedesktopdienste Konfigurationsinformationen für den Arbeitsbereich an.
ms.assetid: 27192dca-cbb4-4620-ae52-c27aba4b4dff
ms.tgt_platform: multiple
keywords:
- Win32_Workspace-Klasse Remotedesktopdienste
- Win32_Workspace Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_Workspace
- Win32_Workspace.Caption
- Win32_Workspace.Description
- Win32_Workspace.InstallDate
- Win32_Workspace.Name
- Win32_Workspace.Status
- Win32_Workspace.IsDefaultName
- Win32_Workspace.ID
- Win32_Workspace.Redirector
- Win32_Workspace.RedirectorAlternateAddress
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1153a4eb8a260e539845a9458a5c8cee4581d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337906"
---
# <a name="win32_workspace-class"></a><span data-ttu-id="c2375-105">Win32- \_ Arbeitsbereichs Klasse</span><span class="sxs-lookup"><span data-stu-id="c2375-105">Win32\_Workspace class</span></span>

<span data-ttu-id="c2375-106">Gibt Remotedesktopdienste Konfigurationsinformationen für den Arbeitsbereich an.</span><span class="sxs-lookup"><span data-stu-id="c2375-106">Specifies Remote Desktop Services workspace configuration information.</span></span>

<span data-ttu-id="c2375-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c2375-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2375-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2375-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov"), singleton]
class Win32_Workspace : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  IsDefaultName;
  string   ID;
  string   Redirector;
  string   RedirectorAlternateAddress;
};
```

## <a name="members"></a><span data-ttu-id="c2375-109">Member</span><span class="sxs-lookup"><span data-stu-id="c2375-109">Members</span></span>

<span data-ttu-id="c2375-110">Die **Win32- \_ Arbeits** Bereichs Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c2375-110">The **Win32\_Workspace** class has these types of members:</span></span>

-   [<span data-ttu-id="c2375-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2375-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2375-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2375-112">Properties</span></span>

<span data-ttu-id="c2375-113">Die **Win32- \_ Arbeits** Bereichs Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c2375-113">The **Win32\_Workspace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2375-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c2375-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2375-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2375-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2375-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2375-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2375-117">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c2375-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c2375-118">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c2375-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="c2375-119">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2375-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2375-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c2375-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2375-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2375-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2375-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2375-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2375-123">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c2375-123">Description of the object.</span></span>

<span data-ttu-id="c2375-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2375-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2375-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="c2375-125">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2375-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2375-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2375-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c2375-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c2375-128">Der Bezeichner des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="c2375-128">The identifier of the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="c2375-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c2375-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2375-130">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c2375-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c2375-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2375-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2375-132">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="c2375-132">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="c2375-133">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c2375-133">The date the object was installed.</span></span> <span data-ttu-id="c2375-134">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c2375-134">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c2375-135">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2375-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2375-136">**Isdefaultname**</span><span class="sxs-lookup"><span data-stu-id="c2375-136">**IsDefaultName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2375-137">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c2375-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2375-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2375-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2375-139">Gibt an, ob der Arbeitsbereichs Name der Standardname ist.</span><span class="sxs-lookup"><span data-stu-id="c2375-139">Specifies if the workspace name is the default name.</span></span> <span data-ttu-id="c2375-140">Enthält einen Wert ungleich 0 (null), wenn der Name ein Standardname ist, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="c2375-140">Contains nonzero if the name is a default name or zero otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="c2375-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="c2375-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2375-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2375-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2375-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2375-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2375-144">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c2375-144">The name of the object.</span></span>

<span data-ttu-id="c2375-145">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2375-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2375-146">**Redirector**</span><span class="sxs-lookup"><span data-stu-id="c2375-146">**Redirector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2375-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2375-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2375-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c2375-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c2375-149">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c2375-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c2375-150">Der Computername des Redirectors für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="c2375-150">The machine name of the redirector for the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="c2375-151">**Redirectorieaddress**</span><span class="sxs-lookup"><span data-stu-id="c2375-151">**RedirectorAlternateAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2375-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2375-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2375-153">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c2375-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c2375-154">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c2375-154">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c2375-155">Die alternative Adresse für den Redirector.</span><span class="sxs-lookup"><span data-stu-id="c2375-155">The alternate address for the redirector.</span></span>

</dd> <dt>

<span data-ttu-id="c2375-156">**Status**</span><span class="sxs-lookup"><span data-stu-id="c2375-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2375-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2375-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2375-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2375-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2375-159">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="c2375-159">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c2375-160">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c2375-160">Current status of the object.</span></span> <span data-ttu-id="c2375-161">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c2375-161">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c2375-162">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="c2375-162">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c2375-163">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="c2375-163">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c2375-164">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2375-164">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c2375-165">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="c2375-165">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c2375-166">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2375-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="c2375-167">("OK")</span><span class="sxs-lookup"><span data-stu-id="c2375-167">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c2375-168">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="c2375-168">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c2375-169">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="c2375-169">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c2375-170">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c2375-170">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c2375-171">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c2375-171">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c2375-172">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="c2375-172">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c2375-173">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="c2375-173">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c2375-174">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="c2375-174">("Service")</span></span>


<span data-ttu-id="c2375-175"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c2375-175"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c2375-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2375-176">Requirements</span></span>



| <span data-ttu-id="c2375-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2375-177">Requirement</span></span> | <span data-ttu-id="c2375-178">Wert</span><span class="sxs-lookup"><span data-stu-id="c2375-178">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2375-179">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2375-179">Minimum supported client</span></span><br/> | <span data-ttu-id="c2375-180">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c2375-180">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c2375-181">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2375-181">Minimum supported server</span></span><br/> | <span data-ttu-id="c2375-182">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2375-182">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="c2375-183">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2375-183">Namespace</span></span><br/>                | <span data-ttu-id="c2375-184">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c2375-184">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c2375-185">MOF</span><span class="sxs-lookup"><span data-stu-id="c2375-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2375-186"><dt>Tscpub. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c2375-186"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="c2375-187">DLL</span><span class="sxs-lookup"><span data-stu-id="c2375-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2375-188"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2375-188"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 


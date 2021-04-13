---
title: CIM_LogicalElement-Klasse (Remotedesktopdienste)
description: Die Basisklasse für alle Systemkomponenten, die abstrakte Systemkomponenten, z. b. profile, Prozesse oder Systemfunktionen, in Form logischer Geräte darstellen.
ms.assetid: 21e4a2ba-7bc5-4e33-a888-198299137da6
ms.tgt_platform: multiple
keywords:
- CIM_LogicalElement-Klasse Remotedesktopdienste
- CIM_LogicalElement Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- CIM_LogicalElement
- CIM_LogicalElement.Caption
- CIM_LogicalElement.Description
- CIM_LogicalElement.InstallDate
- CIM_LogicalElement.Name
- CIM_LogicalElement.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f7e58fe64f3b9dbb76a11d308aadbe6ce50331f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391626"
---
# <a name="cim_logicalelement-class-remote-desktop-services"></a><span data-ttu-id="c373d-105">CIM_LogicalElement-Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="c373d-105">CIM_LogicalElement class (Remote Desktop Services)</span></span>

<span data-ttu-id="c373d-106">Die Basisklasse für alle Systemkomponenten, die abstrakte Systemkomponenten, z. b. profile, Prozesse oder Systemfunktionen, in Form logischer Geräte darstellen.</span><span class="sxs-lookup"><span data-stu-id="c373d-106">The base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

<span data-ttu-id="c373d-107">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c373d-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c373d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c373d-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="c373d-109">Member</span><span class="sxs-lookup"><span data-stu-id="c373d-109">Members</span></span>

<span data-ttu-id="c373d-110">Die **CIM \_ LogicalElement** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c373d-110">The **CIM\_LogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="c373d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c373d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c373d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c373d-112">Properties</span></span>

<span data-ttu-id="c373d-113">Die **CIM \_ LogicalElement** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c373d-113">The **CIM\_LogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c373d-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c373d-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c373d-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c373d-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c373d-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c373d-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c373d-117">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c373d-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c373d-118">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c373d-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="c373d-119">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c373d-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c373d-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c373d-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c373d-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c373d-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c373d-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c373d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c373d-123">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c373d-123">Description of the object.</span></span>

<span data-ttu-id="c373d-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c373d-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c373d-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c373d-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c373d-126">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c373d-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c373d-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c373d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c373d-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="c373d-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="c373d-129">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c373d-129">The date the object was installed.</span></span> <span data-ttu-id="c373d-130">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c373d-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c373d-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c373d-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c373d-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="c373d-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c373d-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c373d-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c373d-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c373d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c373d-135">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c373d-135">The name of the object.</span></span>

<span data-ttu-id="c373d-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c373d-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c373d-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="c373d-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c373d-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c373d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c373d-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c373d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c373d-140">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="c373d-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c373d-141">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c373d-141">Current status of the object.</span></span> <span data-ttu-id="c373d-142">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c373d-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c373d-143">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="c373d-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c373d-144">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="c373d-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c373d-145">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c373d-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c373d-146">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="c373d-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c373d-147">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c373d-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="c373d-148">("OK")</span><span class="sxs-lookup"><span data-stu-id="c373d-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c373d-149">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="c373d-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c373d-150">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="c373d-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c373d-151">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c373d-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c373d-152">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c373d-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c373d-153">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="c373d-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c373d-154">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="c373d-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c373d-155">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="c373d-155">("Service")</span></span>


<span data-ttu-id="c373d-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c373d-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c373d-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c373d-157">Requirements</span></span>



| <span data-ttu-id="c373d-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c373d-158">Requirement</span></span> | <span data-ttu-id="c373d-159">Wert</span><span class="sxs-lookup"><span data-stu-id="c373d-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c373d-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c373d-160">Minimum supported client</span></span><br/> | <span data-ttu-id="c373d-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c373d-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c373d-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c373d-162">Minimum supported server</span></span><br/> | <span data-ttu-id="c373d-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c373d-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c373d-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="c373d-164">Namespace</span></span><br/>                | <span data-ttu-id="c373d-165">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c373d-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c373d-166">MOF</span><span class="sxs-lookup"><span data-stu-id="c373d-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c373d-167"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c373d-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c373d-168">DLL</span><span class="sxs-lookup"><span data-stu-id="c373d-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c373d-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c373d-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c373d-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c373d-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c373d-171">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="c373d-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 


---
title: CIM_Setting-Klasse (Remotedesktopdienste)
description: Stellt Konfigurations bezogene und operative Parameter für ein oder mehrere verwaltete Systemelemente dar.
ms.assetid: d0007762-5d13-421b-a73a-3392a77686a6
ms.tgt_platform: multiple
keywords:
- CIM_Setting-Klasse Remotedesktopdienste
- CIM_Setting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.InstallDate
- CIM_Setting.Name
- CIM_Setting.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d3a9517df9af92f428000ed064b2bb88b348a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340982"
---
# <a name="cim_setting-class-remote-desktop-services"></a><span data-ttu-id="1e33e-105">CIM_Setting-Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="1e33e-105">CIM_Setting class (Remote Desktop Services)</span></span>

<span data-ttu-id="1e33e-106">Stellt Konfigurations bezogene und operative Parameter für ein oder mehrere verwaltete Systemelemente dar.</span><span class="sxs-lookup"><span data-stu-id="1e33e-106">Represents configuration-related and operational parameters for one or more managed system elements.</span></span>

<span data-ttu-id="1e33e-107">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="1e33e-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e33e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e33e-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="1e33e-109">Member</span><span class="sxs-lookup"><span data-stu-id="1e33e-109">Members</span></span>

<span data-ttu-id="1e33e-110">Die **CIM- \_ Einstellungs** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1e33e-110">The **CIM\_Setting** class has these types of members:</span></span>

-   [<span data-ttu-id="1e33e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e33e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e33e-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e33e-112">Properties</span></span>

<span data-ttu-id="1e33e-113">Die **CIM- \_ Einstellungs** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1e33e-113">The **CIM\_Setting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e33e-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1e33e-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e33e-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e33e-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e33e-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e33e-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e33e-117">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1e33e-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1e33e-118">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1e33e-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="1e33e-119">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1e33e-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e33e-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1e33e-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e33e-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e33e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e33e-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e33e-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e33e-123">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="1e33e-123">Description of the object.</span></span>

<span data-ttu-id="1e33e-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1e33e-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e33e-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1e33e-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e33e-126">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1e33e-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1e33e-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e33e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e33e-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="1e33e-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="1e33e-129">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1e33e-129">The date the object was installed.</span></span> <span data-ttu-id="1e33e-130">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1e33e-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1e33e-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1e33e-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e33e-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="1e33e-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e33e-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e33e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e33e-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e33e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e33e-135">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="1e33e-135">The name of the object.</span></span>

<span data-ttu-id="1e33e-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1e33e-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e33e-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="1e33e-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e33e-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1e33e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e33e-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1e33e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e33e-140">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="1e33e-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="1e33e-141">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="1e33e-141">Current status of the object.</span></span> <span data-ttu-id="1e33e-142">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1e33e-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1e33e-143">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="1e33e-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1e33e-144">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="1e33e-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1e33e-145">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e33e-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1e33e-146">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="1e33e-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1e33e-147">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1e33e-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="1e33e-148">("OK")</span><span class="sxs-lookup"><span data-stu-id="1e33e-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e33e-149">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="1e33e-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e33e-150">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="1e33e-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e33e-151">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="1e33e-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e33e-152">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="1e33e-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e33e-153">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="1e33e-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e33e-154">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="1e33e-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e33e-155">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="1e33e-155">("Service")</span></span>


<span data-ttu-id="1e33e-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1e33e-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1e33e-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e33e-157">Requirements</span></span>



| <span data-ttu-id="1e33e-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e33e-158">Requirement</span></span> | <span data-ttu-id="1e33e-159">Wert</span><span class="sxs-lookup"><span data-stu-id="1e33e-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e33e-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e33e-160">Minimum supported client</span></span><br/> | <span data-ttu-id="1e33e-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e33e-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e33e-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e33e-162">Minimum supported server</span></span><br/> | <span data-ttu-id="1e33e-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e33e-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e33e-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="1e33e-164">Namespace</span></span><br/>                | <span data-ttu-id="1e33e-165">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1e33e-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1e33e-166">MOF</span><span class="sxs-lookup"><span data-stu-id="1e33e-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e33e-167"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1e33e-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e33e-168">DLL</span><span class="sxs-lookup"><span data-stu-id="1e33e-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e33e-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e33e-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e33e-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e33e-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e33e-171">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="1e33e-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 


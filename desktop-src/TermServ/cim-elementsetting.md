---
title: CIM_ElementSetting-Klasse (Remotedesktopdienste)
description: Stellt die Zuordnung zwischen verwalteten Systemelementen und der Einstellungs Klasse dar, die für Sie definiert ist.
ms.assetid: b74c2fef-0f3a-46b9-9dd8-11016a8f7b57
ms.tgt_platform: multiple
keywords:
- CIM_ElementSetting-Klasse Remotedesktopdienste
- CIM_ElementSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Caption
- CIM_ElementSetting.Description
- CIM_ElementSetting.InstallDate
- CIM_ElementSetting.Name
- CIM_ElementSetting.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9aff40961ddc8fa07de6c49d6c95aefe3d005d6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103103"
---
# <a name="cim_elementsetting-class-remote-desktop-services"></a><span data-ttu-id="8c48f-105">CIM_ElementSetting-Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="8c48f-105">CIM_ElementSetting class (Remote Desktop Services)</span></span>

<span data-ttu-id="8c48f-106">Stellt die Zuordnung zwischen verwalteten Systemelementen und der Einstellungs Klasse dar, die für Sie definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8c48f-106">Represents the association between managed system elements and the setting class defined for them.</span></span>

<span data-ttu-id="8c48f-107">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8c48f-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c48f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c48f-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="8c48f-109">Member</span><span class="sxs-lookup"><span data-stu-id="8c48f-109">Members</span></span>

<span data-ttu-id="8c48f-110">Die **CIM- \_ ElementSetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8c48f-110">The **CIM\_ElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="8c48f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c48f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c48f-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c48f-112">Properties</span></span>

<span data-ttu-id="8c48f-113">Die **CIM- \_ ElementSetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8c48f-113">The **CIM\_ElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c48f-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8c48f-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c48f-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8c48f-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c48f-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c48f-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c48f-117">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8c48f-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8c48f-118">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8c48f-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="8c48f-119">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8c48f-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c48f-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8c48f-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c48f-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8c48f-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c48f-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c48f-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c48f-123">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8c48f-123">Description of the object.</span></span>

<span data-ttu-id="8c48f-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8c48f-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c48f-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8c48f-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c48f-126">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8c48f-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8c48f-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c48f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c48f-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="8c48f-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="8c48f-129">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8c48f-129">The date the object was installed.</span></span> <span data-ttu-id="8c48f-130">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8c48f-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8c48f-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8c48f-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c48f-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="8c48f-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c48f-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8c48f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c48f-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c48f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c48f-135">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8c48f-135">The name of the object.</span></span>

<span data-ttu-id="8c48f-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8c48f-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c48f-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="8c48f-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c48f-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8c48f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c48f-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c48f-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c48f-140">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="8c48f-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="8c48f-141">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8c48f-141">Current status of the object.</span></span> <span data-ttu-id="8c48f-142">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="8c48f-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8c48f-143">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="8c48f-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8c48f-144">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="8c48f-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8c48f-145">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c48f-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8c48f-146">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="8c48f-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8c48f-147">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8c48f-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="8c48f-148">("OK")</span><span class="sxs-lookup"><span data-stu-id="8c48f-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8c48f-149">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="8c48f-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8c48f-150">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="8c48f-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8c48f-151">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="8c48f-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8c48f-152">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8c48f-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8c48f-153">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="8c48f-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8c48f-154">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="8c48f-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8c48f-155">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="8c48f-155">("Service")</span></span>


<span data-ttu-id="8c48f-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8c48f-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="8c48f-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c48f-157">Requirements</span></span>



| <span data-ttu-id="8c48f-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c48f-158">Requirement</span></span> | <span data-ttu-id="8c48f-159">Wert</span><span class="sxs-lookup"><span data-stu-id="8c48f-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c48f-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c48f-160">Minimum supported client</span></span><br/> | <span data-ttu-id="8c48f-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c48f-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c48f-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c48f-162">Minimum supported server</span></span><br/> | <span data-ttu-id="8c48f-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c48f-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c48f-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="8c48f-164">Namespace</span></span><br/>                | <span data-ttu-id="8c48f-165">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8c48f-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8c48f-166">MOF</span><span class="sxs-lookup"><span data-stu-id="8c48f-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c48f-167"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8c48f-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c48f-168">DLL</span><span class="sxs-lookup"><span data-stu-id="8c48f-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c48f-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c48f-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c48f-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c48f-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c48f-171">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="8c48f-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 


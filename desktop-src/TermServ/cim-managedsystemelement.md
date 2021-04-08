---
title: CIM_ManagedSystemElement-Klasse (Remotedesktopdienste)
description: Die Basisklasse für die System Element Hierarchie.
ms.assetid: c71c0441-381f-4a46-864c-9206c43a27d0
ms.tgt_platform: multiple
keywords:
- CIM_ManagedSystemElement-Klasse Remotedesktopdienste
- CIM_ManagedSystemElement Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.Caption
- CIM_ManagedSystemElement.Description
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b242369df24724fdcc31ce925a229dba5bb515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103102"
---
# <a name="cim_managedsystemelement-class-remote-desktop-services"></a><span data-ttu-id="ef024-105">CIM_ManagedSystemElement-Klasse (Remotedesktopdienste)</span><span class="sxs-lookup"><span data-stu-id="ef024-105">CIM_ManagedSystemElement class (Remote Desktop Services)</span></span>

<span data-ttu-id="ef024-106">Die Basisklasse für die System Element Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="ef024-106">The base class for the system element hierarchy.</span></span>

<span data-ttu-id="ef024-107">Jede unterscheidbare Systemkomponente ist ein Kandidat für die Einbindung in diese Klasse.</span><span class="sxs-lookup"><span data-stu-id="ef024-107">Any distinguishable system component is a candidate for inclusion in this class.</span></span> <span data-ttu-id="ef024-108">Beispiele hierfür sind Softwarekomponenten wie z. b. Dateien. Geräte, z. b. Laufwerke und Controller und physische Komponenten, z. b. Chips und Karten</span><span class="sxs-lookup"><span data-stu-id="ef024-108">Examples include software components, such as files; devices, such as disk drives and controllers; and physical components, such as chips and cards</span></span>

<span data-ttu-id="ef024-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ef024-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef024-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef024-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C517-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="ef024-111">Member</span><span class="sxs-lookup"><span data-stu-id="ef024-111">Members</span></span>

<span data-ttu-id="ef024-112">Die **CIM \_ ManagedSystemElement** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ef024-112">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="ef024-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ef024-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef024-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ef024-114">Properties</span></span>

<span data-ttu-id="ef024-115">Die **CIM \_ ManagedSystemElement** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ef024-115">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef024-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ef024-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef024-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef024-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef024-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef024-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef024-119">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ef024-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ef024-120">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ef024-120">Short description (one-line string) of the object.</span></span>

</dd> <dt>

<span data-ttu-id="ef024-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef024-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef024-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef024-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef024-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef024-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef024-124">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ef024-124">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="ef024-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ef024-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef024-126">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ef024-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef024-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef024-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef024-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="ef024-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ef024-129">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ef024-129">The date the object was installed.</span></span> <span data-ttu-id="ef024-130">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ef024-130">A lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="ef024-131">**Name**</span><span class="sxs-lookup"><span data-stu-id="ef024-131">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef024-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef024-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef024-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef024-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef024-134">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ef024-134">The name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="ef024-135">**Status**</span><span class="sxs-lookup"><span data-stu-id="ef024-135">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef024-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef024-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef024-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef024-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef024-138">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="ef024-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="ef024-139">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ef024-139">Current status of the object.</span></span> <span data-ttu-id="ef024-140">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ef024-140">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ef024-141">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="ef024-141">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ef024-142">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="ef024-142">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ef024-143">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef024-143">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ef024-144">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="ef024-144">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<dt>



 <span data-ttu-id="ef024-145">("OK")</span><span class="sxs-lookup"><span data-stu-id="ef024-145">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ef024-146">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="ef024-146">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ef024-147">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="ef024-147">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ef024-148">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="ef024-148">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ef024-149">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ef024-149">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ef024-150">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="ef024-150">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ef024-151">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="ef024-151">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ef024-152">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="ef024-152">("Service")</span></span>


<span data-ttu-id="ef024-153"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ef024-153"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ef024-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef024-154">Requirements</span></span>



| <span data-ttu-id="ef024-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef024-155">Requirement</span></span> | <span data-ttu-id="ef024-156">Wert</span><span class="sxs-lookup"><span data-stu-id="ef024-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef024-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef024-157">Minimum supported client</span></span><br/> | <span data-ttu-id="ef024-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef024-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef024-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef024-159">Minimum supported server</span></span><br/> | <span data-ttu-id="ef024-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef024-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef024-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef024-161">Namespace</span></span><br/>                | <span data-ttu-id="ef024-162">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ef024-162">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ef024-163">MOF</span><span class="sxs-lookup"><span data-stu-id="ef024-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef024-164"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ef024-164"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef024-165">DLL</span><span class="sxs-lookup"><span data-stu-id="ef024-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef024-166"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef024-166"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 


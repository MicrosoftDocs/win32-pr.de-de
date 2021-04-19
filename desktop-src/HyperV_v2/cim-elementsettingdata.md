---
description: Stellt eine Zuordnung zwischen einem verwalteten Element und den zugehörigen Einstellungsdaten dar. Diese Zuordnung beschreibt auch, ob dies eine Standardeinstellung oder eine aktuelle Einstellung ist.
ms.assetid: 0df2b235-76d9-4899-938b-274ec5471324
title: CIM_ElementSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSettingData
- CIM_ElementSettingData.ManagedElement
- CIM_ElementSettingData.SettingData
- CIM_ElementSettingData.IsDefault
- CIM_ElementSettingData.IsCurrent
- CIM_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e22dbd221f2e83009e4268cc0de337374e04298a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373076"
---
# <a name="cim_elementsettingdata-class"></a><span data-ttu-id="dd692-104">CIM- \_ elementsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="dd692-104">CIM\_ElementSettingData class</span></span>

<span data-ttu-id="dd692-105">Stellt eine Zuordnung zwischen einem verwalteten Element und den zugehörigen Einstellungsdaten dar.</span><span class="sxs-lookup"><span data-stu-id="dd692-105">Represents an association between a managed element and its associated setting data.</span></span> <span data-ttu-id="dd692-106">Diese Zuordnung beschreibt auch, ob dies eine Standardeinstellung oder eine aktuelle Einstellung ist.</span><span class="sxs-lookup"><span data-stu-id="dd692-106">This association also describes whether this is a default or current setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd692-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd692-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.19.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault;
  uint16                 IsCurrent;
  uint16                 IsNext;
};
```

## <a name="members"></a><span data-ttu-id="dd692-108">Member</span><span class="sxs-lookup"><span data-stu-id="dd692-108">Members</span></span>

<span data-ttu-id="dd692-109">Die **CIM \_ elementsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dd692-109">The **CIM\_ElementSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="dd692-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd692-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd692-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd692-111">Properties</span></span>

<span data-ttu-id="dd692-112">Die **CIM \_ elementsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd692-112">The **CIM\_ElementSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd692-113">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="dd692-113">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd692-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd692-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd692-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd692-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd692-116">Gibt an, ob die Einstellung, auf die verwiesen wird, zurzeit vom Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd692-116">Indicates whether the referenced setting is currently being used by the element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd692-117">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dd692-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>

<span data-ttu-id="dd692-118">**Ist aktuell** (1)</span><span class="sxs-lookup"><span data-stu-id="dd692-118">**Is Current** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>

<span data-ttu-id="dd692-119">**Ist nicht aktuell** (2)</span><span class="sxs-lookup"><span data-stu-id="dd692-119">**Is Not Current** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd692-120">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="dd692-120">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd692-121">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd692-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd692-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd692-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd692-123">Der Wert, der angibt, ob die Einstellung eine Standardeinstellung für das Element ist.</span><span class="sxs-lookup"><span data-stu-id="dd692-123">Indicating whether the setting is a default setting for the element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd692-124">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dd692-124">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>

<span data-ttu-id="dd692-125">**Ist Standard** (1)</span><span class="sxs-lookup"><span data-stu-id="dd692-125">**Is Default** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>

<span data-ttu-id="dd692-126">**Ist nicht Standard** (2)</span><span class="sxs-lookup"><span data-stu-id="dd692-126">**Is Not Default** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd692-127">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="dd692-127">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd692-128">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd692-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd692-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd692-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd692-130">Ein Flag, das angibt, wann und wie oft die Einstellung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd692-130">A flag that indicates when and how often to apply the setting.</span></span>

<span data-ttu-id="dd692-131">Die Einstellung kann z. b. auf eine neuinitialisierungs-, Zurücksetzungs-und Neukonfigurations Anforderung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd692-131">For example, the setting could be applied on a re-initialization, reset, reconfiguration request.</span></span> <span data-ttu-id="dd692-132">Dies könnte eine permanente Einstellung oder eine Einstellung sein, die nur ein Mal verwendet wird, wie durch das-Flag angegeben.</span><span class="sxs-lookup"><span data-stu-id="dd692-132">This could be a permanent setting, or a setting used only one time, as indicated by the flag.</span></span> <span data-ttu-id="dd692-133">Wenn es sich um eine permanente Einstellung handelt, wird die Einstellung jedes Mal angewendet, wenn das verwaltete Element erneut initialisiert wird, bis dieses Flag manuell zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="dd692-133">If it is a permanent setting then the setting is applied every time the managed element reinitializes, until this flag is manually reset.</span></span> <span data-ttu-id="dd692-134">Wenn es sich jedoch um eine einzelne Verwendung handelt, wird das Flag nach dem Anwenden der Einstellungen automatisch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dd692-134">However, if it is single use, then the flag is automatically cleared after the settings are applied.</span></span> <span data-ttu-id="dd692-135">Wenn dieses Flag außerdem auf einen anderen Wert als 0 (unbekannt) festgelegt ist, hat dies Vorrang vor einer **SettingData** -Eigenschaft, die auf "Default" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dd692-135">In addition, if this flag is set to value other than 0 (Unknown), then this takes precedence over a **SettingData** property that is set to "Default".</span></span>

<span data-ttu-id="dd692-136">Wenn das verwaltete Element ein Computersystem ist und der Wert dieses Flags "is Next" lautet, wird die Einstellung beim nächsten Zurücksetzen des Systems wirksam.</span><span class="sxs-lookup"><span data-stu-id="dd692-136">If the managed element is a computer system, and the value of this flag is "Is Next", then the setting will be effective next time the system resets.</span></span> <span data-ttu-id="dd692-137">Und wenn dieses Flag nicht geändert wird, wird es für nachfolgende System zurück Stellungen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="dd692-137">And, unless this flag is changed, it will persist for subsequent system resets.</span></span> <span data-ttu-id="dd692-138">Wenn dieses Flag jedoch auf "Next for Single Use" festgelegt ist, wird diese Einstellung nur einmal verwendet, und das Flag würde danach auf 2 zurückgesetzt (nicht weiter).</span><span class="sxs-lookup"><span data-stu-id="dd692-138">However, if this flag is set to "Is Next For Single Use", then this setting will only be used once and the flag would be reset after that to 2 (Is Not Next).</span></span> <span data-ttu-id="dd692-139">Im obigen Beispiel wird die Einstellung beim zweiten Neustart nicht verwendet, wenn das System in einer schnell Folge neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="dd692-139">So, in the above example, if the system reboots in a quick succession, the setting will not be used at the second reboot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd692-140">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dd692-140">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>

<span data-ttu-id="dd692-141">**Ist Next** (1)</span><span class="sxs-lookup"><span data-stu-id="dd692-141">**Is Next** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>

<span data-ttu-id="dd692-142">**Nicht weiter** (2)</span><span class="sxs-lookup"><span data-stu-id="dd692-142">**Is Not Next** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>

<span data-ttu-id="dd692-143">**Nächste Verwendung** (3)</span><span class="sxs-lookup"><span data-stu-id="dd692-143">**Is Next For Single Use** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd692-144">**"Managedelement"**</span><span class="sxs-lookup"><span data-stu-id="dd692-144">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd692-145">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="dd692-145">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="dd692-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd692-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd692-147">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd692-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd692-148">Das verwaltete Element.</span><span class="sxs-lookup"><span data-stu-id="dd692-148">The managed element.</span></span>

</dd> <dt>

<span data-ttu-id="dd692-149">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="dd692-149">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd692-150">Datentyp: **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="dd692-150">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="dd692-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd692-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd692-152">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd692-152">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd692-153">Die Einstellungsdaten, die dem Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="dd692-153">The setting data associated with the element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd692-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd692-154">Requirements</span></span>



| <span data-ttu-id="dd692-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd692-155">Requirement</span></span> | <span data-ttu-id="dd692-156">Wert</span><span class="sxs-lookup"><span data-stu-id="dd692-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd692-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd692-157">Minimum supported client</span></span><br/> | <span data-ttu-id="dd692-158">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dd692-158">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="dd692-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd692-159">Minimum supported server</span></span><br/> | <span data-ttu-id="dd692-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dd692-160">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="dd692-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd692-161">Namespace</span></span><br/>                | <span data-ttu-id="dd692-162">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="dd692-162">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dd692-163">MOF</span><span class="sxs-lookup"><span data-stu-id="dd692-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd692-164"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dd692-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd692-165">DLL</span><span class="sxs-lookup"><span data-stu-id="dd692-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd692-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd692-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


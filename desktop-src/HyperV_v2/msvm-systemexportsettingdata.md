---
description: Ordnet einen virtuellen Computer und seine Export Einstellungsdaten zu.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Msvm_SystemExportSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemExportSettingData
- Msvm_SystemExportSettingData.ManagedElement
- Msvm_SystemExportSettingData.SettingData
- Msvm_SystemExportSettingData.IsDefault
- Msvm_SystemExportSettingData.IsCurrent
- Msvm_SystemExportSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8203a45bb911743bb064c1a686da0b3d8abe99bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346693"
---
# <a name="msvm_systemexportsettingdata-class"></a><span data-ttu-id="1dc4e-103">MSVM \_ systemexportsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="1dc4e-103">Msvm\_SystemExportSettingData class</span></span>

<span data-ttu-id="1dc4e-104">Ordnet einen virtuellen Computer und seine Export Einstellungsdaten zu.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-104">Associates a virtual machine and its export setting data.</span></span> <span data-ttu-id="1dc4e-105">Vor dem Aufrufen der [**exportsystemdefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse kann eine Instanz von [**MSVM \_ virtualsystemexportsettingdata**](msvm-virtualsystemexportsettingdata.md) mithilfe dieser Zuordnung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-105">Before calling the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class, an instance of [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) can be retrieved using this association.</span></span>

<span data-ttu-id="1dc4e-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc4e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dc4e-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemExportSettingData : CIM_ElementSettingData
{
  CIM_ComputerSystem                  REF ManagedElement;
  Msvm_VirtualSystemExportSettingData REF SettingData;
  uint16                                  IsDefault = 1;
  uint16                                  IsCurrent = 1;
  uint16                                  IsNext = 0;
};
```

## <a name="members"></a><span data-ttu-id="1dc4e-108">Member</span><span class="sxs-lookup"><span data-stu-id="1dc4e-108">Members</span></span>

<span data-ttu-id="1dc4e-109">Die **MSVM \_ systemexportsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1dc4e-109">The **Msvm\_SystemExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1dc4e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1dc4e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1dc4e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1dc4e-111">Properties</span></span>

<span data-ttu-id="1dc4e-112">Die **MSVM \_ systemexportsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-112">The **Msvm\_SystemExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1dc4e-113">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="1dc4e-113">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dc4e-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1dc4e-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dc4e-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1dc4e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dc4e-116">Gibt an, ob die Einstellung, auf die verwiesen wird, derzeit im Vorgang des-Elements verwendet wird, oder ob diese Informationen unbekannt sind.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-116">Indicates if the referenced setting is currently being used in the operation of the element, or that this information is unknown.</span></span> <span data-ttu-id="1dc4e-117">Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-117">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="1dc4e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1dc4e-118">Value</span></span>                                                                        | <span data-ttu-id="1dc4e-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1dc4e-119">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="1dc4e-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1dc4e-120"><dt>0</dt></span></span> </dl> | <span data-ttu-id="1dc4e-121">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="1dc4e-121">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="1dc4e-122"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1dc4e-122"><dt>1</dt></span></span> </dl> | <span data-ttu-id="1dc4e-123">Aktuell</span><span class="sxs-lookup"><span data-stu-id="1dc4e-123">Current</span></span><br/>     |
| <dl> <span data-ttu-id="1dc4e-124"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1dc4e-124"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1dc4e-125">Nicht aktuell</span><span class="sxs-lookup"><span data-stu-id="1dc4e-125">Not Current</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1dc4e-126">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="1dc4e-126">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dc4e-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1dc4e-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dc4e-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1dc4e-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dc4e-129">Gibt an, ob die referenzierte Einstellung eine Standardeinstellung für das Element ist, oder ob diese Informationen unbekannt sind.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-129">Indicates if the referenced setting is a default setting for the element, or that this information is unknown.</span></span> <span data-ttu-id="1dc4e-130">Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-130">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="1dc4e-131">Wert</span><span class="sxs-lookup"><span data-stu-id="1dc4e-131">Value</span></span>                                                                        | <span data-ttu-id="1dc4e-132">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1dc4e-132">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="1dc4e-133"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1dc4e-133"><dt>0</dt></span></span> </dl> | <span data-ttu-id="1dc4e-134">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="1dc4e-134">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="1dc4e-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1dc4e-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="1dc4e-136">Standard</span><span class="sxs-lookup"><span data-stu-id="1dc4e-136">Default</span></span><br/>     |
| <dl> <span data-ttu-id="1dc4e-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1dc4e-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1dc4e-138">Nicht Standard</span><span class="sxs-lookup"><span data-stu-id="1dc4e-138">Not Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1dc4e-139">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="1dc4e-139">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dc4e-140">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1dc4e-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dc4e-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1dc4e-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dc4e-142">Gibt an, ob die referenzierte Einstellung die nächste Einstellung ist, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-142">Indicates whether or not the referenced setting is the next setting to be applied.</span></span> <span data-ttu-id="1dc4e-143">Die Anwendung kann z. b. bei einer erneuten Initialisierung, zurück Setzung und Neukonfiguration der Anforderung stattfinden.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-143">For example, the application could take place on a re-initialization, reset, reconfiguration request.</span></span> <span data-ttu-id="1dc4e-144">Dies könnte eine permanente Einstellung oder eine Einstellung sein, die nur ein Mal verwendet wird, wie durch das-Flag angegeben.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-144">This could be a permanent setting, or a setting used only one time, as indicated by the flag.</span></span> <span data-ttu-id="1dc4e-145">Wenn es sich um eine permanente Einstellung handelt, wird die Einstellung jedes Mal angewendet, wenn das verwaltete Element erneut initialisiert wird, bis dieses Flag manuell zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-145">If it is a permanent setting then the setting is applied every time the managed element reinitializes, until this flag is manually reset.</span></span> <span data-ttu-id="1dc4e-146">Wenn es sich jedoch um eine einzelne Verwendung handelt, wird das Flag nach dem Anwenden der Einstellungen automatisch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-146">However, if it is single use, then the flag is automatically cleared after the settings are applied.</span></span> <span data-ttu-id="1dc4e-147">Wenn dieses Flag angegeben wird (d. h. auf einen anderen Wert als 0 (unbekannt) festgelegt ist), hat dies Vorrang vor den Einstellungsdaten, die möglicherweise als Standard angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-147">Also, if this flag is specified (i.e. set to value other than 0 (Unknown)), then this takes precedence over any setting data that may have been specified as default.</span></span> <span data-ttu-id="1dc4e-148">Beispiel: Wenn das verwaltete Element ein Computersystem ist und der Wert dieses Flags 1 ist (steht als nächstes), wird die Einstellung beim nächsten Zurücksetzen des Systems wirksam.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-148">For example: If the managed element is a computer system, and the value of this flag is 1 (Is Next), then the setting will be effective next time the system resets.</span></span> <span data-ttu-id="1dc4e-149">Und wenn dieses Flag nicht geändert wird, wird es für nachfolgende System zurück Stellungen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-149">And, unless this flag is changed, it will persist for subsequent system resets.</span></span> <span data-ttu-id="1dc4e-150">Wenn dieses Flag jedoch auf den Wert 3 festgelegt ist (steht für die einmalige Verwendung), wird diese Einstellung nur einmal verwendet, und das Flag würde danach auf 2 zurückgesetzt (nicht weiter).</span><span class="sxs-lookup"><span data-stu-id="1dc4e-150">However, if this flag is set to 3 (Is Next For Single Use), then this setting will only be used once and the flag would be reset after that to 2 (Is Not Next).</span></span> <span data-ttu-id="1dc4e-151">Im obigen Beispiel wird die Einstellung beim zweiten Neustart nicht verwendet, wenn das System in einer schnell Folge neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-151">So, in the above example, if the system reboots in a quick succession, the setting will not be used at the second reboot.</span></span>

<span data-ttu-id="1dc4e-152">Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-152">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="1dc4e-153">Wert</span><span class="sxs-lookup"><span data-stu-id="1dc4e-153">Value</span></span>                                                                        | <span data-ttu-id="1dc4e-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1dc4e-154">Meaning</span></span>                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="1dc4e-155"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1dc4e-155"><dt>0</dt></span></span> </dl> | <span data-ttu-id="1dc4e-156">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="1dc4e-156">Unknown</span></span><br/>                |
| <dl> <span data-ttu-id="1dc4e-157"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1dc4e-157"><dt>1</dt></span></span> </dl> | <span data-ttu-id="1dc4e-158">Nächste</span><span class="sxs-lookup"><span data-stu-id="1dc4e-158">Is Next</span></span><br/>                |
| <dl> <span data-ttu-id="1dc4e-159"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1dc4e-159"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1dc4e-160">Nicht weiter</span><span class="sxs-lookup"><span data-stu-id="1dc4e-160">Is Not Next</span></span><br/>            |
| <dl> <span data-ttu-id="1dc4e-161"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1dc4e-161"><dt>3</dt></span></span> </dl> | <span data-ttu-id="1dc4e-162">Nächste Verwendung</span><span class="sxs-lookup"><span data-stu-id="1dc4e-162">Is Next For Single Use</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1dc4e-163">**"Managedelement"**</span><span class="sxs-lookup"><span data-stu-id="1dc4e-163">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dc4e-164">Datentyp: **[ **CIM \_ Computersystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="1dc4e-164">Data type: **[**CIM\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1dc4e-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1dc4e-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dc4e-166">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ elementsettingdata. managedelta")</span><span class="sxs-lookup"><span data-stu-id="1dc4e-166">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ElementSettingData.ManagedElement")</span></span>
</dt> </dl>

<span data-ttu-id="1dc4e-167">Verweis auf den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-167">Reference to the virtual machine.</span></span> <span data-ttu-id="1dc4e-168">Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-168">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1dc4e-169">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="1dc4e-169">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dc4e-170">Datentyp: **[ **MSVM \_ virtualsystemexportsettingdata**](msvm-virtualsystemexportsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="1dc4e-170">Data type: **[**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1dc4e-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1dc4e-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dc4e-172">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ elementsettingdata. SettingData")</span><span class="sxs-lookup"><span data-stu-id="1dc4e-172">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ElementSettingData.SettingData")</span></span>
</dt> </dl>

<span data-ttu-id="1dc4e-173">Verweis auf die Export Einstellungsdaten für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-173">Reference to the export setting data for the virtual machine.</span></span> <span data-ttu-id="1dc4e-174">Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-174">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1dc4e-175">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1dc4e-175">Remarks</span></span>

<span data-ttu-id="1dc4e-176">Der Zugriff auf die **MSVM \_ systemexportsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="1dc4e-176">Access to the **Msvm\_SystemExportSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1dc4e-177">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1dc4e-177">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1dc4e-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1dc4e-178">Requirements</span></span>



| <span data-ttu-id="1dc4e-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1dc4e-179">Requirement</span></span> | <span data-ttu-id="1dc4e-180">Wert</span><span class="sxs-lookup"><span data-stu-id="1dc4e-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc4e-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1dc4e-181">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc4e-182">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1dc4e-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1dc4e-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1dc4e-183">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc4e-184">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1dc4e-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1dc4e-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="1dc4e-185">Namespace</span></span><br/>                | <span data-ttu-id="1dc4e-186">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1dc4e-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1dc4e-187">MOF</span><span class="sxs-lookup"><span data-stu-id="1dc4e-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1dc4e-188"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1dc4e-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1dc4e-189">DLL</span><span class="sxs-lookup"><span data-stu-id="1dc4e-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dc4e-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1dc4e-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


---
description: Ordnet einen verwalteten-Element seinen Konfigurationsdaten zu.
ms.assetid: 4DB78E43-E387-478E-999C-770B35925721
title: Msvm_ElementSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementSettingData
- Msvm_ElementSettingData.ManagedElement
- Msvm_ElementSettingData.SettingData
- Msvm_ElementSettingData.IsDefault
- Msvm_ElementSettingData.IsCurrent
- Msvm_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f4d2af614e3b161f49a0d37d1e4d1ee48ce0aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349036"
---
# <a name="msvm_elementsettingdata-class"></a><span data-ttu-id="34c96-103">MSVM \_ elementsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="34c96-103">Msvm\_ElementSettingData class</span></span>

<span data-ttu-id="34c96-104">Ordnet einen verwalteten-Element seinen Konfigurationsdaten zu.</span><span class="sxs-lookup"><span data-stu-id="34c96-104">Associates a managed element with its configuration data.</span></span> <span data-ttu-id="34c96-105">Einige der wichtigeren Anwendungen dieser Zuordnung sind die Verwendung beim Verknüpfen einer virtuellen Maschine und der logischen Geräte, die diesem System mit ihren Informationen zur Momentaufnahme Konfiguration zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="34c96-105">Some of the more notable applications of this association are its use in linking a virtual machine and the logical devices that have been assigned to that system with their snapshot configuration information.</span></span> <span data-ttu-id="34c96-106">Die aktuellen Konfigurationsinformationen werden dem virtuellen Computer und seinen Geräten über die [**MSVM \_ settingsdefinestate**](msvm-settingsdefinestate.md) -Zuordnung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="34c96-106">Current configuration information is associated with the virtual machine and its devices through the [**Msvm\_SettingsDefineState**](msvm-settingsdefinestate.md) association.</span></span>

<span data-ttu-id="34c96-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="34c96-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="34c96-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="34c96-108">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementSettingData : CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault = 0;
  uint16                 IsCurrent = 0;
  uint16                 IsNext = 0;
};
```

## <a name="members"></a><span data-ttu-id="34c96-109">Member</span><span class="sxs-lookup"><span data-stu-id="34c96-109">Members</span></span>

<span data-ttu-id="34c96-110">Die **MSVM \_ elementsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="34c96-110">The **Msvm\_ElementSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="34c96-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34c96-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="34c96-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34c96-112">Properties</span></span>

<span data-ttu-id="34c96-113">Die **MSVM \_ elementsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="34c96-113">The **Msvm\_ElementSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34c96-114">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="34c96-114">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34c96-115">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34c96-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34c96-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34c96-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34c96-117">Gibt an, dass die Einstellung, auf die verwiesen wird, derzeit im Vorgang des-Elements verwendet wird, oder dass diese Informationen unbekannt sind.</span><span class="sxs-lookup"><span data-stu-id="34c96-117">Indicates that the referenced setting is currently being used in the operation of the element or that this information is unknown.</span></span> <span data-ttu-id="34c96-118">Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34c96-118">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="34c96-119">Der Standardwert ist 0 (unbekannt).</span><span class="sxs-lookup"><span data-stu-id="34c96-119">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="34c96-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="34c96-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34c96-121"><span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Ist aktuell** (1)</span><span class="sxs-lookup"><span data-stu-id="34c96-121"><span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Is Current** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34c96-122"><span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**Ist nicht aktuell** (2)</span><span class="sxs-lookup"><span data-stu-id="34c96-122"><span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**Is Not Current** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34c96-123">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="34c96-123">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34c96-124">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34c96-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34c96-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34c96-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34c96-126">Gibt an, dass die referenzierte Einstellung eine Standardeinstellung für das-Element ist oder dass diese Informationen unbekannt sind.</span><span class="sxs-lookup"><span data-stu-id="34c96-126">Indicates that the referenced setting is a default setting for the element or that this information is unknown.</span></span> <span data-ttu-id="34c96-127">Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34c96-127">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="34c96-128">Der Standardwert ist 0 (unbekannt).</span><span class="sxs-lookup"><span data-stu-id="34c96-128">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="34c96-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="34c96-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34c96-130"><span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**Ist Standard** (1)</span><span class="sxs-lookup"><span data-stu-id="34c96-130"><span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**Is Default** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34c96-131"><span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**Ist nicht Standard** (2)</span><span class="sxs-lookup"><span data-stu-id="34c96-131"><span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**Is Not Default** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34c96-132">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="34c96-132">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34c96-133">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34c96-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34c96-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34c96-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34c96-135">Gibt an, ob die referenzierte Einstellung die nächste Einstellung ist, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="34c96-135">Indicates whether the referenced setting is the next setting to be applied.</span></span> <span data-ttu-id="34c96-136">Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34c96-136">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="34c96-137">Der Standardwert ist 0 (unbekannt).</span><span class="sxs-lookup"><span data-stu-id="34c96-137">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="34c96-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="34c96-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34c96-139"><span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Ist Next** (1)</span><span class="sxs-lookup"><span data-stu-id="34c96-139"><span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Is Next** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34c96-140"><span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**Nicht weiter** (2)</span><span class="sxs-lookup"><span data-stu-id="34c96-140"><span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**Is Not Next** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34c96-141"><span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**Nächste Verwendung** (3)</span><span class="sxs-lookup"><span data-stu-id="34c96-141"><span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**Is Next For Single Use** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34c96-142">**"Managedelement"**</span><span class="sxs-lookup"><span data-stu-id="34c96-142">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34c96-143">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="34c96-143">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="34c96-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34c96-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34c96-145">Verweis auf den virtuellen Computer oder das virtuelle Gerät.</span><span class="sxs-lookup"><span data-stu-id="34c96-145">Reference to the virtual machine or virtual device.</span></span> <span data-ttu-id="34c96-146">Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34c96-146">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="34c96-147">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="34c96-147">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34c96-148">Datentyp: **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="34c96-148">Data type: **[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="34c96-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34c96-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34c96-150">Verweis auf die snapshoeteinstellungen für die virtuelle Maschine oder das virtuelle Gerät.</span><span class="sxs-lookup"><span data-stu-id="34c96-150">Reference to the snapshotted settings for the virtual machine or virtual device.</span></span> <span data-ttu-id="34c96-151">Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34c96-151">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34c96-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34c96-152">Remarks</span></span>

<span data-ttu-id="34c96-153">Der Zugriff auf die **MSVM- \_ elementsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="34c96-153">Access to the **Msvm\_ElementSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="34c96-154">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="34c96-154">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="34c96-155">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34c96-155">Examples</span></span>

<span data-ttu-id="34c96-156">Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="34c96-156">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="34c96-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34c96-157">Requirements</span></span>



| <span data-ttu-id="34c96-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34c96-158">Requirement</span></span> | <span data-ttu-id="34c96-159">Wert</span><span class="sxs-lookup"><span data-stu-id="34c96-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34c96-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34c96-160">Minimum supported client</span></span><br/> | <span data-ttu-id="34c96-161">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34c96-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="34c96-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34c96-162">Minimum supported server</span></span><br/> | <span data-ttu-id="34c96-163">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34c96-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="34c96-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="34c96-164">Namespace</span></span><br/>                | <span data-ttu-id="34c96-165">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="34c96-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="34c96-166">MOF</span><span class="sxs-lookup"><span data-stu-id="34c96-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34c96-167"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="34c96-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="34c96-168">DLL</span><span class="sxs-lookup"><span data-stu-id="34c96-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34c96-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="34c96-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="34c96-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34c96-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34c96-171">**CIM- \_ elementsettingdata**</span><span class="sxs-lookup"><span data-stu-id="34c96-171">**CIM\_ElementSettingData**</span></span>](cim-elementsettingdata.md)
</dt> <dt>

[<span data-ttu-id="34c96-172">**CIM- \_ elementsettingdata**</span><span class="sxs-lookup"><span data-stu-id="34c96-172">**CIM\_ElementSettingData**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)
</dt> <dt>

[<span data-ttu-id="34c96-173">Verwaltungs Klassen für virtuelle Systeme</span><span class="sxs-lookup"><span data-stu-id="34c96-173">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 


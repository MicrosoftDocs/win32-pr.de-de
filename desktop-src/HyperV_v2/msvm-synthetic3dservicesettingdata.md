---
description: Stellt die Einstellungen für den synthetischen 3D-Dienst dar, der auf einem einzelnen Host System vorhanden ist.
ms.assetid: ed5d9bba-faad-40a6-8f08-258a94272a11
title: Msvm_Synthetic3DServiceSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DServiceSettingData
- Msvm_Synthetic3DServiceSettingData.InstanceID
- Msvm_Synthetic3DServiceSettingData.Caption
- Msvm_Synthetic3DServiceSettingData.Description
- Msvm_Synthetic3DServiceSettingData.ElementName
- Msvm_Synthetic3DServiceSettingData.GPUOvercommitEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b625064f90ef4c0241dfa48bea9900110f37a4d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131073"
---
# <a name="msvm_synthetic3dservicesettingdata-class"></a><span data-ttu-id="b91cc-103">MSVM \_ Synthetic3DServiceSettingData-Klasse</span><span class="sxs-lookup"><span data-stu-id="b91cc-103">Msvm\_Synthetic3DServiceSettingData class</span></span>

<span data-ttu-id="b91cc-104">Stellt die Einstellungen für den synthetischen 3D-Dienst dar, der auf einem einzelnen Host System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b91cc-104">Represents the settings for the synthetic 3-D service present on a single host system.</span></span> <span data-ttu-id="b91cc-105">Die Eigenschaften für diese Klasse können nicht direkt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b91cc-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="b91cc-106">Der Client muss die [**MSVM \_ Synthetic3DService. modifyservicesettings**](modifyservicesettings-msvm-synthetic3dservice.md) -Methode abrufen, um diese Eigenschaften zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b91cc-106">The client must call the [**Msvm\_Synthetic3DService.ModifyServiceSettings**](modifyservicesettings-msvm-synthetic3dservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="b91cc-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b91cc-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b91cc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b91cc-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Synthetic3D Service Settings";
  string  Description = "Configuration Settings for Synthetic3D Service.";
  string  ElementName = "Synthetic3D Service Settings";
  boolean GPUOvercommitEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="b91cc-109">Member</span><span class="sxs-lookup"><span data-stu-id="b91cc-109">Members</span></span>

<span data-ttu-id="b91cc-110">Die **MSVM \_ Synthetic3DServiceSettingData** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b91cc-110">The **Msvm\_Synthetic3DServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b91cc-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b91cc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b91cc-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b91cc-112">Properties</span></span>

<span data-ttu-id="b91cc-113">Die **MSVM- \_ Synthetic3DServiceSettingData** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b91cc-113">The **Msvm\_Synthetic3DServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b91cc-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b91cc-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b91cc-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b91cc-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b91cc-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b91cc-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b91cc-117">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b91cc-117">A short description of the object.</span></span> <span data-ttu-id="b91cc-118">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b91cc-118">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b91cc-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b91cc-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b91cc-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b91cc-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b91cc-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b91cc-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b91cc-122">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b91cc-122">A description of the object.</span></span> <span data-ttu-id="b91cc-123">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b91cc-123">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b91cc-124">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b91cc-124">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b91cc-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b91cc-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b91cc-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b91cc-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b91cc-127">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b91cc-127">A display name for the object.</span></span> <span data-ttu-id="b91cc-128">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b91cc-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b91cc-129">**Gpuovercommitenabled**</span><span class="sxs-lookup"><span data-stu-id="b91cc-129">**GPUOvercommitEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b91cc-130">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b91cc-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b91cc-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b91cc-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b91cc-132">Steuert, ob bei der Zuweisung von virtuellen Maschinen GPU-Speicherbeschränkungen berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="b91cc-132">Controls whether virtual machine assignment takes GPU memory limitations into account.</span></span>

</dd> <dt>

<span data-ttu-id="b91cc-133">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b91cc-133">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b91cc-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b91cc-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b91cc-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b91cc-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b91cc-136">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="b91cc-136">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b91cc-137">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b91cc-137">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b91cc-138">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b91cc-138">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b91cc-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b91cc-139">Requirements</span></span>



| <span data-ttu-id="b91cc-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b91cc-140">Requirement</span></span> | <span data-ttu-id="b91cc-141">Wert</span><span class="sxs-lookup"><span data-stu-id="b91cc-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b91cc-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b91cc-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b91cc-143">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b91cc-143">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b91cc-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b91cc-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b91cc-145">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b91cc-145">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b91cc-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="b91cc-146">Namespace</span></span><br/>                | <span data-ttu-id="b91cc-147">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b91cc-147">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b91cc-148">MOF</span><span class="sxs-lookup"><span data-stu-id="b91cc-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b91cc-149"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b91cc-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b91cc-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b91cc-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b91cc-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b91cc-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


---
description: Stellt die Einstellungen für den metrikdienst dar. Die Eigenschaften für diese Klasse können nicht direkt geändert werden. Der Client muss die modifyservicesettings-Methode zum Ändern dieser Eigenschaften aufruft.
ms.assetid: 578ddda7-4c8e-498e-8612-29c392390b73
title: Msvm_MetricServiceSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceSettingData
- Msvm_MetricServiceSettingData.InstanceID
- Msvm_MetricServiceSettingData.Caption
- Msvm_MetricServiceSettingData.Description
- Msvm_MetricServiceSettingData.ElementName
- Msvm_MetricServiceSettingData.MetricsFlushInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a1211b19692761dd8b92de69cf42e4ad55246f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347078"
---
# <a name="msvm_metricservicesettingdata-class"></a><span data-ttu-id="a1a35-105">MSVM \_ metricservicesettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="a1a35-105">Msvm\_MetricServiceSettingData class</span></span>

<span data-ttu-id="a1a35-106">Stellt die Einstellungen für den metrikdienst dar.</span><span class="sxs-lookup"><span data-stu-id="a1a35-106">Represents the settings for the metric service.</span></span> <span data-ttu-id="a1a35-107">Die Eigenschaften für diese Klasse können nicht direkt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a1a35-107">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="a1a35-108">Der Client muss die [**modifyservicesettings**](modifyservicesettings-msvm-metricservice.md) -Methode zum Ändern dieser Eigenschaften aufruft.</span><span class="sxs-lookup"><span data-stu-id="a1a35-108">The client must call the [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="a1a35-109">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1a35-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1a35-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1a35-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service Settings";
  string   Description = "Defines Hyper-V Metric Service Settings";
  string   ElementName = "Hyper-V Metric Service Settings";
  datetime MetricsFlushInterval;
};
```

## <a name="members"></a><span data-ttu-id="a1a35-111">Member</span><span class="sxs-lookup"><span data-stu-id="a1a35-111">Members</span></span>

<span data-ttu-id="a1a35-112">Die **MSVM \_ metricservicesettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a1a35-112">The **Msvm\_MetricServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a1a35-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1a35-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1a35-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1a35-114">Properties</span></span>

<span data-ttu-id="a1a35-115">Die **MSVM \_ metricservicesettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1a35-115">The **Msvm\_MetricServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1a35-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a1a35-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1a35-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1a35-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1a35-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1a35-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1a35-119">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1a35-119">A short description of the object.</span></span> <span data-ttu-id="a1a35-120">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Einstellungen für Hyper-V-metrikdienste" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a1a35-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="a1a35-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1a35-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1a35-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1a35-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1a35-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1a35-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1a35-124">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1a35-124">A description of the object.</span></span> <span data-ttu-id="a1a35-125">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "definiert Hyper-V Metric Service Settings" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a1a35-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="a1a35-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a1a35-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1a35-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1a35-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1a35-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1a35-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1a35-129">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a1a35-129">A display name for the object.</span></span> <span data-ttu-id="a1a35-130">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Einstellungen für Hyper-V-metrikdienste" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a1a35-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="a1a35-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a1a35-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1a35-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1a35-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1a35-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1a35-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1a35-134">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="a1a35-134">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a1a35-135">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="a1a35-135">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a1a35-136">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1a35-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a1a35-137">**Metricsflushinterval**</span><span class="sxs-lookup"><span data-stu-id="a1a35-137">**MetricsFlushInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1a35-138">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a1a35-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a1a35-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1a35-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1a35-140">Definiert das Intervall, in dem Metriken auf den Datenträger geleert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a1a35-140">Defines the interval at which metrics should be flushed to disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1a35-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1a35-141">Requirements</span></span>



| <span data-ttu-id="a1a35-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1a35-142">Requirement</span></span> | <span data-ttu-id="a1a35-143">Wert</span><span class="sxs-lookup"><span data-stu-id="a1a35-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1a35-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1a35-144">Minimum supported client</span></span><br/> | <span data-ttu-id="a1a35-145">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1a35-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a1a35-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1a35-146">Minimum supported server</span></span><br/> | <span data-ttu-id="a1a35-147">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1a35-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a1a35-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="a1a35-148">Namespace</span></span><br/>                | <span data-ttu-id="a1a35-149">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a1a35-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a1a35-150">MOF</span><span class="sxs-lookup"><span data-stu-id="a1a35-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1a35-151"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a1a35-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1a35-152">DLL</span><span class="sxs-lookup"><span data-stu-id="a1a35-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1a35-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a1a35-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a1a35-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1a35-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1a35-155">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="a1a35-155">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="a1a35-156">**Modifyservicesettings**</span><span class="sxs-lookup"><span data-stu-id="a1a35-156">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-metricservice.md)
</dt> </dl>

 


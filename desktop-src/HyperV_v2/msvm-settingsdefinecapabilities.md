---
description: Stellt eine Verknüpfung zwischen der Funktionen-Instanz und den minimalen, maximalen, inkrementellen und Standardeinstellungen für eine Ressource bereit.
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Msvm_SettingsDefineCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineCapabilities
- Msvm_SettingsDefineCapabilities.SupportStatement
- Msvm_SettingsDefineCapabilities.GroupComponent
- Msvm_SettingsDefineCapabilities.PartComponent
- Msvm_SettingsDefineCapabilities.PropertyPolicy
- Msvm_SettingsDefineCapabilities.ValueRole
- Msvm_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7a312d3453b783c3d72f909ec6cb0b37d83feb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349049"
---
# <a name="msvm_settingsdefinecapabilities-class"></a><span data-ttu-id="b5215-103">MSVM \_ settingsdefinecapabili-Klasse</span><span class="sxs-lookup"><span data-stu-id="b5215-103">Msvm\_SettingsDefineCapabilities class</span></span>

<span data-ttu-id="b5215-104">Stellt eine Verknüpfung zwischen der Funktionen-Instanz und den minimalen, maximalen, inkrementellen und Standardeinstellungen für eine Ressource bereit.</span><span class="sxs-lookup"><span data-stu-id="b5215-104">Provides a link between the capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span>

<span data-ttu-id="b5215-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b5215-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5215-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5215-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  uint16               SupportStatement;
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a><span data-ttu-id="b5215-107">Member</span><span class="sxs-lookup"><span data-stu-id="b5215-107">Members</span></span>

<span data-ttu-id="b5215-108">Die **MSVM \_ settingsdefinecapabili-** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b5215-108">The **Msvm\_SettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="b5215-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b5215-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5215-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b5215-110">Properties</span></span>

<span data-ttu-id="b5215-111">Die **MSVM \_ settingsdefinecapabili-** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b5215-111">The **Msvm\_SettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5215-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b5215-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5215-113">Datentyp: **[ **CIM- \_ Funktionen**](/previous-versions//cc136806(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="b5215-113">Data type: **[**CIM\_Capabilities**](/previous-versions//cc136806(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="b5215-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5215-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5215-115">Die Instanz der Funktionen.</span><span class="sxs-lookup"><span data-stu-id="b5215-115">The capabilities instance.</span></span> <span data-ttu-id="b5215-116">Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5215-116">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b5215-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b5215-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5215-118">Datentyp: **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="b5215-118">Data type: **[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="b5215-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5215-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5215-120">Eine Einstellung, die zum Definieren der zugeordneten Funktionen Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5215-120">A setting used to define the associated capabilities instance.</span></span> <span data-ttu-id="b5215-121">Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5215-121">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b5215-122">**Propertypolicy**</span><span class="sxs-lookup"><span data-stu-id="b5215-122">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5215-123">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5215-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5215-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5215-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5215-125">Gibt an, ob nicht-NULL-Eigenschaften, die keine Schlüsseleigenschaften der zugeordneten Einstellungsdaten Instanz sind, unabhängig voneinander behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="b5215-125">Indicates whether the non-null, non-key properties of the associated setting data instance are treated independently or as a correlated set.</span></span> <span data-ttu-id="b5215-126">Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)) und immer auf 0 (unabhängig) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b5215-126">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) and it is always set to 0 (Independent).</span></span>

</dd> <dt>

<span data-ttu-id="b5215-127">**Supportstatement**</span><span class="sxs-lookup"><span data-stu-id="b5215-127">**SupportStatement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5215-128">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5215-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5215-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5215-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5215-130">Bezeichnet die Unterstützungs Anweisung.</span><span class="sxs-lookup"><span data-stu-id="b5215-130">Identifies the support statement.</span></span>

> [!Note]  
> <span data-ttu-id="b5215-131">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b5215-131">This property was added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span data-ttu-id="b5215-132"><span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Produktion** (0)</span><span class="sxs-lookup"><span data-stu-id="b5215-132"><span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Production** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span data-ttu-id="b5215-133"><span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Vorab** Version (1)</span><span class="sxs-lookup"><span data-stu-id="b5215-133"><span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Prerelease** (1)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b5215-134">War **nicht** für die Produktion in Windows 10, Version 1703.</span><span class="sxs-lookup"><span data-stu-id="b5215-134">Was **NonProduction** in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="b5215-135"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="b5215-135"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b5215-136">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="b5215-136">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5215-137">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5215-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5215-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5215-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5215-139">Jede weitere Semantik für die Interpretation aller nicht Schlüsseleigenschaften der Einstellungsdaten, die nicht NULL sind.</span><span class="sxs-lookup"><span data-stu-id="b5215-139">Any further semantics on the interpretation of all non-null, non-key properties of the setting data.</span></span> <span data-ttu-id="b5215-140">Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5215-140">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b5215-141">**Valuerole**</span><span class="sxs-lookup"><span data-stu-id="b5215-141">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5215-142">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5215-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5215-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5215-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5215-144">Jede weitere Semantik für die Interpretation der nicht--Schlüsseleigenschaften der Einstellungsdaten, die nicht NULL sind.</span><span class="sxs-lookup"><span data-stu-id="b5215-144">Any further semantics on the interpretation of the non-null, non-key properties of the setting data.</span></span> <span data-ttu-id="b5215-145">Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5215-145">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5215-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5215-146">Remarks</span></span>

<span data-ttu-id="b5215-147">Die Werte für die **valuerole** -und **ValueRange** -Eigenschaften werden in den folgenden Paaren verwendet:</span><span class="sxs-lookup"><span data-stu-id="b5215-147">The values for the **ValueRole** and **ValueRange** properties are used in the following pairs:</span></span>

-   <span data-ttu-id="b5215-148">Point/default (0/0)</span><span class="sxs-lookup"><span data-stu-id="b5215-148">Point/Default (0/0)</span></span>
-   <span data-ttu-id="b5215-149">Minimums/unterstützt (1/3)</span><span class="sxs-lookup"><span data-stu-id="b5215-149">Minimums/Supported (1/3)</span></span>
-   <span data-ttu-id="b5215-150">Maximums/unterstützt (2/3)</span><span class="sxs-lookup"><span data-stu-id="b5215-150">Maximums/Supported (2/3)</span></span>
-   <span data-ttu-id="b5215-151">Inkremente/unterstützt (3/3).</span><span class="sxs-lookup"><span data-stu-id="b5215-151">Increments/Supported (3/3).</span></span>

<span data-ttu-id="b5215-152">"Point" bedeutet, dass alle Eigenschaften des Objekts " **PartComponent** " den Standard der Plattform darstellen.</span><span class="sxs-lookup"><span data-stu-id="b5215-152">"Point" means that each of the properties on the **PartComponent** object represents the platform default.</span></span>

<span data-ttu-id="b5215-153">"Minimums" und "Maximums" bedeuten, dass alle Eigenschaften des Objekts " **PartComponent** " die kleinsten und größten möglichen Werte für diese Eigenschaften darstellen, die von der Plattform basierend auf der aktuellen Computerkonfiguration unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b5215-153">"Minimums" and "Maximums" mean that each of the properties on the **PartComponent** object represent the smallest and largest possible values for these properties that are supported by the platform based on your current machine configuration.</span></span>

<span data-ttu-id="b5215-154">"Inkremente" gibt die Granularität an, mit der Sie die Einstellungen vergrößern oder verkleinern können.</span><span class="sxs-lookup"><span data-stu-id="b5215-154">"Increments" indicates the granularity at which you can increase or decrease the settings.</span></span>

<span data-ttu-id="b5215-155">Der Zugriff auf die **MSVM \_ settingsdefinecapabili-** Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="b5215-155">Access to the **Msvm\_SettingsDefineCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b5215-156">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b5215-156">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5215-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5215-157">Requirements</span></span>



| <span data-ttu-id="b5215-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5215-158">Requirement</span></span> | <span data-ttu-id="b5215-159">Wert</span><span class="sxs-lookup"><span data-stu-id="b5215-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5215-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5215-160">Minimum supported client</span></span><br/> | <span data-ttu-id="b5215-161">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5215-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b5215-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5215-162">Minimum supported server</span></span><br/> | <span data-ttu-id="b5215-163">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5215-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5215-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5215-164">Namespace</span></span><br/>                | <span data-ttu-id="b5215-165">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b5215-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b5215-166">MOF</span><span class="sxs-lookup"><span data-stu-id="b5215-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5215-167"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b5215-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5215-168">DLL</span><span class="sxs-lookup"><span data-stu-id="b5215-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5215-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5215-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b5215-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5215-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5215-171">**CIM \_ settingsdefinecapabilitäten**</span><span class="sxs-lookup"><span data-stu-id="b5215-171">**CIM\_SettingsDefineCapabilities**</span></span>](cim-settingsdefinecapabilities.md)
</dt> <dt>

<span data-ttu-id="b5215-172">[**CIM \_ settingsdefinecapabilitäten**](/previous-versions//cc136913(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b5215-172">[**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b5215-173">**MSVM \_ settingsdefinecapabili(v1)**</span><span class="sxs-lookup"><span data-stu-id="b5215-173">**Msvm\_SettingsDefineCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[<span data-ttu-id="b5215-174">Ressourcen Verwaltungs Klassen</span><span class="sxs-lookup"><span data-stu-id="b5215-174">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 


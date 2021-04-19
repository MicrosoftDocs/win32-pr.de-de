---
description: Stellt eine Zuordnung zwischen den Eigenschaften einer CIM \_ -SettingData-Instanz und einer CIM-Funktions \_ Instanz dar.
ms.assetid: f3364779-baeb-4b84-a0e6-b2a60d1661bd
title: CIM_SettingsDefineCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineCapabilities
- CIM_SettingsDefineCapabilities.GroupComponent
- CIM_SettingsDefineCapabilities.PartComponent
- CIM_SettingsDefineCapabilities.PropertyPolicy
- CIM_SettingsDefineCapabilities.ValueRole
- CIM_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3c36e7c24702578704e849820abf2b1769c91c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360675"
---
# <a name="cim_settingsdefinecapabilities-class"></a><span data-ttu-id="10ea8-103">CIM \_ settingsdefinecapabili-Klasse</span><span class="sxs-lookup"><span data-stu-id="10ea8-103">CIM\_SettingsDefineCapabilities class</span></span>

<span data-ttu-id="10ea8-104">Stellt eine Zuordnung zwischen den Eigenschaften einer [**CIM- \_ SettingData**](cim-settingdata.md) -Instanz und einer CIM-Funktions Instanz dar. [**\_**](cim-capabilities.md)</span><span class="sxs-lookup"><span data-stu-id="10ea8-104">Represents an association between properties of a [**CIM\_SettingData**](cim-settingdata.md) instance and a [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="10ea8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="10ea8-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.22.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingsDefineCapabilities : CIM_Component
{
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a><span data-ttu-id="10ea8-106">Member</span><span class="sxs-lookup"><span data-stu-id="10ea8-106">Members</span></span>

<span data-ttu-id="10ea8-107">Die **CIM \_ settingsdefinecapabili-** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="10ea8-107">The **CIM\_SettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="10ea8-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10ea8-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10ea8-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10ea8-109">Properties</span></span>

<span data-ttu-id="10ea8-110">Die **CIM \_ settingsdefinecapabili-** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="10ea8-110">The **CIM\_SettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10ea8-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="10ea8-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ea8-112">Datentyp: **CIM- \_ Funktionen**</span><span class="sxs-lookup"><span data-stu-id="10ea8-112">Data type: **CIM\_Capabilities**</span></span>
</dt> <dt>

<span data-ttu-id="10ea8-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10ea8-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ea8-114">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="10ea8-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="10ea8-115">Ein Verweis auf die [**CIM- \_ Funktionen**](cim-capabilities.md) -Instanz.</span><span class="sxs-lookup"><span data-stu-id="10ea8-115">A reference to the [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="10ea8-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="10ea8-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ea8-117">Datentyp: **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="10ea8-117">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="10ea8-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10ea8-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ea8-119">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="10ea8-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="10ea8-120">Ein Verweis auf die [**CIM \_ SettingData**](cim-settingdata.md) -Instanz, die verwendet wird, um die CIM-Funktions Instanz zu definieren. [**\_**](cim-capabilities.md)</span><span class="sxs-lookup"><span data-stu-id="10ea8-120">A reference to the [**CIM\_SettingData**](cim-settingdata.md) instance used to define the [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="10ea8-121">**Propertypolicy**</span><span class="sxs-lookup"><span data-stu-id="10ea8-121">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ea8-122">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10ea8-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10ea8-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10ea8-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ea8-124">Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ settingsdefinecapabili.\*\*\*\*Valuerole**","**CIM \_ settingsdefinecapabili.\*\*\*\*ValueRange**")</span><span class="sxs-lookup"><span data-stu-id="10ea8-124">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**ValueRole**", "**CIM\_SettingsDefineCapabilities**.**ValueRange**")</span></span>
</dt> </dl>

<span data-ttu-id="10ea8-125">Gibt an, ob nicht-NULL nicht-Schlüsseleigenschaften der zugeordneten [**CIM \_ SettingData**](cim-settingdata.md) -Instanz unabhängig voneinander behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="10ea8-125">Indicates whether the non-null, non-key properties of the associated [**CIM\_SettingData**](cim-settingdata.md) instance are treated independently or as a correlated set.</span></span> <span data-ttu-id="10ea8-126">Beispielsweise kann ein unabhängiger Satz von maximalen Eigenschaften definiert werden, wenn keine Beziehung zwischen den einzelnen Eigenschaften besteht.</span><span class="sxs-lookup"><span data-stu-id="10ea8-126">For instance, an independent set of maximum properties might be defined when there is no relationship between each property.</span></span> <span data-ttu-id="10ea8-127">Im Gegensatz dazu müssen möglicherweise mehrere korrelierte Sätze von maximalen Eigenschaften definiert werden, wenn die maximalen Werte der einzelnen von einigen der anderen abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="10ea8-127">In contrast, several correlated sets of maximum properties might need to be defined when the maximum values of each are dependent on some of the others.</span></span>

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

<span data-ttu-id="10ea8-128">**Unabhängig** (0)</span><span class="sxs-lookup"><span data-stu-id="10ea8-128">**Independent** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

<span data-ttu-id="10ea8-129">**Korreliert** (1)</span><span class="sxs-lookup"><span data-stu-id="10ea8-129">**Correlated** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="10ea8-130">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="10ea8-130">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10ea8-131">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="10ea8-131">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ea8-132">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10ea8-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10ea8-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10ea8-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ea8-134">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ settingsdefinecapabili.\*\*\*\*Propertypolicy**","**CIM \_ settingsdefinecapabili.\*\*\*\*Valuerole**")</span><span class="sxs-lookup"><span data-stu-id="10ea8-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM\_SettingsDefineCapabilities**.**ValueRole**")</span></span>
</dt> </dl>

<span data-ttu-id="10ea8-135">Gibt den Typ des Wertebereichs an, der von Eigenschaften der nicht--Schlüsseleigenschaften der [**CIM- \_ SettingData**](cim-settingdata.md) -Instanz verwendet wird, die nicht NULL sind.</span><span class="sxs-lookup"><span data-stu-id="10ea8-135">Indicates the type of value range used by properties of the non-null, non-key properties of the [**CIM\_SettingData**](cim-settingdata.md) instance.</span></span>

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span data-ttu-id="10ea8-136">**Punkt** (0)</span><span class="sxs-lookup"><span data-stu-id="10ea8-136">**Point** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

<span data-ttu-id="10ea8-137">**Minimums** (1)</span><span class="sxs-lookup"><span data-stu-id="10ea8-137">**Minimums** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

<span data-ttu-id="10ea8-138">**Maximums** (2)</span><span class="sxs-lookup"><span data-stu-id="10ea8-138">**Maximums** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

<span data-ttu-id="10ea8-139">**Inkremente** (3)</span><span class="sxs-lookup"><span data-stu-id="10ea8-139">**Increments** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="10ea8-140">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="10ea8-140">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10ea8-141">**Valuerole**</span><span class="sxs-lookup"><span data-stu-id="10ea8-141">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ea8-142">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10ea8-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10ea8-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="10ea8-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ea8-144">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ settingsdefinecapabili.\*\*\*\*Propertypolicy**","**CIM \_ settingsdefinecapabili.\*\*\*\*ValueRange**")</span><span class="sxs-lookup"><span data-stu-id="10ea8-144">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM\_SettingsDefineCapabilities**.**ValueRange**")</span></span>
</dt> </dl>

<span data-ttu-id="10ea8-145">Die zusätzliche Semantik für die Interpretation der nicht auf NULL festgelegte, nicht Schlüsseleigenschaften der [**CIM \_ SettingData**](cim-settingdata.md) -Instanz.</span><span class="sxs-lookup"><span data-stu-id="10ea8-145">The additional semantics for the interpretation of the non-null, non-key properties of the [**CIM\_SettingData**](cim-settingdata.md) instance.</span></span>

<span data-ttu-id="10ea8-146">"Default" gibt an, dass Eigenschaftswerte der SettingData-Komponenteninstanz als Standardwerte verwendet werden, wenn eine neue SettingData-Instanz für Elemente erstellt wird, deren Funktionen von der zugeordneten Funktionen-Instanz definiert werden.</span><span class="sxs-lookup"><span data-stu-id="10ea8-146">"Default" indicates that property values of the component SettingData instance will be used as default values, when a new SettingData instance is created for elements whose capabilities are defined by the associated Capabilities instance.</span></span>

<span data-ttu-id="10ea8-147">Zwischen den einzelnen Instanzen von SettingData muss für bestimmte Eigenschaften, die denselben semantischen Zweck aufweisen, höchstens eine solche SettingData-Instanz als Standard angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="10ea8-147">Across instances of settingdata, for particular properties having the same semantic purpose, at most one such settingdata instance shall be specified as a default.</span></span>

<span data-ttu-id="10ea8-148">"Optimal" gibt an, dass die SettingData-Instanz optimale Einstellungs Werte für Elemente darstellt, die der zugeordneten Funktionen-Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="10ea8-148">"Optimal" indicates that the SettingData instance represents optimal setting values for elements associated with the associated capabilities instance.</span></span> <span data-ttu-id="10ea8-149">Mehrere komponentensettingdata-Instanzen können als optimal deklariert werden. " Mean "gibt an, dass die nicht-Schlüssel-, nicht-Schlüssel-und nicht-enumerierten, nicht-booleschen numerischen Eigenschaften der zugeordneten SettingData-Instanz einen durchschnittlichen Punkt entlang einer Dimension darstellen.</span><span class="sxs-lookup"><span data-stu-id="10ea8-149">Multiple component SettingData instances may be declared as optimal."Mean" indicates that the non-null, non-key, non-enumerated, non-boolean, numeric properties of the associated SettingData instance represents an average point along some dimension.</span></span> <span data-ttu-id="10ea8-150">Für verschiedene Kombinationen von SettingData-Eigenschaften können mehrere komponentensettingdata-Instanzen als "Mean" deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="10ea8-150">For different combinations of SettingData properties, multiple component SettingData instances may be declared as "Mean".</span></span> <span data-ttu-id="10ea8-151">"Supported" gibt an, dass die nicht-NULL-Eigenschaften der SettingData-Komponente, die nicht NULL sind, einen Satz unterstützter Eigenschaftswerte darstellen, die ansonsten nicht qualifiziert sind.</span><span class="sxs-lookup"><span data-stu-id="10ea8-151">"Supported" indicates that the non-null, non-key properties of the Component SettingData instance represents a set of supported property values that are not otherwise qualified.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="10ea8-152">**Standard** (0)</span><span class="sxs-lookup"><span data-stu-id="10ea8-152">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

<span data-ttu-id="10ea8-153">**Optimal** (1)</span><span class="sxs-lookup"><span data-stu-id="10ea8-153">**Optimal** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

<span data-ttu-id="10ea8-154">**Mittelwert** (2)</span><span class="sxs-lookup"><span data-stu-id="10ea8-154">**Mean** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="10ea8-155">**Unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="10ea8-155">**Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="10ea8-156">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="10ea8-156">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="10ea8-157"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="10ea8-157"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="10ea8-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10ea8-158">Requirements</span></span>



| <span data-ttu-id="10ea8-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10ea8-159">Requirement</span></span> | <span data-ttu-id="10ea8-160">Wert</span><span class="sxs-lookup"><span data-stu-id="10ea8-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10ea8-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10ea8-161">Minimum supported client</span></span><br/> | <span data-ttu-id="10ea8-162">Windows 8</span><span class="sxs-lookup"><span data-stu-id="10ea8-162">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="10ea8-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10ea8-163">Minimum supported server</span></span><br/> | <span data-ttu-id="10ea8-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10ea8-164">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="10ea8-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="10ea8-165">Namespace</span></span><br/>                | <span data-ttu-id="10ea8-166">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="10ea8-166">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="10ea8-167">MOF</span><span class="sxs-lookup"><span data-stu-id="10ea8-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10ea8-168"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="10ea8-168"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="10ea8-169">DLL</span><span class="sxs-lookup"><span data-stu-id="10ea8-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10ea8-170"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="10ea8-170"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="10ea8-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10ea8-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10ea8-172">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="10ea8-172">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 


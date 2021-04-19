---
description: Stellt eine Verknüpfung zwischen der Instanz der Ethernet-Switch-Funktions Funktionen und den minimalen, maximalen, inkrementellen und Standardeinstellungen für eine Ressource bereit.
ms.assetid: 5abd8b2a-9f72-4875-be5c-ce5a2f526e9a
title: Msvm_FeatureSettingsDefineCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingsDefineCapabilities
- Msvm_FeatureSettingsDefineCapabilities.GroupComponent
- Msvm_FeatureSettingsDefineCapabilities.PartComponent
- Msvm_FeatureSettingsDefineCapabilities.PropertyPolicy
- Msvm_FeatureSettingsDefineCapabilities.ValueRole
- Msvm_FeatureSettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ec91a73931458cb6f7e07a7cfc23e71e4665fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360076"
---
# <a name="msvm_featuresettingsdefinecapabilities-class"></a><span data-ttu-id="a6930-103">MSVM \_ featuresettingsdefinecapabili-Klasse</span><span class="sxs-lookup"><span data-stu-id="a6930-103">Msvm\_FeatureSettingsDefineCapabilities class</span></span>

<span data-ttu-id="a6930-104">Stellt eine Verknüpfung zwischen der Instanz der Ethernet-Switch-Funktions Funktionen und den minimalen, maximalen, inkrementellen und Standardeinstellungen für eine Ressource bereit.</span><span class="sxs-lookup"><span data-stu-id="a6930-104">Provides a link between the Ethernet switch feature capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span>

<span data-ttu-id="a6930-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a6930-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6930-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6930-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  Msvm_EthernetSwitchFeatureCapabilities REF GroupComponent;
  Msvm_FeatureSettingData                REF PartComponent;
  uint16                                     PropertyPolicy = 0;
  uint16                                     ValueRole = 3;
  uint16                                     ValueRange = 0;
};
```

## <a name="members"></a><span data-ttu-id="a6930-107">Member</span><span class="sxs-lookup"><span data-stu-id="a6930-107">Members</span></span>

<span data-ttu-id="a6930-108">Die **MSVM \_ featuresettingsdefinecapabili-** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a6930-108">The **Msvm\_FeatureSettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="a6930-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a6930-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a6930-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a6930-110">Properties</span></span>

<span data-ttu-id="a6930-111">Die **MSVM \_ featuresettingsdefinecapabili-** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a6930-111">The **Msvm\_FeatureSettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a6930-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a6930-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6930-113">Datentyp: **[ **MSVM \_ ethernetungwitchfeatuerabilitäten**](msvm-ethernetswitchfeaturecapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="a6930-113">Data type: **[**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a6930-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6930-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6930-115">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="a6930-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a6930-116">Ein Verweis auf eine Instanz der [**MSVM-Klasse " \_ ethernetswitchfeaturecapabili"**](msvm-ethernetswitchfeaturecapabilities.md) , die die Funktionen der Ethernet-Switch-Funktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="a6930-116">A reference to an instance of the [**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) class that represents the Ethernet switch feature capabilities.</span></span> <span data-ttu-id="a6930-117">Diese Eigenschaft wird von der [**CIM- \_ Komponente**](/windows/desktop/CIMWin32Prov/cim-component)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a6930-117">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="a6930-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a6930-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6930-119">Datentyp: **[ **MSVM \_ featuresettingdata**](msvm-featuresettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="a6930-119">Data type: **[**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a6930-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6930-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6930-121">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="a6930-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a6930-122">Ein Verweis auf eine Instanz der [**MSVM \_ featuresettingdata**](msvm-featuresettingdata.md) -Klasse, die die Ressourcen Einstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="a6930-122">A reference to an instance of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represents the resource settings.</span></span> <span data-ttu-id="a6930-123">Diese Eigenschaft wird von der [**CIM- \_ Komponente**](/windows/desktop/CIMWin32Prov/cim-component)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a6930-123">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="a6930-124">**Propertypolicy**</span><span class="sxs-lookup"><span data-stu-id="a6930-124">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6930-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a6930-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a6930-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6930-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6930-127">Gibt an, ob die nicht-NULL-Eigenschaften (nicht-**null**) der **PartComponent** unabhängig oder als korrelierter Satz behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="a6930-127">Specifies whether the non-**Null**, non-key properties of the **PartComponent** are treated independently or as a correlated set.</span></span> <span data-ttu-id="a6930-128">Beispielsweise kann ein unabhängiger Satz von maximalen Eigenschaften definiert werden, aber es gibt keine Beziehung zwischen den einzelnen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a6930-128">For example, an independent set of maximum properties might be defined, yet there is no relationship between each property.</span></span> <span data-ttu-id="a6930-129">Andererseits müssen möglicherweise mehrere korrelierte Sätze von maximalen Eigenschaften definiert werden, wenn die maximalen Werte von einigen der anderen abhängen.</span><span class="sxs-lookup"><span data-stu-id="a6930-129">On the other hand, several correlated sets of maximum properties might need to be defined when the maximum values of each are dependent on some of the others.</span></span>

<span data-ttu-id="a6930-130">Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a6930-130">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a6930-131"><span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Unabhängig** (0)</span><span class="sxs-lookup"><span data-stu-id="a6930-131"><span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Independent** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a6930-132"><span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Korreliert** (1)</span><span class="sxs-lookup"><span data-stu-id="a6930-132"><span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Correlated** (1)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a6930-133">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="a6930-133">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6930-134">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a6930-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a6930-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6930-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6930-136">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="a6930-136">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a6930-137">Gibt eine weitere Semantik für die Interpretation von nicht-**null**-, nicht Schlüsseleigenschaften der Einstellungsdaten an.</span><span class="sxs-lookup"><span data-stu-id="a6930-137">Indicates further semantics on the interpretation of all non-**Null**, non-key properties of the setting data.</span></span>

<span data-ttu-id="a6930-138">Die folgenden Werte werden nur für **nicht-Schlüssel**, nicht-Schlüssel, nicht aufgelistete, nicht-boolesche, numerische Eigenschaften der Einstellungsdaten ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="a6930-138">The values below are only evaluated against non-**Null**, non-key, non-enumerated, non-Boolean, numeric properties of the setting data.</span></span> <span data-ttu-id="a6930-139">Jede Eigenschaft dieses Satzes muss mathematisch mit anderen Instanzen dieser Eigenschaft vergleichbar sein.</span><span class="sxs-lookup"><span data-stu-id="a6930-139">Each property of that set must be mathematically comparable to other instances of that property.</span></span>

<span data-ttu-id="a6930-140">Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a6930-140">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>



| <span data-ttu-id="a6930-141">Wert</span><span class="sxs-lookup"><span data-stu-id="a6930-141">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="a6930-142">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a6930-142">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="a6930-143"><dt>**Punkt**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a6930-143"><dt>**Point**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="a6930-144">Diese Einstellungsdaten Instanz stellt einen einzelnen Satz von Werten bereit.</span><span class="sxs-lookup"><span data-stu-id="a6930-144">This setting data instance provides a single set of values.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span><dl> <span data-ttu-id="a6930-145"><dt>**Minimums**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a6930-145"><dt>**Minimums**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="a6930-146">Diese Einstellungsdaten stellen die minimalen Werte für ausgewertete Eigenschaften bereit.</span><span class="sxs-lookup"><span data-stu-id="a6930-146">This setting data provides minimum values for evaluated properties.</span></span> <span data-ttu-id="a6930-147">Bei Verwendung mit **propertypolicy** = "Independent" muss für beliebige Funktionen nur eine solche Einstellung pro bestimmter Einstellungsdaten Instanz angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a6930-147">When used with **PropertyPolicy** = "Independent", only one such setting per particular setting data instance must be specified for any capabilities.</span></span> <span data-ttu-id="a6930-148">Sofern nicht durch einen Maximums-Wert für denselben Satz von Eigenschaften eingeschränkt, werden alle Werte, die einen höheren Wert als die angegebenen Werte vergleichen, auch von der zugeordneten Funktionen-Instanz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6930-148">Unless restricted by a Maximums value on the same set of properties, all values that compare higher than the specified values are also considered to be supported by the associated capabilities instance.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span><dl> <span data-ttu-id="a6930-149"><dt>**Maximums**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a6930-149"><dt>**Maximums**</dt> <dt>2</dt></span></span> </dl>         | <span data-ttu-id="a6930-150">Diese Einstellungsdaten stellen maximale Werte für ausgewertete Eigenschaften bereit.</span><span class="sxs-lookup"><span data-stu-id="a6930-150">This setting data provides maximum values for evaluated properties.</span></span> <span data-ttu-id="a6930-151">Bei Verwendung mit **propertypolicy** = "Independent" muss für beliebige Funktionen nur eine solche Einstellung pro bestimmter Einstellungsdaten Instanz angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a6930-151">When used with **PropertyPolicy** = "Independent", only one such setting per particular setting data instance must be specified for any capabilities.</span></span> <span data-ttu-id="a6930-152">Sofern nicht durch einen Minimums-Wert für denselben Satz von Eigenschaften eingeschränkt, werden alle Werte, die niedriger als die angegebenen Werte sind, auch von der zugeordneten Funktionen-Instanz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6930-152">Unless restricted by a Minimums value on the same set of properties, all values that compare lower than the specified values are also considered to be supported by the associated capabilities instance.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span><dl> <span data-ttu-id="a6930-153"><dt>**Inkremente**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a6930-153"><dt>**Increments**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="a6930-154">Diese Einstellungsdaten stellen Inkrement-Werte für ausgewertete Eigenschaften bereit.</span><span class="sxs-lookup"><span data-stu-id="a6930-154">This setting data provides increment values for evaluated properties.</span></span> <span data-ttu-id="a6930-155">Wenn eine ausgewertete Eigenschaft für die zugehörigen Funktionen zurzeit keine entsprechenden Minimums-oder Maximums-Werte aufweist, hat die Eigenschaft keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="a6930-155">For the associated capabilities, if an evaluated property currently has no corresponding Minimums or Maximums values, then the property has no affect.</span></span> <span data-ttu-id="a6930-156">Andernfalls muss der Wert (*x*) für jede ausgewertete Eigenschaft zwischen dem *Minimum Value* und dem *MaximumValue*(inklusiv) liegen und die-Eigenschaft aufweisen, die sowohl das Ergebnis von *MaximumValue* minus *x* als auch das Ergebnis von *x* minus *MinimumValue* jeweils ein ganzzahliges Vielfache des *Inkrements* ist.</span><span class="sxs-lookup"><span data-stu-id="a6930-156">Otherwise, for each evaluated property, its value (*x*) must be between the *MinimumValue* and *MaximumValue*, inclusively, and must have the property that both the result of *MaximumValue* minus *x* and the result of *x* minus *MinimumValue* are each an integer multiple of the *Increment*.</span></span> <span data-ttu-id="a6930-157">Wenn *MinimumValue* oder *MaximumValue* nicht angegeben wird und die andere den Wert hat, muss der fehlende Wert davon ausgegangen werden, dass er der niedrigste oder höchste unterstützte Wert für den Datentyp der Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="a6930-157">If either *MinimumValue* or *MaximumValue* is not specified and the other is, then the missing value must be respectively assumed to be the lowest or highest supported value for the property's data type.</span></span> <span data-ttu-id="a6930-158">Wenn außerdem sowohl ein *Minimum Value* als auch ein *MaximumValue* für eine ausgewertete Eigenschaft angegeben werden, muss das Ergebnis von *MaximumValue* minus *MinimumValue* ein ganzzahliges Vielfache des *Inkrements* sein.</span><span class="sxs-lookup"><span data-stu-id="a6930-158">Additionally, if both a *MinimumValue* and a *MaximumValue* are specified for an evaluated property, then the result of *MaximumValue* minus *MinimumValue* must be an integer multiple of the *Increment*.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="a6930-159">**Valuerole**</span><span class="sxs-lookup"><span data-stu-id="a6930-159">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6930-160">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a6930-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a6930-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a6930-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6930-162">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="a6930-162">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a6930-163">Gibt weitere Semantik für die Interpretation der nicht--Schlüsseleigenschaften der Einstellungsdaten an, die nicht **null** sind.</span><span class="sxs-lookup"><span data-stu-id="a6930-163">Specifies further semantics on the interpretation of the non-**Null**, non-key properties of the setting data.</span></span> <span data-ttu-id="a6930-164">Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a6930-164">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>



| <span data-ttu-id="a6930-165">Wert</span><span class="sxs-lookup"><span data-stu-id="a6930-165">Value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="a6930-166">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a6930-166">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="a6930-167"><dt>**Standard**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a6930-167"><dt>**Default**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="a6930-168">Die Eigenschaftswerte der Einstellungsdaten werden als Standardwerte verwendet, wenn eine neue Einstellungsdaten Instanz für Elemente erstellt wird, deren Funktionen durch die zugehörigen Funktionen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a6930-168">The property values of the setting data will be used as default values, when a new setting data instance is created for elements whose capabilities are defined by the associated capabilities.</span></span> <span data-ttu-id="a6930-169">Über Instanzen der Einstellungsdaten hinweg muss für bestimmte Eigenschaften, die denselben semantischen Zweck aufweisen, höchstens eine solche Einstellungsdaten Instanz als Standard angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a6930-169">Across instances of the setting data, for particular properties having the same semantic purpose, at most one such setting data instance must be specified as a default.</span></span><br/> |
| <span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span><dl> <span data-ttu-id="a6930-170"><dt>**Optimal**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a6930-170"><dt>**Optimal**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="a6930-171">Die Setting Data instance stellt optimale Einstellungs Werte für Elemente dar, die den zugeordneten Funktionen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a6930-171">The setting data instance represents optimal setting values for elements associated with the associated capabilities.</span></span> <span data-ttu-id="a6930-172">Mehrere Daten Instanzen der Komponenten Einstellung können als optimal deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="a6930-172">Multiple component setting data instances may be declared as optimal.</span></span><br/>                                                                                                                                                                              |
| <span id="Mean"></span><span id="mean"></span><span id="MEAN"></span><dl> <span data-ttu-id="a6930-173"><dt>**Mittelwert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a6930-173"><dt>**Mean**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="a6930-174">Nicht-**null**-nicht-Schlüssel, nicht aufgelistete, nicht-boolesche numerische Eigenschaften der zugeordneten Einstellungsdaten Instanz repräsentieren einen durchschnittlichen Punkt entlang einer Dimension.</span><span class="sxs-lookup"><span data-stu-id="a6930-174">The non-**Null**, non-key, non-enumerated, non-Boolean, numeric properties of the associated setting data instance represents an average point along some dimension.</span></span> <span data-ttu-id="a6930-175">Für verschiedene Kombinationen der Einstellung von Daten Eigenschaften können mehrere Daten Instanzen der Komponenten Einstellung als **Mittelwert** deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="a6930-175">For different combinations of setting data properties, multiple component setting data instances may be declared as **Mean**.</span></span> <br/>                                                                      |
| <span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span><dl> <span data-ttu-id="a6930-176"><dt>**Unterstützt**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a6930-176"><dt>**Supported**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="a6930-177">Die nicht-**null**-, nicht-Schlüsseleigenschaften der Einstellungsdaten stellen einen Satz unterstützter Eigenschaftswerte dar, die ansonsten nicht qualifiziert sind.</span><span class="sxs-lookup"><span data-stu-id="a6930-177">The non-**Null**, non-key properties of the setting data represents a set of supported property values that are not otherwise qualified.</span></span> <br/>                                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6930-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6930-178">Requirements</span></span>



| <span data-ttu-id="a6930-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6930-179">Requirement</span></span> | <span data-ttu-id="a6930-180">Wert</span><span class="sxs-lookup"><span data-stu-id="a6930-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6930-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6930-181">Minimum supported client</span></span><br/> | <span data-ttu-id="a6930-182">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6930-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a6930-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6930-183">Minimum supported server</span></span><br/> | <span data-ttu-id="a6930-184">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6930-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6930-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6930-185">Namespace</span></span><br/>                | <span data-ttu-id="a6930-186">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a6930-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a6930-187">MOF</span><span class="sxs-lookup"><span data-stu-id="a6930-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6930-188"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a6930-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6930-189">DLL</span><span class="sxs-lookup"><span data-stu-id="a6930-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6930-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a6930-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


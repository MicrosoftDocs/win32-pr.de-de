---
description: Stellt eine Zuordnung zwischen Eigenschaften einer CIM \_ SettingData-Instanz und einer CIM \_ Capabilities-Instanz dar.
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
ms.openlocfilehash: b53f0e72e21b73932c144602308ee599c523ea755b45dae12774109f6a9e010f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899660"
---
# <a name="cim_settingsdefinecapabilities-class"></a>CIM \_ SettingsDefineCapabilities-Klasse

Stellt eine Zuordnung zwischen Eigenschaften einer [**CIM \_ SettingData-Instanz**](cim-settingdata.md) und einer [**CIM \_ Capabilities-Instanz**](cim-capabilities.md) dar.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **CIM \_ SettingsDefineCapabilities-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ SettingsDefineCapabilities-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Funktionen**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Aggregieren, Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) [](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ein Verweis auf die [**CIM \_ Capabilities-Instanz.**](cim-capabilities.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ SettingData**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ein Verweis auf die [**CIM \_ SettingData-Instanz,**](cim-settingdata.md) die zum Definieren der [**CIM \_ Capabilities-Instanz**](cim-capabilities.md) verwendet wird.

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Erforderlich,**](/windows/desktop/WmiSdk/standard-qualifiers) [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-EinstellungenDefineCapabilities**.**ValueRole**", "**\_ CIM-EinstellungenDefineCapabilities**.**ValueRange**")
</dt> </dl>

Gibt an, ob die Nicht-NULL-Eigenschaften der zugeordneten [**CIM \_ SettingData-Instanz**](cim-settingdata.md) unabhängig oder als korrelierte Gruppe behandelt werden. Beispielsweise kann ein unabhängiger Satz maximaler Eigenschaften definiert werden, wenn keine Beziehung zwischen den einzelnen Eigenschaften besteht. Im Gegensatz dazu müssen möglicherweise mehrere korrelierte Sätze von maximalen Eigenschaften definiert werden, wenn die maximalen Werte der einzelnen von einigen der anderen abhängig sind.

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

**Unabhängig** (0)


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

**Korreliert** (1)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-EinstellungenDefineCapabilities**.**PropertyPolicy**", "**\_ CIM-EinstellungenDefineCapabilities**.**ValueRole**")
</dt> </dl>

Gibt den Typ des Wertbereichs an, der von Eigenschaften der Nicht-NULL-Eigenschaften der [**CIM \_ SettingData-Instanz verwendet**](cim-settingdata.md) wird.

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

**Punkt** (0)


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

**Mindestanzahl** (1)


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

**Maximums** (2)


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

**Inkremente** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-EinstellungenDefineCapabilities**.**PropertyPolicy**", "**\_ CIM-EinstellungenDefineCapabilities**.**ValueRange**")
</dt> </dl>

Die zusätzliche Semantik für die Interpretation der Nicht-NULL-Eigenschaften, die keine Schlüsseleigenschaften der [**CIM \_ SettingData-Instanz**](cim-settingdata.md) sind.

"Default" gibt an, dass Eigenschaftswerte der SettingData-Instanz der Komponente als Standardwerte verwendet werden, wenn eine neue SettingData-Instanz für Elemente erstellt wird, deren Funktionen von der zugeordneten Capabilities-Instanz definiert werden.

Für bestimmte Eigenschaften, die denselben semantischen Zweck haben, muss in Instanzen von settingdata nur eine solche settingdata-Instanz als Standard angegeben werden.

"Optimal" gibt an, dass die SettingData-Instanz optimale Einstellungswerte für Elemente darstellt, die der zugeordneten Capabilities-Instanz zugeordnet sind. SettingData-Instanzen mit mehreren Komponenten können als optimal deklariert werden." Mean" gibt an, dass die numerischen Eigenschaften der zugeordneten SettingData-Instanz, die nicht NULL sind, keine Schlüssel, nicht aufzählen und nicht boolesch sind, einen durchschnittlichen Punkt entlang einer Dimension darstellt. Für verschiedene Kombinationen von SettingData-Eigenschaften können mehrere SettingData-Komponenteninstanzen als "Mean" deklariert werden. "Supported" gibt an, dass die Nicht-NULL-Eigenschaften der Component SettingData-Instanz einen Satz unterstützter Eigenschaftswerte darstellt, die andernfalls nicht qualifiziert sind.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Standard** (0)


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

**Optimal** (1)


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

**Mittelwert** (2)


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

**Unterstützt** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Komponente**](cim-component.md)
</dt> </dl>

 


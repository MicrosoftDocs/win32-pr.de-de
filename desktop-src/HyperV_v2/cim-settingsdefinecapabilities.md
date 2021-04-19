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
# <a name="cim_settingsdefinecapabilities-class"></a>CIM \_ settingsdefinecapabili-Klasse

Stellt eine Zuordnung zwischen den Eigenschaften einer [**CIM- \_ SettingData**](cim-settingdata.md) -Instanz und einer CIM-Funktions Instanz dar. [**\_**](cim-capabilities.md)

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

Die **CIM \_ settingsdefinecapabili-** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ settingsdefinecapabili-** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Funktionen**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein Verweis auf die [**CIM- \_ Funktionen**](cim-capabilities.md) -Instanz.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ SettingData**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ein Verweis auf die [**CIM \_ SettingData**](cim-settingdata.md) -Instanz, die verwendet wird, um die CIM-Funktions Instanz zu definieren. [**\_**](cim-capabilities.md)

</dd> <dt>

**Propertypolicy**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ settingsdefinecapabili.****Valuerole**","**CIM \_ settingsdefinecapabili.****ValueRange**")
</dt> </dl>

Gibt an, ob nicht-NULL nicht-Schlüsseleigenschaften der zugeordneten [**CIM \_ SettingData**](cim-settingdata.md) -Instanz unabhängig voneinander behandelt werden. Beispielsweise kann ein unabhängiger Satz von maximalen Eigenschaften definiert werden, wenn keine Beziehung zwischen den einzelnen Eigenschaften besteht. Im Gegensatz dazu müssen möglicherweise mehrere korrelierte Sätze von maximalen Eigenschaften definiert werden, wenn die maximalen Werte der einzelnen von einigen der anderen abhängig sind.

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

**Unabhängig** (0)


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

**Korreliert** (1)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ settingsdefinecapabili.****Propertypolicy**","**CIM \_ settingsdefinecapabili.****Valuerole**")
</dt> </dl>

Gibt den Typ des Wertebereichs an, der von Eigenschaften der nicht--Schlüsseleigenschaften der [**CIM- \_ SettingData**](cim-settingdata.md) -Instanz verwendet wird, die nicht NULL sind.

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

**Punkt** (0)


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

**Minimums** (1)


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

**Maximums** (2)


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

**Inkremente** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Valuerole**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ settingsdefinecapabili.****Propertypolicy**","**CIM \_ settingsdefinecapabili.****ValueRange**")
</dt> </dl>

Die zusätzliche Semantik für die Interpretation der nicht auf NULL festgelegte, nicht Schlüsseleigenschaften der [**CIM \_ SettingData**](cim-settingdata.md) -Instanz.

"Default" gibt an, dass Eigenschaftswerte der SettingData-Komponenteninstanz als Standardwerte verwendet werden, wenn eine neue SettingData-Instanz für Elemente erstellt wird, deren Funktionen von der zugeordneten Funktionen-Instanz definiert werden.

Zwischen den einzelnen Instanzen von SettingData muss für bestimmte Eigenschaften, die denselben semantischen Zweck aufweisen, höchstens eine solche SettingData-Instanz als Standard angegeben werden.

"Optimal" gibt an, dass die SettingData-Instanz optimale Einstellungs Werte für Elemente darstellt, die der zugeordneten Funktionen-Instanz zugeordnet sind. Mehrere komponentensettingdata-Instanzen können als optimal deklariert werden. " Mean "gibt an, dass die nicht-Schlüssel-, nicht-Schlüssel-und nicht-enumerierten, nicht-booleschen numerischen Eigenschaften der zugeordneten SettingData-Instanz einen durchschnittlichen Punkt entlang einer Dimension darstellen. Für verschiedene Kombinationen von SettingData-Eigenschaften können mehrere komponentensettingdata-Instanzen als "Mean" deklariert werden. "Supported" gibt an, dass die nicht-NULL-Eigenschaften der SettingData-Komponente, die nicht NULL sind, einen Satz unterstützter Eigenschaftswerte darstellen, die ansonsten nicht qualifiziert sind.

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

**DMTF reserviert** (..)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Komponente**](cim-component.md)
</dt> </dl>

 


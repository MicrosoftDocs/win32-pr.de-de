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
# <a name="msvm_featuresettingsdefinecapabilities-class"></a>MSVM \_ featuresettingsdefinecapabili-Klasse

Stellt eine Verknüpfung zwischen der Instanz der Ethernet-Switch-Funktions Funktionen und den minimalen, maximalen, inkrementellen und Standardeinstellungen für eine Ressource bereit.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **MSVM \_ featuresettingsdefinecapabili-** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ featuresettingsdefinecapabili-** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ ethernetungwitchfeatuerabilitäten**](msvm-ethernetswitchfeaturecapabilities.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM-Klasse " \_ ethernetswitchfeaturecapabili"**](msvm-ethernetswitchfeaturecapabilities.md) , die die Funktionen der Ethernet-Switch-Funktion darstellt. Diese Eigenschaft wird von der [**CIM- \_ Komponente**](/windows/desktop/CIMWin32Prov/cim-component)geerbt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ featuresettingdata**](msvm-featuresettingdata.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ featuresettingdata**](msvm-featuresettingdata.md) -Klasse, die die Ressourcen Einstellungen darstellt. Diese Eigenschaft wird von der [**CIM- \_ Komponente**](/windows/desktop/CIMWin32Prov/cim-component)geerbt.

</dd> <dt>

**Propertypolicy**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die nicht-NULL-Eigenschaften (nicht-**null**) der **PartComponent** unabhängig oder als korrelierter Satz behandelt werden. Beispielsweise kann ein unabhängiger Satz von maximalen Eigenschaften definiert werden, aber es gibt keine Beziehung zwischen den einzelnen Eigenschaften. Andererseits müssen möglicherweise mehrere korrelierte Sätze von maximalen Eigenschaften definiert werden, wenn die maximalen Werte von einigen der anderen abhängen.

Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)).

<dl> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Unabhängig** (0)
</dt> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Korreliert** (1)
</dt> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Gibt eine weitere Semantik für die Interpretation von nicht-**null**-, nicht Schlüsseleigenschaften der Einstellungsdaten an.

Die folgenden Werte werden nur für **nicht-Schlüssel**, nicht-Schlüssel, nicht aufgelistete, nicht-boolesche, numerische Eigenschaften der Einstellungsdaten ausgewertet. Jede Eigenschaft dieses Satzes muss mathematisch mit anderen Instanzen dieser Eigenschaft vergleichbar sein.

Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)).



| Wert                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <dt>**Punkt**</dt> <dt>0</dt> </dl>                     | Diese Einstellungsdaten Instanz stellt einen einzelnen Satz von Werten bereit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span><dl> <dt>**Minimums**</dt> <dt>1</dt> </dl>         | Diese Einstellungsdaten stellen die minimalen Werte für ausgewertete Eigenschaften bereit. Bei Verwendung mit **propertypolicy** = "Independent" muss für beliebige Funktionen nur eine solche Einstellung pro bestimmter Einstellungsdaten Instanz angegeben werden. Sofern nicht durch einen Maximums-Wert für denselben Satz von Eigenschaften eingeschränkt, werden alle Werte, die einen höheren Wert als die angegebenen Werte vergleichen, auch von der zugeordneten Funktionen-Instanz unterstützt. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span><dl> <dt>**Maximums**</dt> <dt>2</dt> </dl>         | Diese Einstellungsdaten stellen maximale Werte für ausgewertete Eigenschaften bereit. Bei Verwendung mit **propertypolicy** = "Independent" muss für beliebige Funktionen nur eine solche Einstellung pro bestimmter Einstellungsdaten Instanz angegeben werden. Sofern nicht durch einen Minimums-Wert für denselben Satz von Eigenschaften eingeschränkt, werden alle Werte, die niedriger als die angegebenen Werte sind, auch von der zugeordneten Funktionen-Instanz unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span><dl> <dt>**Inkremente**</dt> <dt>3</dt> </dl> | Diese Einstellungsdaten stellen Inkrement-Werte für ausgewertete Eigenschaften bereit. Wenn eine ausgewertete Eigenschaft für die zugehörigen Funktionen zurzeit keine entsprechenden Minimums-oder Maximums-Werte aufweist, hat die Eigenschaft keine Auswirkung. Andernfalls muss der Wert (*x*) für jede ausgewertete Eigenschaft zwischen dem *Minimum Value* und dem *MaximumValue*(inklusiv) liegen und die-Eigenschaft aufweisen, die sowohl das Ergebnis von *MaximumValue* minus *x* als auch das Ergebnis von *x* minus *MinimumValue* jeweils ein ganzzahliges Vielfache des *Inkrements* ist. Wenn *MinimumValue* oder *MaximumValue* nicht angegeben wird und die andere den Wert hat, muss der fehlende Wert davon ausgegangen werden, dass er der niedrigste oder höchste unterstützte Wert für den Datentyp der Eigenschaft ist. Wenn außerdem sowohl ein *Minimum Value* als auch ein *MaximumValue* für eine ausgewertete Eigenschaft angegeben werden, muss das Ergebnis von *MaximumValue* minus *MinimumValue* ein ganzzahliges Vielfache des *Inkrements* sein. <br/> |



 

</dd> <dt>

**Valuerole**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Gibt weitere Semantik für die Interpretation der nicht--Schlüsseleigenschaften der Einstellungsdaten an, die nicht **null** sind. Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)).



| Wert                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**Standard**</dt> Wert <dt>0</dt> </dl>         | Die Eigenschaftswerte der Einstellungsdaten werden als Standardwerte verwendet, wenn eine neue Einstellungsdaten Instanz für Elemente erstellt wird, deren Funktionen durch die zugehörigen Funktionen definiert werden. Über Instanzen der Einstellungsdaten hinweg muss für bestimmte Eigenschaften, die denselben semantischen Zweck aufweisen, höchstens eine solche Einstellungsdaten Instanz als Standard angegeben werden.<br/> |
| <span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span><dl> <dt>**Optimal**</dt> <dt>1</dt> </dl>         | Die Setting Data instance stellt optimale Einstellungs Werte für Elemente dar, die den zugeordneten Funktionen zugeordnet sind. Mehrere Daten Instanzen der Komponenten Einstellung können als optimal deklariert werden.<br/>                                                                                                                                                                              |
| <span id="Mean"></span><span id="mean"></span><span id="MEAN"></span><dl> <dt>**Mittelwert**</dt> <dt>2</dt> </dl>                     | Nicht-**null**-nicht-Schlüssel, nicht aufgelistete, nicht-boolesche numerische Eigenschaften der zugeordneten Einstellungsdaten Instanz repräsentieren einen durchschnittlichen Punkt entlang einer Dimension. Für verschiedene Kombinationen der Einstellung von Daten Eigenschaften können mehrere Daten Instanzen der Komponenten Einstellung als **Mittelwert** deklariert werden. <br/>                                                                      |
| <span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span><dl> <dt>**Unterstützt**</dt> <dt>3</dt> </dl> | Die nicht-**null**-, nicht-Schlüsseleigenschaften der Einstellungsdaten stellen einen Satz unterstützter Eigenschaftswerte dar, die ansonsten nicht qualifiziert sind. <br/>                                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


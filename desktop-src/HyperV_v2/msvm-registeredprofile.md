---
description: Beschreibt eine Gruppe von Klassen mit erforderlichen Eigenschaften und Methoden, die zum Verwalten einer realen Entität oder zur Unterstützung eines Verwendungsszenarios auf interoperable Weise erforderlich sind.
ms.assetid: 75644856-3B47-43B8-835C-783A6BEE7251
title: Msvm_RegisteredProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredProfile
- Msvm_RegisteredProfile.InstanceID
- Msvm_RegisteredProfile.Caption
- Msvm_RegisteredProfile.Description
- Msvm_RegisteredProfile.ElementName
- Msvm_RegisteredProfile.RegisteredOrganization
- Msvm_RegisteredProfile.OtherRegisteredOrganization
- Msvm_RegisteredProfile.RegisteredName
- Msvm_RegisteredProfile.RegisteredVersion
- Msvm_RegisteredProfile.AdvertiseTypes
- Msvm_RegisteredProfile.AdvertiseTypeDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0773ad1b7c992211e8bc578ac2cf2bea7706313918581ef2da9df8e2887b536d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535770"
---
# <a name="msvm_registeredprofile-class"></a>Msvm \_ RegisteredProfile-Klasse

Beschreibt eine Gruppe von Klassen mit erforderlichen Eigenschaften und Methoden, die zum Verwalten einer realen Entität oder zur Unterstützung eines Verwendungsszenarios auf interoperable Weise erforderlich sind.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Msvm_RegisteredProfile : CIM_RegisteredProfile
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 RegisteredOrganization;
  string OtherRegisteredOrganization;
  string RegisteredName;
  string RegisteredVersion;
  uint16 AdvertiseTypes[];
  string AdvertiseTypeDescriptions[];
};
```

## <a name="members"></a>Member

Die **Msvm \_ RegisteredProfile-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ RegisteredProfile-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AdvertiseTypeDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Zeichenfolgen, das zusätzliche Informationen im Zusammenhang mit der **AdvertiseType-Eigenschaft** enthält. Eine Beschreibung muss angegeben werden, wenn **"AdvertiseType"** den Wert 1 (Sonstige) hat. Ein Eintrag in diesem Array entspricht demselben Index im **AdvertiseTypes-Array.** Diese Eigenschaft wird von [**CIM \_ RegisteredProfile geerbt.**](/previous-versions//ee309375(v=vs.85))

</dd> <dt>

**AdvertiseTypes**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Ankündigung für die Profilinformationen an. Sie wird von den Werbediensten der WBEM-Infrastruktur verwendet, um zu bestimmen, was mit welchen Mechanismen angekündigt werden soll. Die -Eigenschaft ist ein Array, sodass das Profil mit mehreren Mechanismen angekündigt werden kann. Wenn diese Eigenschaft NULL **ist,** entspricht dies der Angabe des Werts 2 (Nicht angekündigt). Diese Eigenschaft wird von [**CIM \_ RegisteredProfile geerbt.**](/previous-versions//ee309375(v=vs.85))

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)
</dt> <dt>

<span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Nicht angekündigt** (2)
</dt> <dt>

<span id="SLP_"></span><span id="slp_"></span>**SLP** (3 )
</dt> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel,** **Überschreibung**
</dt> </dl>

Eine Zeichenfolge, die eine Instanz dieser Klasse eindeutig identifiziert. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**OtherRegisteredOrganization**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** ( 256 )
</dt> </dl>

Eine Zeichenfolge, die eine Beschreibung der Organisation enthält, **wenn RegisteredOrganization** 1 (Other) enthält. Diese Eigenschaft wird von [**CIM \_ RegisteredProfile geerbt.**](/previous-versions//ee309375(v=vs.85))

</dd> <dt>

**RegisteredName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** ( 256 )
</dt> </dl>

Der Name dieses registrierten Profils. Da mehrere Versionen für denselben **RegisteredName** vorhanden sein können, muss die Kombination aus **RegisteredName,** **RegisteredOrganization** und **RegisteredVersion** das registrierte Profil innerhalb des Bereichs der Organisation eindeutig identifizieren. Diese Eigenschaft wird von [**CIM \_ RegisteredProfile geerbt.**](/previous-versions//ee309375(v=vs.85))

</dd> <dt>

**RegisteredOrganization**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Organisation, die dieses Profil definiert. Diese Eigenschaft wird von [**CIM \_ RegisteredProfile geerbt.**](/previous-versions//ee309375(v=vs.85))

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)
</dt> <dt>

<span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)
</dt> <dt>

<span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)
</dt> <dt>

<span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consortium for Service Innovation** (4)
</dt> <dt>

<span id="FAST"></span><span id="fast"></span>**FAST** (5)
</dt> <dt>

<span id="GGF"></span><span id="ggf"></span>**GGF** (6)
</dt> <dt>

<span id="INTAP"></span><span id="intap"></span>**INTAP** (7)
</dt> <dt>

<span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)
</dt> <dt>

<span id="NAC"></span><span id="nac"></span>**NAC** (9)
</dt> <dt>

<span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**"10 Northwest Energy Efficiency Alliance"** (10)
</dt> <dt>

<span id="SNIA"></span><span id="snia"></span>**SNIA** (11)
</dt> <dt>

<span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**TM-Forum** (12)
</dt> <dt>

<span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**Die geöffnete Gruppe** (13)
</dt> <dt>

<span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)
</dt> <dt>

<span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)
</dt> <dt>

<span id="IETF"></span><span id="ietf"></span>**IETF** (16)
</dt> <dt>

<span id="INCITS"></span><span id="incits"></span>**INCITS** (17)
</dt> <dt>

<span id="ISO"></span><span id="iso"></span>**ISO** (18)
</dt> <dt>

<span id="W3C"></span><span id="w3c"></span>**W3C** (19)
</dt> <dt>

<span id="__20___________OGF"></span><span id="__20___________ogf"></span>**/20 OGF** (20)
</dt> <dt>

<span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**Das grüne Raster** (21)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (.. )
</dt> </dl>

</dd> <dt>

**RegisteredVersion**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version dieses Profils. Die Zeichenfolge muss im folgenden Formular sein: "*M*. *N*. *U*" Where:

-   *M* ist die Hauptversion (in numerischer Form), die die Erstellung oder letzte Änderung des Profils beschreibt.
-   *N* ist die Nebenversion (in numerischer Form), die die Erstellung oder letzte Änderung des Profils beschreibt.
-   *U* ist das Update (in numerischer Form), das die Erstellung oder letzte Änderung des Profils beschreibt.

Diese Eigenschaft wird von [**CIM \_ RegisteredProfile geerbt.**](/previous-versions//ee309375(v=vs.85))

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\Stamm-Interop<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


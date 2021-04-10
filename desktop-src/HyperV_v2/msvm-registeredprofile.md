---
description: Beschreibt eine Reihe von Klassen mit erforderlichen Eigenschaften und Methoden, die zum Verwalten einer realen Entität oder zur Unterstützung eines Verwendungs Szenarios auf interoperable Weise erforderlich sind.
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
ms.openlocfilehash: a7014687355524fbe10ff01869cac6c3fd35a894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042327"
---
# <a name="msvm_registeredprofile-class"></a>MSVM \_ registeredprofile-Klasse

Beschreibt eine Reihe von Klassen mit erforderlichen Eigenschaften und Methoden, die zum Verwalten einer realen Entität oder zur Unterstützung eines Verwendungs Szenarios auf interoperable Weise erforderlich sind.

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

Die **MSVM \_ registeredprofile** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ registeredprofile** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**"Werbe Beschreibungen"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Zeichen folgen, das zusätzliche Informationen bereitstellt, die sich auf die " **Werbung** "-Eigenschaft beziehen. Es muss eine Beschreibung angegeben werden, wenn der **Typ** von "1 (sonstige)" lautet. Ein Eintrag in diesem Array entspricht dem gleichen Index im **Werbe Types** -Array. Diese Eigenschaft wird von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))geerbt.

</dd> <dt>

**Werbung Typen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Ankündigung für die Profilinformationen an. Sie wird von den Ankündigungs Diensten der WBEM-Infrastruktur verwendet, um zu bestimmen, was durch welche Mechanismen angekündigt werden soll. Die-Eigenschaft ist ein Array, sodass das Profil mithilfe verschiedener Mechanismen angekündigt werden kann. Wenn diese Eigenschaft **null** ist, entspricht dies der Angabe des Werts 2 (nicht angekündigt). Diese Eigenschaft wird von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))geerbt.

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)
</dt> <dt>

<span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Nicht angekündigt** (2)
</dt> <dt>

<span id="SLP_"></span><span id="slp_"></span>**SLP** (3)
</dt> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **override**
</dt> </dl>

Eine Zeichenfolge, die eine Instanz dieser Klasse eindeutig identifiziert. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Otherregisteredorganization**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (256)
</dt> </dl>

Eine Zeichenfolge, die eine Beschreibung der Organisation bereitstellt, wenn **RegisteredOrganization** 1 (Sonstiges) enthält. Diese Eigenschaft wird von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))geerbt.

</dd> <dt>

**Registeredname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (256)
</dt> </dl>

Der Name dieses registrierten Profils. Da für denselben **registeredname** mehrere Versionen vorhanden sein können, muss die Kombination von **registeredname**, **RegisteredOrganization** und **registeredversion** das registrierte Profil innerhalb des Bereichs der Organisation eindeutig identifizieren. Diese Eigenschaft wird von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))geerbt.

</dd> <dt>

**RegisteredOrganization**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Organisation, die dieses Profil definiert. Diese Eigenschaft wird von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))geerbt.

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)
</dt> <dt>

<span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)
</dt> <dt>

<span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)
</dt> <dt>

<span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Konsortium für Dienst Innovation** (4)
</dt> <dt>

<span id="FAST"></span><span id="fast"></span>**Schnell** (5)
</dt> <dt>

<span id="GGF"></span><span id="ggf"></span>**Ggf** . (6)
</dt> <dt>

<span id="INTAP"></span><span id="intap"></span>**Einzug** (7)
</dt> <dt>

<span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)
</dt> <dt>

<span id="NAC"></span><span id="nac"></span>**NAC** (9)
</dt> <dt>

<span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**10 Nordwest-Energieeffizienz-Alliance** (10)
</dt> <dt>

<span id="SNIA"></span><span id="snia"></span>**Sja** (11)
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

<span id="__20___________OGF"></span><span id="__20___________ogf"></span>**20 OGF** . (20)
</dt> <dt>

<span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**Grünes Raster** (21)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (.. )
</dt> </dl>

</dd> <dt>

**Registeredversion**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version dieses Profils. Die Zeichenfolge muss folgendes Format aufweisen: "*M*. *N*. *U*"WHERE:

-   *M* ist die Hauptversion (in numerischer Form), in der die Profilerstellung oder die letzte Änderung beschrieben wird.
-   *N* ist die neben Version (in numerischer Form), in der die Profilerstellung oder die letzte Änderung beschrieben wird.
-   *U* ist das Update (in numerischer Form), das die Profilerstellung oder die letzte Änderung beschreibt.

Diese Eigenschaft wird von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root- \\ Interop<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


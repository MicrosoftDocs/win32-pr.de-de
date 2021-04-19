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
# <a name="msvm_settingsdefinecapabilities-class"></a>MSVM \_ settingsdefinecapabili-Klasse

Stellt eine Verknüpfung zwischen der Funktionen-Instanz und den minimalen, maximalen, inkrementellen und Standardeinstellungen für eine Ressource bereit.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **MSVM \_ settingsdefinecapabili-** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ settingsdefinecapabili-** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM- \_ Funktionen**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Instanz der Funktionen. Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Einstellung, die zum Definieren der zugeordneten Funktionen Instanz verwendet wird. Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**Propertypolicy**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob nicht-NULL-Eigenschaften, die keine Schlüsseleigenschaften der zugeordneten Einstellungsdaten Instanz sind, unabhängig voneinander behandelt werden. Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)) und immer auf 0 (unabhängig) festgelegt.

</dd> <dt>

**Supportstatement**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bezeichnet die Unterstützungs Anweisung.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Produktion** (0)


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Vorab** Version (1)


</dt> <dd>

> [!Note]  
> War **nicht** für die Produktion in Windows 10, Version 1703.

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserviert** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Jede weitere Semantik für die Interpretation aller nicht Schlüsseleigenschaften der Einstellungsdaten, die nicht NULL sind. Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**Valuerole**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Jede weitere Semantik für die Interpretation der nicht--Schlüsseleigenschaften der Einstellungsdaten, die nicht NULL sind. Diese Eigenschaft wird von [**CIM \_ settingsdefinecapabiligeerbt**](/previous-versions//cc136913(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Werte für die **valuerole** -und **ValueRange** -Eigenschaften werden in den folgenden Paaren verwendet:

-   Point/default (0/0)
-   Minimums/unterstützt (1/3)
-   Maximums/unterstützt (2/3)
-   Inkremente/unterstützt (3/3).

"Point" bedeutet, dass alle Eigenschaften des Objekts " **PartComponent** " den Standard der Plattform darstellen.

"Minimums" und "Maximums" bedeuten, dass alle Eigenschaften des Objekts " **PartComponent** " die kleinsten und größten möglichen Werte für diese Eigenschaften darstellen, die von der Plattform basierend auf der aktuellen Computerkonfiguration unterstützt werden.

"Inkremente" gibt die Granularität an, mit der Sie die Einstellungen vergrößern oder verkleinern können.

Der Zugriff auf die **MSVM \_ settingsdefinecapabili-** Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ settingsdefinecapabilitäten**](cim-settingsdefinecapabilities.md)
</dt> <dt>

[**CIM \_ settingsdefinecapabilitäten**](/previous-versions//cc136913(v=vs.85))
</dt> <dt>

[**MSVM \_ settingsdefinecapabili(v1)**](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[Ressourcen Verwaltungs Klassen](resource-management-classes.md)
</dt> </dl>

 


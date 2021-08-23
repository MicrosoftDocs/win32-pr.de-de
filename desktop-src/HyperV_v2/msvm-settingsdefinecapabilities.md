---
description: Stellt eine Verknüpfung zwischen der Capabilities-Instanz und den minimalen, maximalen, inkrementellen und Standardeinstellungen für eine Ressource bereit.
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
ms.openlocfilehash: 7194632af7bc1154e6a9bbca1dd5ef0bcca0fb46ab13693d20160ea404068adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950463"
---
# <a name="msvm_settingsdefinecapabilities-class"></a>Msvm \_ SettingsDefineCapabilities-Klasse

Stellt eine Verknüpfung zwischen der Capabilities-Instanz und den minimalen, maximalen, inkrementellen und Standardeinstellungen für eine Ressource bereit.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **Msvm \_ SettingsDefineCapabilities-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ SettingsDefineCapabilities-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **\_ CIM-Funktionen**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Capabilities-Instanz. Diese Eigenschaft wird von [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))geerbt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Einstellung, die verwendet wird, um die zugeordnete Capabilities-Instanz zu definieren. Diese Eigenschaft wird von [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))geerbt.

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Nicht-NULL-Eigenschaften der zugeordneten Einstellungsdateninstanz unabhängig oder als korrelierter Satz behandelt werden. Diese Eigenschaft wird von [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) geerbt und immer auf 0 (unabhängig) festgelegt.

</dd> <dt>

**SupportStatement**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert die Support-Anweisung.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10 Version 1703 hinzugefügt.

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Produktion** (0)


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Vorabversion** (1)


</dt> <dd>

> [!Note]  
> War **nonProduction** in Windows 10, Version 1703.

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserviert** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Jede weitere Semantik zur Interpretation aller Nicht-NULL-, Nicht-Schlüsseleigenschaften der Einstellungsdaten. Diese Eigenschaft wird von [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))geerbt.

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Jede weitere Semantik zur Interpretation der Nicht-NULL-Eigenschaften der Einstellungsdaten. Diese Eigenschaft wird von [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Werte für die Eigenschaften **ValueRole** und **ValueRange** werden in den folgenden Paaren verwendet:

-   Point/Default (0/0)
-   Minimums/Supported (1/3)
-   Maximalwerte/Unterstützt (2/3)
-   Inkremente/Unterstützt (3/3).

"Punkt" bedeutet, dass jede der Eigenschaften im **PartComponent-Objekt** den Plattformstandard darstellt.

"Minimums" und "Maximums" bedeuten, dass jede der Eigenschaften im **PartComponent-Objekt** die kleinsten und größtmöglichen Werte für diese Eigenschaften darstellt, die von der Plattform basierend auf Ihrer aktuellen Computerkonfiguration unterstützt werden.

"Inkremente" gibt die Granularität an, mit der Sie die Einstellungen erhöhen oder verringern können.

Der Zugriff auf die **Msvm \_ SettingsDefineCapabilities-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-EinstellungenDefineCapabilities**](cim-settingsdefinecapabilities.md)
</dt> <dt>

[**\_CIM-EinstellungenDefineCapabilities**](/previous-versions//cc136913(v=vs.85))
</dt> <dt>

[**\_Msvm-EinstellungenDefineCapabilities (V1)**](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[Ressourcenverwaltungsklassen](resource-management-classes.md)
</dt> </dl>

 


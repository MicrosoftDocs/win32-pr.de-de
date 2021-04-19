---
description: Stellt die Isolations Einstellungsdaten dar.
ms.assetid: f6bf5fcf-61c4-4e69-8ba0-fff4c4873368
title: Msvm_EthernetSwitchPortIsolationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortIsolationSettingData
- Msvm_EthernetSwitchPortIsolationSettingData.IsolationMode
- Msvm_EthernetSwitchPortIsolationSettingData.AllowUntaggedTraffic
- Msvm_EthernetSwitchPortIsolationSettingData.DefaultIsolationId
- Msvm_EthernetSwitchPortIsolationSettingData.EnableMultiTenantStack
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d7761b090cfd3bf2ae6aaaa92e9c5d09d55eae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368834"
---
# <a name="msvm_ethernetswitchportisolationsettingdata-class"></a>MSVM \_ ethernetzwitchportisolationsettingdata-Klasse

Stellt die Isolations Einstellungsdaten dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("83AF2CCB-72C9-4479-A285-94E58A98CAA6"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Isolation Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortIsolationSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32  IsolationMode = 0;
  boolean AllowUntaggedTraffic = FALSE;
  uint32  DefaultIsolationId = 0;
  Boolean EnableMultiTenantStack = FALSE;
};
```

## <a name="members"></a>Member

Die **MSVM \_ ethernetzwitchportisolationsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ ethernetzwitchportisolationsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**"Zugewuntaggedtraffic"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Gibt an, ob der Port nicht markierten Datenverkehr senden/empfangen darf.

</dd> <dt>

**Defaultisolationid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Die standardvirtualsubnetz-ID oder VLAN, die für den gesamten Sende-/empfangsdatenverkehr festgelegt wird, wenn " **zuordnduntaggedtraffic** " **true**

</dd> <dt>

**Enablemultitenantstack**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

**True** gibt an, dass der Netzwerk Stapel auf der VM auf die Isolations Konfiguration zugreifen kann. Der Standardwert ist **false**.

</dd> <dt>

**IsolationMode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Gibt an, ob der Port **VLAN** oder **virtualsubnetztid** für die Isolation verwendet. **Nativevirtualsubnettid** wird für wNv-virtualsubnetztid-basierte Netzwerke verwendet.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (0)


</dt> <dd></dd> <dt>

<span id="NativeVirtualSubnetId"></span><span id="nativevirtualsubnetid"></span><span id="NATIVEVIRTUALSUBNETID"></span>

**Nativevirtualsubnetztid** (1)


</dt> <dd></dd> <dt>

<span id="ExternalVirtualSubnetId"></span><span id="externalvirtualsubnetid"></span><span id="EXTERNALVIRTUALSUBNETID"></span>

**Externalvirtualsubnetztid** (2)


</dt> <dd></dd> <dt>

<span id="VLAN"></span><span id="vlan"></span>

**VLAN** (3)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ ethernetzwitchportfeaturesettingdata**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 


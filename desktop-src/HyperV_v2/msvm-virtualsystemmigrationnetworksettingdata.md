---
description: Stellt das Netzwerk dar, auf dem der Dienst für die Migration des virtuellen Systems auf die Migration eingehender virtueller Systeme lauscht.
ms.assetid: 24458602-ff5c-45c2-8053-00315b59d3bb
title: Msvm_VirtualSystemMigrationNetworkSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationNetworkSettingData
- Msvm_VirtualSystemMigrationNetworkSettingData.InstanceID
- Msvm_VirtualSystemMigrationNetworkSettingData.Caption
- Msvm_VirtualSystemMigrationNetworkSettingData.Description
- Msvm_VirtualSystemMigrationNetworkSettingData.ElementName
- Msvm_VirtualSystemMigrationNetworkSettingData.SubnetNumber
- Msvm_VirtualSystemMigrationNetworkSettingData.PrefixLength
- Msvm_VirtualSystemMigrationNetworkSettingData.Metric
- Msvm_VirtualSystemMigrationNetworkSettingData.Tags
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4f7c24bb754148fa8ede12292f308164512af646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862059"
---
# <a name="msvm_virtualsystemmigrationnetworksettingdata-class"></a>MSVM \_ virtualsystemmigrationnetworksettingdata-Klasse

Stellt das Netzwerk dar, auf dem der Dienst für die Migration des virtuellen Systems auf die Migration eingehender virtueller Systeme lauscht.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationNetworkSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SubnetNumber;
  uint8  PrefixLength;
  uint32 Metric;
  string Tags[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ virtualsystemmigrationnetworksettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualsystemmigrationnetworksettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von der [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse geerbt.

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

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Metrik**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Prioritäts Metrik dieses Netzwerks für die Migration. Niedrigere Werte sind höher als die Priorität.

</dd> <dt>

**PrefixLength**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Länge des Subnetzpräfixes des Migrationsnetzwerks.

</dd> <dt>

**Subnetnumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Subnetznummer des Migrationsnetzwerks.

</dd> <dt>

**Tags**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Tags, die darstellen, welches Verwaltungssystem dieses Netzwerk für den Dienst für die virtuelle System Migration festgelegt hat.

</dd> </dl>

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

[**CIM- \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**Modifynetworksettings**](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 


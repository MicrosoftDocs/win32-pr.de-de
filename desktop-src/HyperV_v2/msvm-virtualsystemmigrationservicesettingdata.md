---
description: Stellt die Einstellungen für den Dienst für die virtuelle System Migration auf einem Host dar.
ms.assetid: 56711134-9a4a-49bd-8a0e-ce679b959adf
title: Msvm_VirtualSystemMigrationServiceSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingData
- Msvm_VirtualSystemMigrationServiceSettingData.InstanceID
- Msvm_VirtualSystemMigrationServiceSettingData.Caption
- Msvm_VirtualSystemMigrationServiceSettingData.Description
- Msvm_VirtualSystemMigrationServiceSettingData.ElementName
- Msvm_VirtualSystemMigrationServiceSettingData.EnableVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveStorageMigration
- Msvm_VirtualSystemMigrationServiceSettingData.AuthenticationType
- Msvm_VirtualSystemMigrationServiceSettingData.EnableCompression
- Msvm_VirtualSystemMigrationServiceSettingData.EnableSmbTransport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8c8685e468d60983408c52a985169c61be91f632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339751"
---
# <a name="msvm_virtualsystemmigrationservicesettingdata-class"></a>MSVM \_ virtualsystemmigrationservicesettingdata-Klasse

Stellt die Einstellungen für den Dienst für die virtuelle System Migration auf einem Host dar. Die Eigenschaften für diese Klasse können nicht direkt geändert werden. Der Client muss die **MSVM \_ virtualsystemmigrationservice. modifyservicesettings** -Methode abrufen, um diese Eigenschaften zu ändern.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  boolean EnableVirtualSystemMigration;
  uint32  MaximumActiveVirtualSystemMigration;
  uint32  MaximumActiveStorageMigration;
  uint32  AuthenticationType;
  boolean EnableCompression = True;
  boolean EnableSmbTransport = False;
};
```

## <a name="members"></a>Member

Die **MSVM \_ virtualsystemmigrationservicesettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualsystemmigrationservicesettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AuthenticationType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Authentifizierungsmechanismus an, der für die Netzwerkverbindungen der virtuellen System Migration verwendet wird. Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) -Methode der [**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md) -Klasse geändert werden kann.

<dt>

<span id="CredSSP"></span><span id="credssp"></span><span id="CREDSSP"></span>

" **Kredssp** " (0)


</dt> <dd></dd> <dt>

<span id="Kerberos"></span><span id="kerberos"></span><span id="KERBEROS"></span>

**Kerberos** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

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

**EnableCompression**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Komprimierung des Live Migrations Datenverkehrs aktiviert oder deaktiviert ist. True gibt den Wert aktiviert an.

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

</dd> <dt>

**Enablesmbtransport**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Verwendung von SMB als Transporttyp für die Übertragung des VM-Zustands zwischen den Hyper-V-Hosts bei der Migration virtueller Systeme aktiviert oder deaktiviert ist. **True** gibt den Wert aktiviert an. Eine höhere Leistung wird erzielt, wenn RDMA-NICs während der VM-Live Migration für den SMB-Transport konfiguriert sind. Wenn der **enablesmbtransport** -Wert true ist, wird der Wert von **EnableCompression** ignoriert.

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

</dd> <dt>

**Enablevirtualsystemmigration**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Migration virtueller Systeme aktiviert oder deaktiviert ist. Die Speicher Migration ist immer aktiviert. Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) -Methode der [**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md) -Klasse geändert werden kann.

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

**Maximumactivestoragemigration**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die maximal zulässige Anzahl aktiver Speicher Migrationen an. Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) -Methode der [**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md) -Klasse geändert werden kann.

</dd> <dt>

**Maximumactivevirtualsystemmigration**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die maximal zulässige Anzahl aktiver virtueller System Migrationen an. Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) -Methode der [**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md) -Klasse geändert werden kann.

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

[**Modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 


---
description: Stellt die Einstellungen für den Migrationsdienst des virtuellen Systems auf einem Host dar.
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
ms.openlocfilehash: 9ab3feab1f34d0f44ce5cd0618915d8575af9e463a9ec772961c185e946ac094
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963500"
---
# <a name="msvm_virtualsystemmigrationservicesettingdata-class"></a>Msvm \_ VirtualSystemMigrationServiceSettingData-Klasse

Stellt die Einstellungen für den Migrationsdienst des virtuellen Systems auf einem Host dar. Die Eigenschaften für diese Klasse können nicht direkt geändert werden. Der Client muss die **Msvm \_ VirtualSystemMigrationService.ModifyServiceSettings-Methode** aufrufen, um eine dieser Eigenschaften zu ändern.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **Msvm \_ VirtualSystemMigrationServiceSettingData-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ VirtualSystemMigrationServiceSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AuthenticationType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Authentifizierungsmechanismus an, der für Netzwerkverbindungen der Migration virtueller Systeme verwendet wird. Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) der [**Msvm \_ VirtualSystemMigrationService-Klasse**](msvm-virtualsystemmigrationservice.md) geändert werden kann.

<dt>

<span id="CredSSP"></span><span id="credssp"></span><span id="CREDSSP"></span>

**CredSSP** (0)


</dt> <dd></dd> <dt>

<span id="Kerberos"></span><span id="kerberos"></span><span id="KERBEROS"></span>

**Kerberos** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von der [**CIM \_ ManagedElement-Klasse**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.

</dd> <dt>

**EnableCompression**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Komprimierung des Livemigrationsdatenverkehrs aktiviert oder deaktiviert ist. True gibt an, dass aktiviert ist.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyResourceSettings-Methode**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) geändert werden kann.

**Windows 8.1:** Dieser Wert wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.

</dd> <dt>

**EnableSmbTransport**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Verwendung von SMB als Transporttyp für die Übertragung des VM-Zustands zwischen den Hyper-V-Hosts während der Migration des virtuellen Systems aktiviert oder deaktiviert ist. **True** gibt an, dass aktiviert ist. Eine höhere Leistung wird erzielt, wenn RDMA-NICs während der Vm-Livemigration für den SMB-Transport konfiguriert sind. Wenn **der EnableSmbTransport-Wert** TRUE ist, wird der Wert von **EnableCompression** ignoriert.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyResourceSettings-Methode**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) geändert werden kann.

**Windows 8.1:** Dieser Wert wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.

</dd> <dt>

**EnableVirtualSystemMigration**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Migration des virtuellen Systems aktiviert oder deaktiviert ist. Storage Migration ist immer aktiviert. Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) der [**Msvm \_ VirtualSystemMigrationService-Klasse**](msvm-virtualsystemmigrationservice.md) geändert werden kann.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**MaximumActiveStorageMigration**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die maximale Anzahl der zulässigen aktiven Speichermigrationen an. Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) der [**Msvm \_ VirtualSystemMigrationService-Klasse**](msvm-virtualsystemmigrationservice.md) geändert werden kann.

</dd> <dt>

**MaximumActiveVirtualSystemMigration**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die maximale Anzahl aktiver virtueller Systemmigrationen an, die zulässig sind. Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) der [**Msvm \_ VirtualSystemMigrationService-Klasse**](msvm-virtualsystemmigrationservice.md) geändert werden kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 


---
description: Stellt die Einstellungen für den Virtualisierungsdienst dar, der auf einem einzelnen Hostsystem vorhanden ist.
ms.assetid: E3265AFE-0117-4F59-9A6B-34CEA7A61EDD
title: Msvm_VirtualSystemManagementServiceSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementServiceSettingData
- Msvm_VirtualSystemManagementServiceSettingData.InstanceID
- Msvm_VirtualSystemManagementServiceSettingData.Caption
- Msvm_VirtualSystemManagementServiceSettingData.Description
- Msvm_VirtualSystemManagementServiceSettingData.ElementName
- Msvm_VirtualSystemManagementServiceSettingData.BiosLockString
- Msvm_VirtualSystemManagementServiceSettingData.DefaultExternalDataRoot
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskPath
- Msvm_VirtualSystemManagementServiceSettingData.MaximumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.NumaSpanningEnabled
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerContact
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerName
- Msvm_VirtualSystemManagementServiceSettingData.HbaLunTimeout
- Msvm_VirtualSystemManagementServiceSettingData.MaximumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.CurrentWWNNAddress
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskCachingMode
- Msvm_VirtualSystemManagementServiceSettingData.HypervisorRootSchedulerEnabled
- Msvm_VirtualSystemManagementServiceSettingData.EnhancedSessionModeEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3ccb0a1a9bc4a10ec7f8a366f012446e0374dab299f8ee779f16cfeb38fb005b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147973"
---
# <a name="msvm_virtualsystemmanagementservicesettingdata-class"></a>Msvm \_ VirtualSystemManagementServiceSettingData-Klasse

Stellt die Einstellungen für den Virtualisierungsdienst dar, der auf einem einzelnen Hostsystem vorhanden ist. Die Eigenschaften für diese Klasse können nicht direkt geändert werden. Der Client muss die [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) aufrufen, um eine dieser Eigenschaften zu ändern.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementServiceSettingData : CIM_SettingData
{
  string  InstanceID = "Microsoft:host";
  string  Caption = "Hyper-V Virtual System Management Service";
  string  Description = "Settings for the Virtual System Management Service";
  string  ElementName = "Hyper-V Virtual System Management Service";
  string  BiosLockString;
  string  DefaultExternalDataRoot = "root\ProgramData\Microsoft\Windows\Virtualization";
  string  DefaultVirtualHardDiskPath = "root\Users\Public\Documents\Virtual Hard Disks";
  string  MaximumMacAddress;
  string  MinimumMacAddress;
  boolean NumaSpanningEnabled;
  string  PrimaryOwnerContact = "";
  string  PrimaryOwnerName = "Administrators";
  uint32  HbaLunTimeout;
  string  MaximumWWPNAddress;
  string  MinimumWWPNAddress;
  string  CurrentWWNNAddress;
  uint16  DefaultVirtualHardDiskCachingMode;
  boolean HypervisorRootSchedulerEnabled;
  boolean EnhancedSessionModeEnabled;
};
```

## <a name="members"></a>Member

Die **Msvm \_ VirtualSystemManagementServiceSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ VirtualSystemManagementServiceSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BiosLockString**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)
</dt> </dl>

Wird von OEMs verwendet, um BIOS-gesperrten Windows betriebssystemen die Ausführung auf dem virtuellen Computer zu ermöglichen. Diese Zeichenfolge muss genau 32 Zeichen lang sein.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Hyper-V Virtual System Management Service" festgelegt.

</dd> <dt>

**CurrentWWNNAddress**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die WWNN-Adresse (World Wide Node Name) für dynamisch generierte Weltweitnamenadressen, die für synthetische Hostbusadapter verwendet werden.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

</dd> <dt>

**DefaultExternalDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")
</dt> </dl>

Der standardmäßige externe Datenstamm. Standardmäßig *"root* \\ ProgramData \\ Microsoft Windows \\ \\ Virtualization".

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

</dd> <dt>

**DefaultVirtualHardDiskCachingMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Zwischenspeichern von Dateien im Arbeitsspeicher standardmäßig für Datenträger verwendet werden soll. Dieser Wert kann pro Datenträger im Feld **CachingMode** der [**Msvm \_ StorageAllocationSettingData-Klasse überschrieben**](msvm-storageallocationsettingdata.md) werden.

> [!Note]  
> Hinzugefügt in Windows 10 und Windows Server 2016.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

**Keine Zwischenspeicherung** (3)


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

**Cache Sharable Parents** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**DefaultVirtualHardDiskPath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Standardpfad der virtuellen Festplatte. Standardmäßig *"root* \\ Users Public Documents Virtual Hard \\ \\ \\ Disks".

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Einstellungen für den Virtual System Management Service" festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Hyper-V Virtual System Management Service" festgelegt. Durch Ändern dieser Eigenschaft wird die **ElementName-Eigenschaft** der zugeordneten [**CIM \_ LogicalDevice-Ableitung**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geändert.

</dd> <dt>

**EnhancedSessionModeEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der erweiterte Sitzungsmodus auf dem Server zulässig ist. **True gibt** an, dass zulässig ist, andernfalls **False.**

**Windows 8.1:** Dieser Wert wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.

</dd> <dt>

**HbaLunTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie lange das synthetische Fibre Channel virtuelles Gerät wartet, bis eine logische Gerätenummer (LOGICAL Unit Number, LUN) angezeigt wird, bevor ein virtueller Computer gestartet wird.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

</dd> <dt>

**HypervisorRootSchedulerEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Hypervisor-Stammplaner aktiviert ist.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ SettingData geerbt**](/previous-versions//cc136911(v=vs.85))und immer auf "Microsoft:*host"* festgelegt, wobei *host* der NetBIOS-Name des Hostcomputersystems ist.

</dd> <dt>

**MaximumMacAddress**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale MAC-Adresse für dynamisch generierte MAC-Adressen.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

</dd> <dt>

**MaximumWWPNAddress**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale WWPN-Adresse (World Wide Port Name) für dynamisch generierte Weltweitnamenadressen, die für synthetische Hostbusadapter verwendet werden.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

</dd> <dt>

**MinimumMacAddress**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die minimale MAC-Adresse für dynamisch generierte MAC-Adressen.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

</dd> <dt>

**MinimumWWPNAddress**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die mindestadresse für den Namen des weltweiten Ports für dynamisch generierte Weltweitnamenadressen, die für synthetische Hostbusadapter verwendet werden.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

</dd> <dt>

**NumaSpanningEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Arbeitsspeicher von NUMA-Knoten (Remote Nonuniform Memory Access) beim Starten eines virtuellen Computers oder beim Zuweisen von Arbeitsspeicher zu einem virtuellen Computer durch dynamischen Arbeitsspeicher zugeordnet werden kann. Dies kann einer der folgenden Werte sein.



| Wert                                                                                | Bedeutung                                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**Richtig**</dt> </dl>  | Arbeitsspeicher kann sowohl von lokalen als auch von Remote-NUMA-Knoten zugeordnet werden.<br/>                   |
| <dl> <dt>**Falsch**</dt> </dl> | Arbeitsspeicher kann nur über den NUMA-Knoten zugeordnet werden, der dem virtuellen Computer zugewiesen ist.<br/> |



 

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| General Information \| 001.4")
</dt> </dl>

Beschreibt, wie der primäre Systembesitzer erreicht werden kann (z. B. Telefonnummer oder E-Mail-Adresse). Standardmäßig leer. Dieser Name darf 256 Zeichen nicht überschreiten.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| General Information \| 001.3")
</dt> </dl>

Der Name des primären Systembesitzers. Standardmäßig "Administratoren". Dieser Wert darf 64 Zeichen nicht überschreiten.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyServiceSettings-Methode**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ VirtualSystemManagementServiceSettingData-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))
</dt> <dt>

[Verwaltungsklassen für virtuelle Systeme](virtual-system-management-classes.md)
</dt> </dl>

 


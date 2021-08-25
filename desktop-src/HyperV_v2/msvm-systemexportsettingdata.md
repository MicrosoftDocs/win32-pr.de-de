---
description: Ordnet einen virtuellen Computer und die zugehörigen Exporteinstellungsdaten zu.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Msvm_SystemExportSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemExportSettingData
- Msvm_SystemExportSettingData.ManagedElement
- Msvm_SystemExportSettingData.SettingData
- Msvm_SystemExportSettingData.IsDefault
- Msvm_SystemExportSettingData.IsCurrent
- Msvm_SystemExportSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 39e096c466dd4accc1a2c87ececd6ce23ba27cb173e6b5fa0d6728852ad59cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811870"
---
# <a name="msvm_systemexportsettingdata-class"></a>Msvm \_ SystemExportSettingData-Klasse

Ordnet einen virtuellen Computer und die zugehörigen Exporteinstellungsdaten zu. Vor dem Aufrufen der [**ExportSystemDefinition-Methode**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) kann eine Instanz von [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) mithilfe dieser Zuordnung abgerufen werden.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemExportSettingData : CIM_ElementSettingData
{
  CIM_ComputerSystem                  REF ManagedElement;
  Msvm_VirtualSystemExportSettingData REF SettingData;
  uint16                                  IsDefault = 1;
  uint16                                  IsCurrent = 1;
  uint16                                  IsNext = 0;
};
```

## <a name="members"></a>Member

Die **Msvm \_ SystemExportSettingData-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ SystemExportSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Iscurrent**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Einstellung, auf die verwiesen wird, derzeit beim Vorgang des Elements verwendet wird oder dass diese Informationen unbekannt sind. Diese Eigenschaft wird von [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.



| Wert                                                                        | Bedeutung                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unbekannt<br/>     |
| <dl> <dt>1</dt> </dl> | Aktuell<br/>     |
| <dl> <dt>2</dt> </dl> | Nicht aktuell<br/> |



 

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Referenzeinstellung eine Standardeinstellung für das Element ist oder dass diese Informationen unbekannt sind. Diese Eigenschaft wird von [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.



| Wert                                                                        | Bedeutung                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unbekannt<br/>     |
| <dl> <dt>1</dt> </dl> | Standard<br/>     |
| <dl> <dt>2</dt> </dl> | Nicht standardmäßig<br/> |



 

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Einstellung, auf die verwiesen wird, die nächste anzuwendende Einstellung ist. Beispielsweise kann die Anwendung bei einer Anforderung zur Erneutinitialisierung, Zurücksetzung und Neukonfiguration erfolgen. Dies kann eine permanente Einstellung oder eine Einstellung sein, die nur einmal verwendet wird, wie durch das -Flag angegeben. Wenn es sich um eine permanente Einstellung handelt, wird die Einstellung jedes Mal angewendet, wenn das verwaltete Element erneut initialisiert wird, bis dieses Flag manuell zurückgesetzt wird. Wenn es sich jedoch um eine einzelne Verwendung handelt, wird das Flag automatisch gelöscht, nachdem die Einstellungen angewendet wurden. Wenn dieses Flag angegeben wird (d. h. auf einen anderen Wert als 0 (Unbekannt)) festgelegt ist, hat dies Vorrang vor allen Einstellungsdaten, die möglicherweise als Standard angegeben wurden. Beispiel: Wenn das verwaltete Element ein Computersystem ist und der Wert dieses Flags 1 (Is Next) ist, ist die Einstellung beim nächsten Zurücksetzen des Systems wirksam. Wenn dieses Flag nicht geändert wird, wird es für nachfolgende Systemrücksetzungen beibehalten. Wenn dieses Flag jedoch auf 3 (Is Next For Single Use) festgelegt ist, wird diese Einstellung nur einmal verwendet, und das Flag wird danach auf 2 (Is Not Next) zurückgesetzt. Wenn das System also im obigen Beispiel in kurzer Folge neu gestartet wird, wird die Einstellung beim zweiten Neustart nicht verwendet.

Diese Eigenschaft wird von [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.



| Wert                                                                        | Bedeutung                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>0</dt> </dl> | Unbekannt<br/>                |
| <dl> <dt>1</dt> </dl> | Is Next<br/>                |
| <dl> <dt>2</dt> </dl> | Is Not Next<br/>            |
| <dl> <dt>3</dt> </dl> | Ist der nächste Schritt für die einmalige Verwendung<br/> |



 

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData.ManagedElement")
</dt> </dl>

Verweis auf den virtuellen Computer. Diese Eigenschaft wird von [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.

</dd> <dt>

**Settingdata**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) \_ ("CIM-ElementSettingData.SettingData")
</dt> </dl>

Verweis auf die Exporteinstellungsdaten für den virtuellen Computer. Diese Eigenschaft wird von [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ SystemExportSettingData-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


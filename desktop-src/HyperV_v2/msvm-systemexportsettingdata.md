---
description: Ordnet einen virtuellen Computer und seine Export Einstellungsdaten zu.
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
ms.openlocfilehash: 8203a45bb911743bb064c1a686da0b3d8abe99bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346693"
---
# <a name="msvm_systemexportsettingdata-class"></a>MSVM \_ systemexportsettingdata-Klasse

Ordnet einen virtuellen Computer und seine Export Einstellungsdaten zu. Vor dem Aufrufen der [**exportsystemdefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse kann eine Instanz von [**MSVM \_ virtualsystemexportsettingdata**](msvm-virtualsystemexportsettingdata.md) mithilfe dieser Zuordnung abgerufen werden.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **MSVM \_ systemexportsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ systemexportsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Einstellung, auf die verwiesen wird, derzeit im Vorgang des-Elements verwendet wird, oder ob diese Informationen unbekannt sind. Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.



| Wert                                                                        | Bedeutung                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unbekannt<br/>     |
| <dl> <dt>1</dt> </dl> | Aktuell<br/>     |
| <dl> <dt>2</dt> </dl> | Nicht aktuell<br/> |



 

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die referenzierte Einstellung eine Standardeinstellung für das Element ist, oder ob diese Informationen unbekannt sind. Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.



| Wert                                                                        | Bedeutung                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unbekannt<br/>     |
| <dl> <dt>1</dt> </dl> | Standard<br/>     |
| <dl> <dt>2</dt> </dl> | Nicht Standard<br/> |



 

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die referenzierte Einstellung die nächste Einstellung ist, die angewendet werden soll. Die Anwendung kann z. b. bei einer erneuten Initialisierung, zurück Setzung und Neukonfiguration der Anforderung stattfinden. Dies könnte eine permanente Einstellung oder eine Einstellung sein, die nur ein Mal verwendet wird, wie durch das-Flag angegeben. Wenn es sich um eine permanente Einstellung handelt, wird die Einstellung jedes Mal angewendet, wenn das verwaltete Element erneut initialisiert wird, bis dieses Flag manuell zurückgesetzt wird. Wenn es sich jedoch um eine einzelne Verwendung handelt, wird das Flag nach dem Anwenden der Einstellungen automatisch gelöscht. Wenn dieses Flag angegeben wird (d. h. auf einen anderen Wert als 0 (unbekannt) festgelegt ist), hat dies Vorrang vor den Einstellungsdaten, die möglicherweise als Standard angegeben wurden. Beispiel: Wenn das verwaltete Element ein Computersystem ist und der Wert dieses Flags 1 ist (steht als nächstes), wird die Einstellung beim nächsten Zurücksetzen des Systems wirksam. Und wenn dieses Flag nicht geändert wird, wird es für nachfolgende System zurück Stellungen beibehalten. Wenn dieses Flag jedoch auf den Wert 3 festgelegt ist (steht für die einmalige Verwendung), wird diese Einstellung nur einmal verwendet, und das Flag würde danach auf 2 zurückgesetzt (nicht weiter). Im obigen Beispiel wird die Einstellung beim zweiten Neustart nicht verwendet, wenn das System in einer schnell Folge neu gestartet wird.

Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.



| Wert                                                                        | Bedeutung                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>0</dt> </dl> | Unbekannt<br/>                |
| <dl> <dt>1</dt> </dl> | Nächste<br/>                |
| <dl> <dt>2</dt> </dl> | Nicht weiter<br/>            |
| <dl> <dt>3</dt> </dl> | Nächste Verwendung<br/> |



 

</dd> <dt>

**"Managedelement"**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ Computersystem**](msvm-computersystem.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ elementsettingdata. managedelta")
</dt> </dl>

Verweis auf den virtuellen Computer. Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ virtualsystemexportsettingdata**](msvm-virtualsystemexportsettingdata.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ elementsettingdata. SettingData")
</dt> </dl>

Verweis auf die Export Einstellungsdaten für den virtuellen Computer. Diese Eigenschaft wird von [**CIM \_ elementsettingdata**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ systemexportsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


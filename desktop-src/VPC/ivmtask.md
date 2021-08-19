---
title: IVMTask-Schnittstelle (VPCCOMInterfaces.h)
description: Verwenden Sie die IVMTask-Schnittstelle, um asynchrone Aufgaben für verschiedene COM-Methoden zu überwachen und zu steuern.
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- IVMTask-Schnittstelle Virtueller PC
- IVMTask-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMTask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6e7afa39e8e95ac2a961212b3a3fe7b74e73bc8b1100ac44b34d09700ab58bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998720"
---
# <a name="ivmtask-interface"></a>IVMTask-Schnittstelle

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Verwenden Sie die **IVMTask-Schnittstelle,** um asynchrone Aufgaben für verschiedene COM-Methoden zu überwachen und zu steuern.

## <a name="members"></a>Member

Die **IVMTask-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMTask verfügt** auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IVMTask-Schnittstelle** verfügt über diese Methoden.



| Methode                                                 | Beschreibung                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Abbrechen**](ivmtask-cancel.md)                       | Bricht die Aufgabe ab.<br/>                                                                |
| [**WaitForCompletion**](ivmtask-waitforcompletion.md) | Wartet, bis der Task abgeschlossen ist oder das angegebene Time out-Intervall verstreicht.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IVMTask-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                        | Zugriffstyp          | Beschreibung                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [**Beschreibung**](ivmtask-description.md)<br/>           | Schreibgeschützt<br/> | Eine Beschreibung des Tasks.<br/>                              |
| [**Fehler**](ivmtask-error.md)<br/>                       | Schreibgeschützt<br/> | Der für diesen Task aufgezeichnete Fehler.<br/>                       |
| [**ErrorDescription**](ivmtask-errordescription.md)<br/> | Schreibgeschützt<br/> | Die lokalisierte Fehlerbeschreibung, die für diesen Task aufgezeichnet wurde.<br/> |
| [**Id**](ivmtask-id.md)<br/>                             | Schreibgeschützt<br/> | Ein eindeutiger Bezeichner für diesen Task.<br/>                      |
| [**Iscancelable**](ivmtask-iscancelable.md)<br/>         | Schreibgeschützt<br/> | Gibt an, ob der Task abgebrochen werden kann.<br/>             |
| [**IsComplete**](ivmtask-iscomplete.md)<br/>             | Schreibgeschützt<br/> | Gibt an, ob die Aufgabe abgeschlossen wurde.<br/>               |
| [**PercentCompleted**](ivmtask-percentcompleted.md)<br/> | Schreibgeschützt<br/> | Der Abschlussprozentsatz der Aufgabe.<br/>                  |
| [**Ergebnis**](ivmtask-result.md)<br/>                     | Schreibgeschützt<br/> | Das Ergebnis der Aufgabe.<br/>                                 |



 

## <a name="remarks"></a>Hinweise

Ein **IVMTask-Objekt** wird von Methoden zurückgegeben, die möglicherweise einen erheblichen Zeitraum für den Abschluss benötigen. Dadurch kann die Anwendung den Fortschritt des gewünschten Vorgangs überwachen, ohne die weitere Ausführung zu blockieren, während auf den Abschluss des Vorgangs gewartet wird.

Die folgenden Methoden geben ein **IVMTask-Objekt** zurück, das zum Nachverfolgen des Fortschritts verwendet werden kann:

-   [**IVMGuestOS::Logoff**](ivmguestos-logoff.md)
-   [**IVMGuestOS::Restart**](ivmguestos-restart.md)
-   [**IVMGuestOS::Shutdown**](ivmguestos-shutdown.md)
-   [**IVMHardDisk::Compact**](ivmharddisk-compact.md)
-   [**IVMHardDisk::Convert**](ivmharddisk-convert.md)
-   [**IVMHardDisk::Merge**](ivmharddisk-merge.md)
-   [**IVMHardDisk::MergeTo**](ivmharddisk-mergeto.md)
-   [**IVMVirtualMachine::MergeUndoDisks**](ivmvirtualmachine-mergeundodisks.md)
-   [**IVMVirtualMachine::Reset**](ivmvirtualmachine-reset.md)
-   [**IVMVirtualMachine::Save**](ivmvirtualmachine-save.md)
-   [**IVMVirtualMachine::Startup**](ivmvirtualmachine-startup.md)
-   [**IVMVirtualMachine::Startup2**](ivmvirtualmachine-startup2.md)
-   [**IVMVirtualMachine::TurnOff**](ivmvirtualmachine-turnoff.md)
-   [**IVMVirtualPC::CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [**IVMVirtualPC::CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [**IVMVirtualPC::CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask ist als ab72b222-6e9c-48ae-aa54-85e3e635767c definiert.<br/>                    |



 


---
title: Ivmtask-Schnittstelle (vpccominterfaces. h)
description: Verwenden Sie die ivmtask-Schnittstelle, um asynchrone Aufgaben für verschiedene com-Methoden zu überwachen und zu steuern.
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- Ivmtask Interface Virtual PC
- Virtueller Computer für ivmtask Interface, beschrieben
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
ms.openlocfilehash: a8e1d519471fe5b1fc32cb6365d1139243c85538
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518383"
---
# <a name="ivmtask-interface"></a>Ivmtask-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Verwenden Sie die **ivmtask** -Schnittstelle, um asynchrone Aufgaben für verschiedene com-Methoden zu überwachen und zu steuern.

## <a name="members"></a>Member

Die **ivmtask** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmtask** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmtask** -Schnittstelle verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Abbrechen**](ivmtask-cancel.md)                       | Bricht die Aufgabe ab.<br/>                                                                |
| [**Waitforcompletion**](ivmtask-waitforcompletion.md) | Wartet, bis die Aufgabe beendet oder das angegebene Timeout Intervall abläuft.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **ivmtask** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                        | Zugriffstyp          | BESCHREIBUNG                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [**Beschreibung**](ivmtask-description.md)<br/>           | Schreibgeschützt<br/> | Eine Beschreibung des Tasks.<br/>                              |
| [**Fehler**](ivmtask-error.md)<br/>                       | Schreibgeschützt<br/> | Der für diese Aufgabe aufgezeichnete Fehler.<br/>                       |
| [**ErrorDescription**](ivmtask-errordescription.md)<br/> | Schreibgeschützt<br/> | Die lokalisierte Fehlerbeschreibung, die für diese Aufgabe aufgezeichnet wurde.<br/> |
| [**id**](ivmtask-id.md)<br/>                             | Schreibgeschützt<br/> | Ein eindeutiger Bezeichner für diese Aufgabe.<br/>                      |
| [**IsCancelable**](ivmtask-iscancelable.md)<br/>         | Schreibgeschützt<br/> | Gibt an, ob der Task abgebrochen werden kann.<br/>             |
| [**IsComplete**](ivmtask-iscomplete.md)<br/>             | Schreibgeschützt<br/> | Gibt an, ob die Aufgabe abgeschlossen wurde.<br/>               |
| [**Prozentuabgeschlossen**](ivmtask-percentcompleted.md)<br/> | Schreibgeschützt<br/> | Der Abschluss Prozentsatz der Aufgabe.<br/>                  |
| [**Dadurch**](ivmtask-result.md)<br/>                     | Schreibgeschützt<br/> | Das Ergebnis der Aufgabe.<br/>                                 |



 

## <a name="remarks"></a>Bemerkungen

Ein **ivmtask** -Objekt wird von Methoden zurückgegeben, für die möglicherweise eine beträchtliche Zeitspanne benötigt wird. Dies ermöglicht es der Anwendung, den Fortschritt des gewünschten Vorgangs zu überwachen, ohne Sie zu erzwingen, dass eine weitere Ausführung blockiert wird, während auf den Abschluss des Vorgangs gewartet wird.

Die folgenden Methoden geben ein **ivmtask** -Objekt zurück, das verwendet werden kann, um den Fortschritt zu verfolgen:

-   [**Ivmguestos:: abmelden**](ivmguestos-logoff.md)
-   [**Ivmguestos:: Restart**](ivmguestos-restart.md)
-   [**Ivmguestos:: Shutdown**](ivmguestos-shutdown.md)
-   [**Ivmharddisk:: Compact**](ivmharddisk-compact.md)
-   [**Ivmharddisk:: Convert**](ivmharddisk-convert.md)
-   [**Ivmharddisk:: Merge**](ivmharddisk-merge.md)
-   [**Ivmharddisk:: mergeto**](ivmharddisk-mergeto.md)
-   [**Ivmvirtualmachine:: mergeundodisks**](ivmvirtualmachine-mergeundodisks.md)
-   [**Ivmvirtualmachine:: Reset**](ivmvirtualmachine-reset.md)
-   [**Ivmvirtualmachine:: Save**](ivmvirtualmachine-save.md)
-   [**Ivmvirtualmachine:: Startup**](ivmvirtualmachine-startup.md)
-   [**Ivmvirtualmachine:: Startup2**](ivmvirtualmachine-startup2.md)
-   [**Ivmvirtualmachine:: Turnoff**](ivmvirtualmachine-turnoff.md)
-   [**Ivmvirtualpc:: kreatedifferencingvirtualharddisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [**Ivmvirtualpc:: kreatedynamicvirtualharddisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [**Ivmvirtualpc:: kreatefixedvirtualharddisk**](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.<br/>                    |



 


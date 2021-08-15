---
description: Erweitert das IShellDispatch-Objekt um eine Vielzahl neuer Funktionen.
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: IShellDispatch2-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 481e64c00ced458be05255af451206a42d449c42d157794dfd1077cf2dda278a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721090"
---
# <a name="ishelldispatch2-object"></a>IShellDispatch2-Objekt

Erweitert das [**IShellDispatch-Objekt**](ishelldispatch.md) um eine Vielzahl neuer Funktionen.

> [!Note]  
> **IShellDispatch2** wird implementiert und über das [**Shell-Objekt**](shell.md) aufgerufen.

 

## <a name="members"></a>Member

Das **IShellDispatch2-Objekt** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **IShellDispatch2-Objekt** verfügt über diese Methoden.



| Methode                                                               | Beschreibung                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**CanStartStopService**](ishelldispatch2-canstartstopservice.md)   | Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und beenden kann.<br/>    |
| [**FindPrinter**](ishelldispatch2-findprinter.md)                   | Zeigt das Dialogfeld **Drucker suchen** an.<br/>                               |
| [**GetSystemInformation**](ishelldispatch2-getsysteminformation.md) | Ruft Systeminformationen ab.<br/>                                           |
| [**Isrestricted**](ishelldispatch2-isrestricted.md)                 | Ruft die Einschränkungseinstellung einer Gruppe aus der Registrierung ab.<br/>              |
| [**IsServiceRunning**](ishelldispatch2-isservicerunning.md)         | Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.<br/> |
| [**ServiceStart**](ishelldispatch2-servicestart.md)                 | Startet einen benannten Dienst.<br/>                                                 |
| [**ServiceStop**](ishelldispatch2-servicestop.md)                   | Beendet einen benannten Dienst.<br/>                                                  |
| [**ShellExecute**](ishelldispatch2-shellexecute.md)                 | Führt einen angegebenen Vorgang für eine angegebene Datei aus.<br/>                     |
| [**ShowBrowserBar**](ishelldispatch2-showbrowserbar.md)             | Zeigt eine Browserleiste an.<br/>                                                 |



 

## <a name="remarks"></a>Hinweise

Eine Erläuterung Windows Dienste finden Sie in der [Dokumentation zu Diensten.](../services/services.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Shell-Objekt**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> </dl>

 

 

---
description: Erweitert das ishelldispatch-Objekt mit einer Reihe von neuen Funktionen.
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: IShellDispatch2-Objekt (Shldisp. h)
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
ms.openlocfilehash: 79d3abbed038e09f2e73c62e5e3d9b16545e8f60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978032"
---
# <a name="ishelldispatch2-object"></a>IShellDispatch2-Objekt

Erweitert das [**ishelldispatch**](ishelldispatch.md) -Objekt mit einer Reihe von neuen Funktionen.

> [!Note]  
> **IShellDispatch2** wird implementiert, und der Zugriff erfolgt über das [**Shellobjekt**](shell.md) .

 

## <a name="members"></a>Member

Das **IShellDispatch2** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **IShellDispatch2** -Objekt verfügt über diese Methoden.



| Methode                                                               | BESCHREIBUNG                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**Canstartstopservice**](ishelldispatch2-canstartstopservice.md)   | Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und Abbrechen kann.<br/>    |
| [**Findprinter**](ishelldispatch2-findprinter.md)                   | Zeigt das Dialogfeld **Drucker suchen** an.<br/>                               |
| [**Getsysteminformation**](ishelldispatch2-getsysteminformation.md) | Ruft Systeminformationen ab.<br/>                                           |
| [**IsRestricted**](ishelldispatch2-isrestricted.md)                 | Ruft die Einschränkungs Einstellung einer Gruppe aus der Registrierung ab.<br/>              |
| [**Isservicerunning**](ishelldispatch2-isservicerunning.md)         | Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.<br/> |
| [**Servicestart**](ishelldispatch2-servicestart.md)                 | Startet einen benannten Dienst.<br/>                                                 |
| [**Servicestop**](ishelldispatch2-servicestop.md)                   | Beendet einen benannten Dienst.<br/>                                                  |
| [**ShellExecute**](ishelldispatch2-shellexecute.md)                 | Führt einen angegebenen Vorgang für eine angegebene Datei aus.<br/>                     |
| [**Showbrowserbar**](ishelldispatch2-showbrowserbar.md)             | Zeigt eine Browserleiste an.<br/>                                                 |



 

## <a name="remarks"></a>Bemerkungen

Eine Erläuterung der Windows-Dienste finden Sie in der Dokumentation zu [Diensten](../services/services.md) .

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Shellobjekt**](shell.md)
</dt> <dt>

[**Ishelldispatch**](ishelldispatch.md)
</dt> </dl>

 

 

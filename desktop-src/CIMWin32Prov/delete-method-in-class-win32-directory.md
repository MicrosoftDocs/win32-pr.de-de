---
description: Mit der DELETE WMI class-Methode wird die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) gelöscht.
ms.assetid: 5663b8a8-3089-475b-8a36-454a7315bfca
ms.tgt_platform: multiple
title: Delete-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 843583698c11c1b9ad8f08e83aa6e4b894b55db8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340132"
---
# <a name="delete-method-of-the-win32_directory-class"></a>Delete-Methode der Win32- \_ Verzeichnis Klasse

Mit der **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode wird die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) gelöscht.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich gelöscht wurde, und jede andere Zahl gibt einen Fehler an.

<dl> <dt>

**0**
</dt> <dd>

Die Anforderung wurde erfolgreich gesendet.

</dd> <dt>

**2**
</dt> <dd>

Der Zugriff wurde verweigert.

</dd> <dt>

**8**
</dt> <dd>

Ein nicht angegebener Fehler ist aufgetreten.

</dd> <dt>

**9**
</dt> <dd>

Der angegebene Name war ungültig.

</dd> <dt>

**10**
</dt> <dd>

Das angegebene Objekt ist bereits vorhanden.

</dd> <dt>

**11**
</dt> <dd>

Das Dateisystem ist nicht NTFS.

</dd> <dt>

**12**
</dt> <dd>

Die Plattform ist nicht Windows.

</dd> <dt>

**13**
</dt> <dd>

Das Laufwerk ist nicht identisch.

</dd> <dt>

**14**
</dt> <dd>

Das Verzeichnis ist nicht leer.

</dd> <dt>

**15**
</dt> <dd>

Es ist eine Freigabe Verletzung aufgetreten.

</dd> <dt>

**16**
</dt> <dd>

Die angegebene Startdatei war ungültig.

</dd> <dt>

**17**
</dt> <dd>

Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.

</dd> <dt>

**21**
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ordner sind nicht notwendigerweise permanente Ergänzungen zu einem Dateisystem. Manchmal müssen Ordner gelöscht werden, da Sie möglicherweise nicht mehr benötigt werden, da sich die Rolle des Computers geändert hat oder die Ordner versehentlich erstellt wurden.

Löschen ermöglicht es Ihnen, Ordner zu löschen: Sie binden einfach an den fraglichen Ordner und dann die Delete-Methode. Nachdem die Delete-Methode aufgerufen wurde, wird der Ordner dauerhaft aus dem Dateisystem entfernt. Er wird nicht an den Papierkorb gesendet. Außerdem wird keine Bestätigung angezeigt ("möchten Sie diesen Ordner wirklich löschen?"). Stattdessen wird der Ordner sofort entfernt.

Sie können schreibgeschützte Ordner nicht mithilfe von FileSystemObject löschen. Dies kann jedoch mithilfe von WMI erfolgen. Wenn das Skript WMI verwendet und Sie keinen schreibgeschützten Ordner entfernen möchten, müssen Sie die lesbare Eigenschaft verwenden, um den Ordner Status zu überprüfen, bevor Sie ihn löschen.

## <a name="examples"></a>Beispiele

Das folgende VBScript-Codebeispiel löscht den Ordner C: \\ Scripts.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Delete
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ Verzeichnis**](win32-directory.md)
</dt> </dl>

 


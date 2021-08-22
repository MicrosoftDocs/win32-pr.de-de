---
description: Die Delete WMI-Klassenmethode löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist.
ms.assetid: 5663b8a8-3089-475b-8a36-454a7315bfca
ms.tgt_platform: multiple
title: Delete-Methode der Win32_Directory Klasse
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
ms.openlocfilehash: 2966751c822213025d7107e4eff055900e6c8102711b66329e6f3c4fcbe1ed02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676696"
---
# <a name="delete-method-of-the-win32_directory-class"></a>Delete-Methode der Win32 \_ Directory-Klasse

Die **Delete** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich gelöscht wurde, und eine beliebige andere Zahl, um einen Fehler anzugeben.

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

Es ist ein nicht angegebener Fehler aufgetreten.

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

Es ist ein Freigabeverstoß vor worden.

</dd> <dt>

**16**
</dt> <dd>

Die angegebene Startdatei war ungültig.

</dd> <dt>

**17**
</dt> <dd>

Für den Vorgang ist keine Berechtigung erforderlich.

</dd> <dt>

**21**
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ordner sind nicht unbedingt dauerhafte Ergänzungen zu einem Dateisystem. Zu einem bestimmten Zeitpunkt müssen Ordner möglicherweise gelöscht werden, z. B. weil sie nicht mehr benötigt werden, weil sich die Rolle des Computers geändert hat oder weil die Ordner aus Versehen erstellt wurden.

Mit delete können Sie Ordner löschen: Sie binden einfach an den in Frage gestellten Ordner und rufen dann die Delete-Methode auf. Nachdem die Delete-Methode aufgerufen wurde, wird der Ordner dauerhaft aus dem Dateisystem entfernt. es wird nicht an die Papierkorb. Darüber hinaus wird kein Bestätigungshinweis ("Möchten Sie diesen Ordner wirklich löschen?") ausgegeben. Stattdessen wird der Ordner sofort entfernt.

Sie können schreibgeschützte Ordner nicht mit fileSystemObject löschen. Dies kann jedoch mithilfe von WMI erfolgen. Wenn Ihr Skript WMI verwendet und Sie keinen schreibgeschützten Ordner entfernen möchten, müssen Sie die Eigenschaft Lesbar verwenden, um den Ordnerstatus zu überprüfen, bevor Sie ihn löschen.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird der Ordner C: \\ Skripts gelöscht.


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32-Verzeichnis \_**](win32-directory.md)
</dt> </dl>

 


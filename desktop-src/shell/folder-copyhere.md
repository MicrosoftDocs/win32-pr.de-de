---
description: Kopiert ein Element oder Elemente in einen Ordner.
title: Folder.CopyHere-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.CopyHere
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 22bf1b4c-f242-4c52-b094-c5339bb35d02
ms.openlocfilehash: 1466e5d01715c0c820cbc7cd9809c51e4963ec56
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842141"
---
# <a name="foldercopyhere-method"></a>Folder.CopyHere-Methode

Kopiert ein Element oder Elemente in einen Ordner.

## <a name="syntax"></a>Syntax


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vItem* 
</dt> <dd>

Typ: **Variant**

Das zu kopierende Element oder die zu kopierende Elemente. Dies kann eine Zeichenfolge sein, die einen Dateinamen, ein [**FolderItem-Objekt**](folderitem.md) oder ein [**FolderItems-Objekt**](folderitems.md) darstellt.

</dd> <dt>

*vOptions* \[ Optional\]
</dt> <dd>

Typ: **Variant**

Optionen für den Kopiervorgang. Dieser Wert kann 0 (null) oder eine Kombination der folgenden Werte sein. Diese Werte basieren auf Flags, die für die Verwendung mit dem **fFlags-Member** der [**C++-SHFILEOPSTRUCT-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) definiert sind. Jeder Shellnamespace muss eine eigene Implementierung dieser Flags bereitstellen, und jeder Namespace kann einige oder sogar alle dieser Flags ignorieren. Diese Flags werden nicht anhand des Namens für Visual Basic, VBScript oder JScript definiert. Daher müssen Sie sie selbst definieren oder ihre numerischen Entsprechungen verwenden.

> [!Note]  
> In einigen Fällen, z. B. komprimierten Dateien (ZIP-Dateien), werden einige Optionsflags möglicherweise entwurfsweise ignoriert.

 

<dt>



 (4)


</dt> <dd>

Zeigen Sie kein Statusdialogfeld an.

</dd> <dt>



 (8)


</dt> <dd>

Geben Sie der Datei, die mit einem neuen Namen betrieben wird, einen Verschiebungs-, Kopier- oder Umbenennungsvorgang, wenn bereits eine Datei mit dem Zielnamen vorhanden ist.

</dd> <dt>



 (16)


</dt> <dd>

Antworten Sie für alle angezeigten Dialogfelder mit "Ja zu allen".

</dd> <dt>



 (64)


</dt> <dd>

Behalten Sie nach Möglichkeit rückgängige Informationen bei.

</dd> <dt>



 (128)


</dt> <dd>

Führen Sie den Vorgang für Dateien nur aus, wenn ein Platzhalterdateiname ( \* . \* ) angegeben ist.

</dd> <dt>



 (256)


</dt> <dd>

Zeigt ein Statusdialogfeld an, zeigt jedoch nicht die Dateinamen an.

</dd> <dt>



 (512)


</dt> <dd>

Bestätigen Sie die Erstellung eines neuen Verzeichnisses nicht, wenn für den Vorgang ein Verzeichnis erstellt werden muss.

</dd> <dt>



 (1024)


</dt> <dd>

Zeigen Sie keine Benutzeroberfläche an, wenn ein Fehler auftritt.

</dd> <dt>



 (2048)


</dt> <dd>

[Version 4.71.](versions.md) Kopieren Sie nicht die Sicherheitsattribute der Datei.

</dd> <dt>



 (4096)


</dt> <dd>

Wird nur im lokalen Verzeichnis verwendet. Arbeiten Sie nicht rekursiv in Unterverzeichnisse.

</dd> <dt>



 (8192)


</dt> <dd>

[Version 5.0.](versions.md) Kopieren Sie verbundene Dateien nicht als Gruppe. Kopieren Sie nur die angegebenen Dateien.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das aufrufende Programm erhält keine Benachrichtigung, um anzugeben, dass die Kopie abgeschlossen wurde.

> [!Note]  
> Nicht alle Methoden werden für alle Ordner implementiert. Beispielsweise wird die [**ParseName-Methode**](folder-parsename.md) nicht für den ordner Systemsteuerung (CSIDL \_ CONTROLS) implementiert. Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800A01BD (Dezimalzahl 445) ausgelöst.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **CopyHere** verwendet, um die Autoexec.bat-Datei aus dem Stammverzeichnis in das Verzeichnis C: Windows zu \\ kopieren. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

Jscript:


```JScript
<script language="JScript">
    function fnCopyHereJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.CopyHere("C:\\AUTOEXEC.BAT");
        }
    }
 </script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnCopyHereVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")
 
        if not objFolder is nothing then
            objFolder.CopyHere("C:\AUTOEXEC.BAT")
        end if
 
        set objShell = nothing
        set objFolder = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnCopyHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
 
    If (Not objFolder Is Nothing) Then
        objFolder.CopyHere ("C:\AUTOEXEC.BAT")
    End If
 
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ordner**](folder.md)
</dt> </dl>

 

 





---
description: Kopiert ein Element oder Elemente in einen Ordner.
title: Folder. copyhere-Methode (Shldisp. h)
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
ms.openlocfilehash: ac616aa88cfb0ad6742c6037ec28e8b93ff1a4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994735"
---
# <a name="foldercopyhere-method"></a>Folder. copyhere-Methode

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

*vitem* 
</dt> <dd>

Typ: **Variant**

Das Element, das kopiert werden soll. Dabei kann es sich um eine Zeichenfolge handeln, die einen Dateinamen, ein [**folderItem**](folderitem.md) -Objekt oder ein [**folderitems**](folderitems.md) -Objekt darstellt.

</dd> <dt>

*voptions* \[ optionale\]
</dt> <dd>

Typ: **Variant**

Optionen für den Kopiervorgang. Dieser Wert kann 0 (null) oder eine Kombination der folgenden Werte sein. Diese Werte basieren auf Flags, die für die Verwendung mit dem **fFlags** -Member der C++ [**shfleopstruct**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) -Struktur definiert sind. Jeder Shell-Namespace muss eine eigene Implementierung dieser Flags bereitstellen, und jeder Namespace kann einige oder sogar alle dieser Flags ignorieren. Diese Flags werden nicht durch den Namen für Visual Basic, VBScript oder JScript definiert, sodass Sie Sie selbst definieren oder ihre numerischen Entsprechungen verwenden müssen.

> [!Note]  
> In einigen Fällen, z. b. komprimierte Dateien (ZIP-Dateien), werden einige Optionsflags möglicherweise vom Design ignoriert.

 

<dt>



 (4)


</dt> <dd>

Zeigt kein Status Dialogfeld an.

</dd> <dt>



 (8)


</dt> <dd>

Übergeben Sie die Datei mit einem neuen Namen in einem Verschiebungs-, Kopier-oder Umbenennungs Vorgang, wenn bereits eine Datei mit dem Zielnamen vorhanden ist.

</dd> <dt>



 (16)


</dt> <dd>

Antworten Sie für jedes Dialogfeld, das angezeigt wird, mit "Ja, alle".

</dd> <dt>



 (64)


</dt> <dd>

Behalten Sie die rückgängig-Informationen bei, sofern möglich.

</dd> <dt>



 (128)


</dt> <dd>

Der Vorgang wird nur für Dateien durchgeführt, wenn ein Platzhalter Dateiname ( \* . \* ) angegeben wird.

</dd> <dt>



 (256)


</dt> <dd>

Zeigt ein Status Dialogfeld an, aber die Dateinamen werden nicht angezeigt.

</dd> <dt>



 (512)


</dt> <dd>

Bestätigen Sie die Erstellung eines neuen Verzeichnisses nicht, wenn der Vorgang zum Erstellen eines neuen Verzeichnisses erforderlich ist.

</dd> <dt>



 (1024)


</dt> <dd>

Wenn ein Fehler auftritt, wird keine Benutzeroberfläche angezeigt.

</dd> <dt>



 (2048)


</dt> <dd>

[Version 4,71.](versions.md) Kopieren Sie die Sicherheits Attribute der Datei nicht.

</dd> <dt>



 (4096)


</dt> <dd>

Nur im lokalen Verzeichnis ausführen. Arbeiten Sie nicht rekursiv in Unterverzeichnissen.

</dd> <dt>



 (8192)


</dt> <dd>

[Version 5,0.](versions.md) Kopieren Sie keine verbundenen Dateien als Gruppe. Kopiert nur die angegebenen Dateien.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dem aufrufenden Programm wird keine Benachrichtigung erteilt, um anzugeben, dass der Kopiervorgang abgeschlossen wurde.

> [!Note]  
> Nicht alle Methoden werden für alle Ordner implementiert. Beispielsweise ist die Methode " [**Parser Name**](folder-parsename.md) " nicht für den System Steuerungs Ordner (CSIDL-Steuer \_ Elemente) implementiert. Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800a01bd (Decimal 445)-Fehler ausgelöst.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **copyhere** zum Kopieren der Autoexec.bat Datei aus dem Stammverzeichnis in das Verzeichnis "C: Windows" verwendet \\ . Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript


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



VBScript


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Ordner**](folder.md)
</dt> </dl>

 

 





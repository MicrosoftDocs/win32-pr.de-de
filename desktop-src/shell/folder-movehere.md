---
description: Verschiebt ein Element oder Elemente in diesen Ordner.
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: Folder.MoveHere-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.MoveHere
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: eb826d23a168d81d838341e96fa5e613f8b6f5261a3cda548a2be320acebbde8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458918"
---
# <a name="foldermovehere-method"></a>Folder.MoveHere-Methode

Verschiebt ein Element oder Elemente in diesen Ordner.

## <a name="syntax"></a>Syntax


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vItem* \[ In\]
</dt> <dd>

Typ: **Variant**

Das element oder die Elemente, die bzw. die sie verschieben. Dies kann eine Zeichenfolge sein, die einen Dateinamen, ein [**FolderItem-Objekt**](folderitem.md) oder ein [**FolderItems-Objekt**](folderitems.md) darstellt.

</dd> <dt>

*vOptions* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Optionen für den Move-Vorgang. Dieser Wert kann 0 (null) oder eine Kombination der folgenden Werte sein. Diese Werte basieren auf Flags, die für die Verwendung mit dem **fFlags-Member** der C++-SHFILEOPSTRUCT-Struktur [**definiert**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) sind. Diese Flags sind nicht als solche für Visual Basic, VBScript oder JScript definiert, daher müssen Sie sie selbst definieren oder ihre numerischen Entsprechungen verwenden.

<dt>



 (4)


</dt> <dd>

Zeigt kein Statusdialogfeld an.

</dd> <dt>



 (8)


</dt> <dd>

Geben Sie der Datei, die in einem Verschieben, Kopieren oder Umbenennen verwendet wird, einen neuen Namen, wenn bereits eine Datei mit dem Zielnamen vorhanden ist.

</dd> <dt>



 (16)


</dt> <dd>

Antworten Sie mit "Ja zu allen" für jedes dialogfeld, das angezeigt wird.

</dd> <dt>



 (64)


</dt> <dd>

Behalten Sie nach Möglichkeit rückgängig gemachte Informationen bei.

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

Wird nur im lokalen Verzeichnis betrieben. Arbeiten Sie nicht rekursiv in Unterverzeichnisse.

</dd> <dt>



 (9182)


</dt> <dd>

[Version 5.0.](versions.md) Verschieben Sie verbundene Dateien nicht als Gruppe. Verschieben Sie nur die angegebenen Dateien.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Nicht alle Methoden werden für alle Ordner implementiert. Beispielsweise ist die [**ParseName-Methode**](folder-parsename.md) nicht für den ordner Systemsteuerung (CSIDL \_ CONTROLS) implementiert. Wenn Sie versuchen, eine nichtimplementierte Methode auf 0x800A01BD fehler (dezimal 445) wird ausgelöst.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **MoveHere** verwendet, um die Datei Temp.txt aus dem Stammverzeichnis des Laufwerks C in den Ordner C: Windows \\ zu verschieben. Die richtige Verwendung wird für JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    var FOF_NOCONFIRMATION = 16;

    function fnFolderObjectMoveHereJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.MoveHere ("C:\\temp.txt", FOF_NOCONFIRMATION);
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    private const FOF_NOCONFIRMATION = 16
    
    function fnFolderObjectMoveHereVB()
        dim objShell
        dim objFolder

        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            objFolder.MoveHere "C:\temp.txt", FOF_NOCONFIRMATION
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Const FOF_NOCONFIRMATION = &H10

Private Sub btnMoveHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        objFolder.MoveHere "c:\temp.txt", FOF_NOCONFIRMATION
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



 

 





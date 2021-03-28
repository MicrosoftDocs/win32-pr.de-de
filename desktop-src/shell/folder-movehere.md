---
description: Verschiebt ein Element oder Elemente in diesen Ordner.
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: Folder. muvehere-Methode (Shldisp. h)
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
ms.openlocfilehash: da6590d63f4a3c79252e25f3625c0ee75b146b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749177"
---
# <a name="foldermovehere-method"></a>Folder. muvehere-Methode

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

*vitem* \[ in\]
</dt> <dd>

Typ: **Variant**

Das Element oder die Elemente, die verschoben werden sollen. Dabei kann es sich um eine Zeichenfolge handeln, die einen Dateinamen, ein [**folderItem**](folderitem.md) -Objekt oder ein [**folderitems**](folderitems.md) -Objekt darstellt.

</dd> <dt>

*voptions* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Optionen für den Verschiebungs Vorgang. Dieser Wert kann 0 (null) oder eine Kombination der folgenden Werte sein. Diese Werte basieren auf Flags, die für die Verwendung mit dem **fFlags** -Member der C++ [**shfleopstruct**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) -Struktur definiert sind. Diese Flags sind nicht für Visual Basic, VBScript oder JScript definiert, sodass Sie Sie selbst definieren oder deren numerische Entsprechungen verwenden müssen.

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



 (9182)


</dt> <dd>

[Version 5,0.](versions.md) Verschieben Sie verbundene Dateien nicht als Gruppe. Verschieben Sie nur die angegebenen Dateien.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Nicht alle Methoden werden für alle Ordner implementiert. Beispielsweise ist die Methode " [**Parser Name**](folder-parsename.md) " nicht für den System Steuerungs Ordner (CSIDL-Steuer \_ Elemente) implementiert. Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800a01bd (Decimal 445)-Fehler ausgelöst.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **movehere** verwendet, um die Datei Temp.txt aus dem Stammverzeichnis des Laufwerks c in den Ordner c: Windows zu verschieben \\ . Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript


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



VBScript


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 





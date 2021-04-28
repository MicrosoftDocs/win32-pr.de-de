---
description: 'IShellDispatch2.ShellExecute-Methode: Führt einen angegebenen Vorgang für eine angegebene Datei aus.'
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
title: IShellDispatch2.ShellExecute-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5c058275948d5d96805ae24a76389321d7c69b8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117018"
---
# <a name="ishelldispatch2shellexecute-method"></a>IShellDispatch2.ShellExecute-Methode

Führt einen angegebenen Vorgang für eine angegebene Datei aus.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = IShellDispatch2.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
)
```


```VB

IShellDispatch2.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*sFile* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge,** die den Namen der Datei enthält, für die **ShellExecute** die durch vOperation angegebene *Aktion ausführen soll.*

</dd> <dt>

*vArguments* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Eine Zeichenfolge, die Parameterwerte für den Vorgang enthält.

</dd> <dt>

*vDirectory* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Der vollqualifizierte Pfad des Verzeichnisses, das die durch sFile angegebene *Datei enthält.* Wenn dieser Parameter nicht angegeben wird, wird das aktuelle Arbeitsverzeichnis verwendet.

</dd> <dt>

*vOperation* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Der Vorgang, der ausgeführt werden soll. Dieser Wert wird auf eine der Verbzeichenfolgen festgelegt, die von der Datei unterstützt werden. Eine Beschreibung der Verben finden Sie im Abschnitt "Hinweise". Wenn dieser Parameter nicht angegeben wird, wird der Standardvorgang ausgeführt.

</dd> <dt>

*vShow* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Eine Empfehlung, wie das Anwendungsfenster anfänglich angezeigt werden soll. Die Anwendung kann diese Empfehlung ignorieren. Dieser Parameter kann einen der folgenden Werte annehmen. Wenn dieser Parameter nicht angegeben ist, verwendet die Anwendung ihren Standardwert.



| Wert                                                                                                                               | Bedeutung                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>0 (0)</dt> </dl>  | Öffnen Sie die Anwendung mit einem ausgeblendeten Fenster.<br/>                                                                                                    |
| <dl> <dt></dt> <dt>1</dt> </dl>  | Öffnen Sie die Anwendung in einem normalen Fenster. Wenn das Fenster minimiert oder maximiert ist, stellt das System es auf seine ursprüngliche Größe und Position wieder her.<br/> |
| <dl> <dt></dt> <dt>2</dt> </dl>  | Öffnen Sie die Anwendung mit einem minimierten Fenster.<br/>                                                                                                 |
| <dl> <dt></dt> <dt>3</dt> </dl>  | Öffnen Sie die Anwendung mit einem maximierten Fenster.<br/>                                                                                                 |
| <dl> <dt></dt><dt>4</dt> </dl>  | Öffnen Sie die Anwendung mit ihrem Fenster mit der neuesten Größe und Position. Das aktive Fenster bleibt aktiv.<br/>                                  |
| <dl> <dt></dt><dt>5</dt> </dl>  | Öffnen Sie die Anwendung mit ihrem Fenster in ihrer aktuellen Größe und Position.<br/>                                                                        |
| <dl> <dt></dt><dt>7</dt> </dl>  | Öffnen Sie die Anwendung mit einem minimierten Fenster. Das aktive Fenster bleibt aktiv.<br/>                                                               |
| <dl> <dt></dt><dt>10</dt> </dl> | Öffnen Sie die Anwendung mit ihrem Fenster in dem von der Anwendung angegebenen Standardzustand.<br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell.ShellExecute-Methode**](./shell-shellexecute.md) aufgerufen.

Diese Methode entspricht dem Starten eines der Befehle, die dem Kontextmenü einer Datei zugeordnet sind. Jeder Befehl wird durch eine Verbzeichenfolge dargestellt. Die Gruppe der unterstützten Verben variiert von Datei zu Datei. Das am häufigsten unterstützte Verb ist "open", was in der Regel auch das Standardverb ist. Andere Verben werden möglicherweise nur von bestimmten Dateitypen unterstützt. Weitere Informationen zu Shellverben finden Sie unter [Starten von Anwendungen](launch.md) oder Erweitern von [Kontextmenüs.](context.md)

Diese Methode ist derzeit in Microsoft Visual Basic.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **ShellExecute zum** Öffnen des Editors gezeigt. Die Verwendung wird für JScript und VBScript angezeigt.

Jscript:


```JScript
<script language="JScript">
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellExecuteVB()
        dim objShell

        set objShell = CreateObject("shell.application")

        objShell.ShellExecute "notepad.exe", "", "", "open", 1

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 

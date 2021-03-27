---
description: Führt einen angegebenen Vorgang für eine angegebene Datei aus.
ms.assetid: 62E59A1C-51BD-4864-AF09-35FFD49FAB9D
title: Shell.ShellExecute-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 83ab9741199bff675245f15dc2ad1ffb20592a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979888"
---
# <a name="shellshellexecute-method"></a>Shell. ShellExecute-Methode

Führt einen angegebenen Vorgang für eine angegebene Datei aus.

## <a name="syntax"></a>Syntax

JScript

```js
iRetVal = Shell.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
);
```

VBScript

```vb
iRetVal = Shell.ShellExecute( _
  sFile, _
  [ ByVal vArguments ], _
  [ ByVal vDirectory ], _
  [ ByVal vOperation ], _
  [ ByVal vShow ] _
)
```

VB:

```vb
Shell.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*sFile* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge** , die den Namen der Datei enthält, in der **ShellExecute** die durch *voperation* angegebene Aktion ausführt.

</dd> <dt>

*varguments* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Eine Zeichenfolge, die Parameterwerte für den Vorgang enthält.

</dd> <dt>

*vdirectory* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Der voll qualifizierte Pfad des Verzeichnisses, das die von *sFile* angegebene Datei enthält. Wenn dieser Parameter nicht angegeben wird, wird das aktuelle Arbeitsverzeichnis verwendet.

</dd> <dt>

*voperation* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Der Vorgang, der ausgeführt werden soll. Dieser Wert wird auf eine der Verb Zeichenfolgen festgelegt, die von der Datei unterstützt werden. Eine Erläuterung der Verben finden Sie im Abschnitt "Hinweise". Wenn dieser Parameter nicht angegeben wird, wird der Standard Vorgang ausgeführt.

</dd> <dt>

*vshow* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Eine Empfehlung, wie das Anwendungsfenster anfänglich angezeigt werden soll. Diese Empfehlung kann von der Anwendung ignoriert werden. Dieser Parameter kann einen der folgenden Werte annehmen. Wenn dieser Parameter nicht angegeben wird, verwendet die Anwendung den Standardwert.



| Wert                                                                                                                               | Bedeutung                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>0</dt> </dl>  | Öffnen Sie die Anwendung mit einem ausgeblendeten Fenster.<br/>                                                                                                    |
| <dl> <dt></dt> <dt>1</dt> </dl>  | Öffnen Sie die Anwendung mit einem normalen Fenster. Wenn das Fenster minimiert oder maximiert ist, stellt das System die ursprüngliche Größe und Position wieder her.<br/> |
| <dl> <dt></dt> <dt>2</dt> </dl>  | Öffnen Sie die Anwendung mit einem minimierten Fenster.<br/>                                                                                                 |
| <dl> <dt></dt> <dt>3</dt> </dl>  | Öffnen Sie die Anwendung mit einem maximierten Fenster.<br/>                                                                                                 |
| <dl> <dt></dt> <dt>4</dt> </dl>  | Öffnen Sie die Anwendung mit Ihrem Fenster an der aktuellen Größe und Position. Das aktive Fenster bleibt aktiv.<br/>                                  |
| <dl> <dt></dt><dt>5</dt> </dl>  | Öffnen Sie die Anwendung mit Ihrem Fenster an der aktuellen Größe und Position.<br/>                                                                        |
| <dl> <dt></dt><dt>7</dt> </dl>  | Öffnen Sie die Anwendung mit einem minimierten Fenster. Das aktive Fenster bleibt aktiv.<br/>                                                               |
| <dl> <dt></dt><dt>10</dt> </dl> | Öffnen Sie die Anwendung mit Ihrem Fenster im Standardzustand, der von der Anwendung angegeben wird.<br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Methode entspricht dem Starten eines der Befehle, die dem Kontextmenü einer Datei zugeordnet sind. Jeder Befehl wird durch eine Verb Zeichenfolge dargestellt. Der Satz unterstützter Verben variiert von Datei zu Datei. Das am häufigsten unterstützte Verb ist "Open", das in der Regel auch das Standard Verb ist. Andere Verben können von nur bestimmten Dateitypen unterstützt werden. Weitere Informationen zu Shellverben finden Sie unter [Starten von Anwendungen](launch.md) oder Erweitern von Kontext [Menüs](context.md).

Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **ShellExecute** zum Öffnen von Notepad veranschaulicht. Die Verwendung wird für JScript und VBScript angezeigt.

JScript


```JScript
function ShellExecuteJS()
{
    var objShell = new ActiveXObject("Shell.Application");
    objShell.ShellExecute("notepad.exe", "", "", "open", 1);
}
```

VBScript

```vb
Function ShellExecuteVB()
    Dim objShell
    Set objShell = CreateObject("Shell.Application")
    Call objShell.ShellExecute("notepad.exe", "", "", "open", 1)
End Function
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



 

 

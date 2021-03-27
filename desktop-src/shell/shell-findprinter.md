---
description: Zeigt das Dialogfeld Drucker suchen an.
ms.assetid: 61C700CF-623B-4c99-A211-AC26A1E4AE85
title: Shell. findprinter-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1286bb7247359ea91d29a53f8f0eaa13b55be5e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980633"
---
# <a name="shellfindprinter-method"></a>Shell. findprinter-Methode

Zeigt das Dialogfeld **Drucker suchen** an.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = Shell.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

Shell.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*sname* \[ in, optional\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge** , die den Drucker Namen enthält.

</dd> <dt>

*slotung* \[ in, optional\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge** , die den Drucker Speicherort enthält.

</dd> <dt>

*smodel* \[ in, optional\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge** , die das Drucker Modell enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie einem oder mehreren optionalen Parametern Zeichen folgen zuweisen, werden diese als Standardwerte im zugeordneten Bearbeitungs Steuerelement angezeigt, wenn das Dialogfeld " **Drucker suchen** " angezeigt wird. Der Benutzer kann diese Werte entweder annehmen oder außer Kraft setzen. Wenn einem Parameter kein Wert zugewiesen wird, ist das zugehörige Bearbeitungsfeld leer, und der Benutzer muss einen Wert eingeben.

Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird gezeigt, wie **findprinter** verwendet wird, um das Dialogfeld **Drucker** suchen für eine bestimmte Anwendung anzuzeigen. Die Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



 

 

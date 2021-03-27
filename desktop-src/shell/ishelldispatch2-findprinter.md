---
description: Zeigt das Dialogfeld Drucker suchen an.
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: IShellDispatch2. findprinter-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 81124e3f0d04244b9b81e812e090bde25971c17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214872"
---
# <a name="ishelldispatch2findprinter-method"></a>IShellDispatch2. findprinter-Methode

Zeigt das Dialogfeld **Drucker suchen** an.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = IShellDispatch2.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

IShellDispatch2.FindPrinter( _
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

Diese Methode wird implementiert, und der Zugriff erfolgt über die [**Shell. findprinter**](./shell-findprinter.md) -Methode.

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



 

 

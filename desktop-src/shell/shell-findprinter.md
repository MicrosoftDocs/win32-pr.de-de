---
description: 'Shell.FindPrinter-Methode: Zeigt das Dialogfeld Drucker suchen an.'
ms.assetid: 61C700CF-623B-4c99-A211-AC26A1E4AE85
title: Shell.FindPrinter-Methode (Shldisp.h)
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
ms.openlocfilehash: 17d04b60de2b52ca3d2f17fbdccf7de93ac095b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104308"
---
# <a name="shellfindprinter-method"></a>Shell.FindPrinter-Methode

Zeigt das **Dialogfeld Drucker suchen** an.

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

*sName* \[ in, optional\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge,** die den Druckernamen enthält.

</dd> <dt>

*sLocation* \[ in, optional\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge,** die den Druckerspeicherort enthält.

</dd> <dt>

*sModel* \[ in, optional\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge,** die das Druckermodell enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie einem oder mehrere der optionalen Parameter Zeichenfolgen zuweisen, werden sie  als Standardwerte im zugeordneten Bearbeitungssteuerfeld angezeigt, wenn das Dialogfeld Drucker suchen angezeigt wird. Der Benutzer kann diese Werte entweder akzeptieren oder überschreiben. Wenn einem Parameter kein Wert zugewiesen wird, ist das zugeordnete Bearbeitungsfeld leer, und der Benutzer muss einen Wert eingeben.

Diese Methode ist derzeit in Microsoft Visual Basic.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung **von FindPrinter** zum Anzeigen **des** Dialogfelds Drucker suchen für eine bestimmte Anwendung gezeigt. Die Verwendung wird für JScript, VBScript und Visual Basic.

Jscript:


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



Vbscript:


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



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 

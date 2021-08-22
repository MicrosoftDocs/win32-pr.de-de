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
ms.openlocfilehash: 3c3208d001f501371245e578ca691267604be691076f858b0a9f8bb7eeb36279
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111150"
---
# <a name="shellfindprinter-method"></a>Shell.FindPrinter-Methode

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

## <a name="remarks"></a>Hinweise

Wenn Sie einem oder mehreren optionalen Parametern Zeichenfolgen zuweisen, werden diese im zugeordneten Bearbeitungssteuerelement als Standardwerte angezeigt, wenn das Dialogfeld **Drucker suchen** angezeigt wird. Der Benutzer kann diese Werte entweder akzeptieren oder überschreiben. Wenn einem Parameter kein Wert zugewiesen wird, ist das zugeordnete Bearbeitungsfeld leer, und der Benutzer muss einen Wert eingeben.

Diese Methode ist derzeit in Microsoft Visual Basic nicht verfügbar.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **FindPrinter** zum Anzeigen des Dialogfelds **Drucker suchen** für eine bestimmte Anwendung gezeigt. Die Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript:


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



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 

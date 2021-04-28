---
description: 'IShellDispatch2.FindPrinter-Methode: Zeigt das Dialogfeld Drucker suchen an.'
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: IShellDispatch2.FindPrinter-Methode (Shldisp.h)
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
ms.openlocfilehash: 64a3975039255de76b3e59432b0848cc2cb1795b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117118"
---
# <a name="ishelldispatch2findprinter-method"></a>IShellDispatch2.FindPrinter-Methode

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

Diese Methode wird implementiert und über die [**Shell.FindPrinter-Methode**](./shell-findprinter.md) aufgerufen.

Wenn Sie einem oder mehreren optionalen Parametern Zeichenfolgen zuweisen, werden diese im zugeordneten Bearbeitungssteuerelement als Standardwerte angezeigt, wenn das Dialogfeld **Drucker suchen** angezeigt wird. Der Benutzer kann diese Werte entweder akzeptieren oder überschreiben. Wenn einem Parameter kein Wert zugewiesen ist, ist das zugeordnete Bearbeitungsfeld leer, und der Benutzer muss einen Wert eingeben.

Diese Methode ist derzeit in Microsoft Visual Basic nicht verfügbar.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **FindPrinter** zum Anzeigen des Dialogfelds **Drucker suchen** für eine bestimmte Anwendung gezeigt. Die Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 

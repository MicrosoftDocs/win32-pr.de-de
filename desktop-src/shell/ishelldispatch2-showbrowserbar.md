---
description: Zeigt eine Browserleiste an.
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: IShellDispatch2. showbrowserbar-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e1df729401dd12b8221ba98a3b81ea65569113e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978016"
---
# <a name="ishelldispatch2showbrowserbar-method"></a>IShellDispatch2. showbrowserbar-Methode

Zeigt eine Browserleiste an.

## <a name="syntax"></a>Syntax


```JScript
retVal = IShellDispatch2.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

IShellDispatch2.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*sclsid* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichen** Folge, die die Zeichen folgen Form der CLSID der anzuzeigenden Browserleiste enthält. Das Objekt muss als Explorer-Balken Objekt mit der Kategorie "CATID \_ Infoband-Komponente" registriert werden. Weitere Informationen finden Sie unter [Creating Custom Explorer Bars, Toolbands und Desk Bands](band-objects.md).

</dd> <dt>

*vshow* \[ in\]
</dt> <dd>

Typ: **Variant**

Legen Sie diese Einstellung auf " **true** " fest **, um die** Browserleiste anzuzeigen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **Variant \** _

Gibt _ *true** zurück, wenn erfolgreich; andernfalls **false**.

### <a name="vb"></a>VB

Typ: **Variant \** _

Gibt _ *true** zurück, wenn erfolgreich; andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell. showbrowserbar**](./shell-showbrowserbar.md) -Methode aufgerufen.

Sie können eine der Standard-Explorer-leisten anzeigen, indem Sie den *sclsid* -Parameter auf die CLSID dieser Explorer-Leiste festlegen. Die Standard-Explorer-leisten und Ihre CLSID-Zeichen folgen lauten wie folgt:



| Explorer-Leiste | CLSID-Zeichenfolge                           |
|--------------|----------------------------------------|
| Favoriten    | {EFA24E61-B078-11d0-89E4-00C04FC9E26E} |
| Ordner      | {EFA24E64-B078-11d0-89E4-00C04FC9E26E} |
| Verlauf      | {EFA24E62-B078-11d0-89E4-00C04FC9E26E} |
| Suchen,       | {30d02401-6a81-11D0-8274-00c04\d5ae38} |



 

Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird gezeigt, wie Sie **showbrowserbar** verwenden, um die **Favoriten** -Browserleiste anzuzeigen. Die Verwendung wird für JScript und VBScript angezeigt.

JScript


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

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



 

 

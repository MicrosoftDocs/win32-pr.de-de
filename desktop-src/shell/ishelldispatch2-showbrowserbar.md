---
description: 'IShellDispatch2.ShowBrowserBar-Methode: Zeigt eine Browserleiste an.'
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: IShellDispatch2.ShowBrowserBar-Methode (Shldisp.h)
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
ms.openlocfilehash: 7143b55ae59c8fca845d256ddc1f79e69672364b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116938"
---
# <a name="ishelldispatch2showbrowserbar-method"></a>IShellDispatch2.ShowBrowserBar-Methode

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

*sCLSID* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge,** die die Zeichenfolgenform der CLSID der anzuzeigenden Browserleiste enthält. Das Objekt muss als Explorer-Balkenobjekt mit einer CATID \_ InfoBand-Komponentenkategorie registriert werden. Weitere Informationen finden Sie unter [Erstellen von benutzerdefinierten Explorer-Balken, Toolbändern und Desk-Bändern.](band-objects.md)

</dd> <dt>

*vShow* \[ In\]
</dt> <dd>

Typ: **Variant**

Legen Sie diese Einstellung auf **TRUE** fest, um die Browserleiste anzuzeigen, oder **auf FALSE,** um sie auszublenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **\* Variant**

Gibt **true** zurück, wenn erfolgreich. andernfalls **FALSE.**

### <a name="vb"></a>VB

Typ: **\* Variant**

Gibt **true** zurück, wenn erfolgreich. andernfalls **FALSE.**

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell.ShowBrowserBar-Methode**](./shell-showbrowserbar.md) aufgerufen.

Sie können eine der Standard-Explorer-Balken anzeigen, indem Sie den *sCLSID-Parameter* auf die CLSID dieser Explorer-Leiste festlegen. Die standardmäßigen Explorer-Balken und ihre CLSID-Zeichenfolgen sind wie folgt:



| Explorer-Leiste | CLSID-Zeichenfolge                           |
|--------------|----------------------------------------|
| Favoriten    | {EFA24E61-B078-11d0-89E4-00C04FC9E26E} |
| Ordner      | {EFA24E64-B078-11d0-89E4-00C04FC9E26E} |
| Verlauf      | {EFA24E62-B078-11d0-89E4-00C04FC9E26E} |
| Suche       | {30D02401-6A81-11d0-8274-00C04FD5AE38} |



 

Diese Methode ist derzeit in Microsoft Visual Basic nicht verfügbar.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **ShowBrowserBar** zum Anzeigen der **Browserleiste Favoriten** gezeigt. Die Verwendung wird für JScript und VBScript angezeigt.

Jscript:


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



Vbscript:


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



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 

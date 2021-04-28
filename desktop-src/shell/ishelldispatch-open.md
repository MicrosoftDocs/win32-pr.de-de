---
description: 'IShellDispatch.Open-Methode: Öffnet den angegebenen Ordner.'
ms.assetid: 30FE669A-4AFD-4dfa-9F62-E62E744469C7
title: IShellDispatch.Open-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4b5301e030926b9bcfdc18949b6a04706c22bb71
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086628"
---
# <a name="ishelldispatchopen-method"></a>IShellDispatch.Open-Methode

Öffnet den angegebenen Ordner.

## <a name="syntax"></a>Syntax


```JScript
IShellDispatch.Open(
  vDir
)
```


```VB

IShellDispatch.Open( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*vDir* \[ In\]
</dt> <dd>

Typ: **Variant**

Eine Zeichenfolge, die den Pfad des Ordners oder eines der [**ShellSpecialFolderConstants-Werte angibt.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) Beachten Sie, dass die konstanten Namen in **ShellSpecialFolderConstants** in Visual Basic, aber nicht in VBScript oder JScript verfügbar sind. In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.

Wenn *vDir* auf einen der [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) festgelegt ist und der spezielle Ordner nicht vorhanden ist, erstellt diese Funktion den Ordner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell.Open-Methode aufgerufen.**](shell-open.md)

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **Open** in JScript, VBScript und Visual Basic.

Jscript:


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objshell.Open(ssfWINDOWS);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Open("C:\")

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Open (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**Erkunden**](shell-explore.md)
</dt> </dl>

 

 





---
description: Fügt der Liste der Kanäle im Windows Internet Explorer Favoritenmenü und der Kanalleiste auf dem Desktop einen neuen Kanal hinzu.
title: ShellUIHelper.AddChannel-Methode (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddChannel
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b62e6e82-429a-4d41-96d4-cba639b611f5
ms.openlocfilehash: d08c1360cb2a96fbc7b87daecb650bbf46aa6ad9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841201"
---
# <a name="shelluihelperaddchannel-method"></a>ShellUIHelper.AddChannel-Methode

Fügt der Liste der Kanäle im Menü Windows Internet Explorer **Favoriten**  und der Kanalleiste auf dem Desktop einen neuen Kanal hinzu.

> [!Note]  
> Diese Methode wird unter Windows Vista nicht mehr unterstützt. Unter diesem Betriebssystem wird E \_ NOTIMPL zurückgegeben.

 

## <a name="syntax"></a>Syntax


```JScript
iRetVal = ShellUIHelper.AddChannel(
  sURL
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sURL* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Ein **Zeichenfolgenwert,** der die URL der CDF-Datei angibt.

> [!Note]  
> Die Links in der CDF-Datei müssen http-, HTTPS- oder FTP-Protokolle verwenden. Wenn die CDF-Datei ein anderes Protokoll enthält, schlägt das Hinzufügen des Kanals fehl, und es wird kein Dialogfeld angezeigt.

 

</dd> </dl>

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die ordnungsgemäße Verwendung dieser Methode für JScript veranschaulicht, das in HTML und Visual Basic.

Jscript:


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddChannelJ()
    {
        ShellUIHelper.AddChannel("https://www.microsoft.com/windows/cdf/g_stock.cdf");
    }
</script>

</head>
<body onload=fnShellUIHelperAddChannelJ()>
</body>
</html>
```



Visual Basic:


```VB
Private Sub fnShellUIHelperAddChannelVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddChannel ("https://www.microsoft.com/windows/cdf/g_stock.cdf")
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 

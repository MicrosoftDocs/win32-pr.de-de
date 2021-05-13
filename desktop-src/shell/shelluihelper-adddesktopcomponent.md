---
description: Fügt dem Microsoft-Konto ein Element Active Desktop.
title: ShellUIHelper.AddDesktopComponent-Methode (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddDesktopComponent
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 41634a89-15b9-41c8-ba3f-4bf19b786f6f
ms.openlocfilehash: 2edaa79bd62dcee40e4f197700d2128cb0b2070d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842461"
---
# <a name="shelluihelperadddesktopcomponent-method"></a>ShellUIHelper.AddDesktopComponent-Methode

Fügt dem Microsoft-Konto ein Element Active Desktop.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = ShellUIHelper.AddDesktopComponent(
  sURL,
  sType,
  [ Left ],
  [ Top ],
  [ Width ],
  [ Height ]
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sURL* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Ein **Zeichenfolgenwert,** der die URL des neuen Favoritenelements angibt.

</dd> <dt>

*sType* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Ein **Zeichenfolgenwert,** der den Typ des hinzugefügten Elements angibt. Dies kann einer der folgenden Werte sein.

<dt>



 (Bild)


</dt> <dd>

Die Komponente ist ein Bild.

</dd> <dt>



 (Website)


</dt> <dd>

Die Komponente ist eine Website.

</dd> </dl> </dd> <dt>

*Links* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die Position des linken Rands der Komponente in Bildschirmkoordinaten.

</dd> <dt>

*Oben* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die Position des oberen Rands der Komponente in Bildschirmkoordinaten.

</dd> <dt>

*Breite* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die Breite der Komponente in Bildschirmeinheiten.

</dd> <dt>

*Höhe* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die Höhe der Komponente in Bildschirmeinheiten.

</dd> </dl>

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript, das in HTML und Visual Basic eingebettet ist.

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
    function fnShellUIHelperAddDesktopComponentJ()
    {
        ShellUIHelper.AddDesktopComponent("https://www.microsoft.com/", "website");
    }
</script>

</head>
<body onload=fnShellUIHelperAddDesktopComponentJ()>
</body>
</html>
```



Visual Basic:


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 

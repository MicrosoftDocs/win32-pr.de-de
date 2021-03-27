---
description: Fügt dem Microsoft Active Desktop ein Element hinzu.
title: Shelluihelper. adddesktopcomponent-Methode (Exdisp. h)
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
ms.openlocfilehash: d5234a0b43ea25c8ac931dc14ec90f7a6696ddfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980592"
---
# <a name="shelluihelperadddesktopcomponent-method"></a>Shelluihelper. adddesktopcomponent-Methode

Fügt dem Microsoft Active Desktop ein Element hinzu.

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

*sUrl* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Ein **Zeichen** folgen Wert, der die URL des neuen bevorzugten Elements angibt.

</dd> <dt>

*sType* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Ein **Zeichen** folgen Wert, der den Typ des hinzugefügten Elements angibt. Dies kann einer der folgenden Werte sein:

<dt>



 Klang


</dt> <dd>

Die Komponente ist ein Bild.

</dd> <dt>



 Website


</dt> <dd>

Die Komponente ist eine Website.

</dd> </dl> </dd> <dt>

*Links* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die Position des linken Rands der Komponente in Bildschirm Koordinaten.

</dd> <dt>

Nach *oben* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die Position des oberen Rands der Komponente in Bildschirm Koordinaten.

</dd> <dt>

*Breite* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die Breite der Komponente in Bildschirm Einheiten.

</dd> <dt>

*Höhe* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die Höhe der Komponente in Bildschirm Einheiten.

</dd> </dl>

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript Embedded in HTML und Visual Basic.

JScript


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 

---
title: THEME.openDialog
description: Die openDialog-Methode öffnet ein Dateidialogfeld.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- THEME.openDialog-Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d57218105aa081ddebcb98fadbdb40b4bbd42511de9df94e204320ce78cf03c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134553"
---
# <a name="themeopendialog"></a>THEME.openDialog

Die **openDialog-Methode** öffnet ein Dateidialogfeld.

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*
</dt> <dd>

Eine **Zeichenfolge,** die den Typ des Dialogfelds angibt. Muss auf "FILE OPEN" festgelegt \_ werden.

</dd> <dt>

<span id="parameters"></span><span id="PARAMETERS"></span>*Parameter*
</dt> <dd>

Eine **Zeichenfolge,** die für zusätzliche Informationen verwendet werden kann. Muss auf "FILES \_ ALLMEDIA" festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück, die die URL der ausgewählten Datei enthält, oder "" (leere Zeichenfolge), wenn der Benutzer auf Abbrechen klickt.

## <a name="remarks"></a>Hinweise

Diese Methode kann für Dateien auf den lokalen Festplatten oder auf Netzwerklaufwerken verwendet werden.

## <a name="examples"></a>Beispiele


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**THEME-Element**](theme-element.md)
</dt> </dl>

 

 






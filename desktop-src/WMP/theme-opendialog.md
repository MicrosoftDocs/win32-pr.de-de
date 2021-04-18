---
title: Design. OpenDialog
description: Die OpenDialog-Methode öffnet ein Datei Dialogfeld.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- Design. OpenDialog-Fenster Media Player
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79b9478b6b970b1d8d18b6f40975479e4755fa6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355055"
---
# <a name="themeopendialog"></a>Design. OpenDialog

Die **OpenDialog** -Methode öffnet ein Datei Dialogfeld.

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*DialogType*
</dt> <dd>

Eine **Zeichenfolge** , die den Typ des Dialog Felds angibt. Muss auf "Datei öffnen" festgelegt werden \_ .

</dd> <dt>

<span id="parameters"></span><span id="PARAMETERS"></span>*Metern*
</dt> <dd>

Eine **Zeichenfolge** , die für weitere Informationen verwendet werden kann. Muss auf "Files \_ AllMedia" festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** mit der URL der ausgewählten Datei oder "" (leere Zeichenfolge) zurück, wenn der Benutzer auf Abbrechen klickt.

## <a name="remarks"></a>Bemerkungen

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
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Design-Element**](theme-element.md)
</dt> </dl>

 

 






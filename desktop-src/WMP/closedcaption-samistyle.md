---
title: Closedcaption. samistyle
description: Die samistyle-Eigenschaft gibt den Beschriftungs Stil an oder ruft ihn ab.
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- Fenster "closedcaption. samistyle" Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyle
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe81c2c2c4f4504d6167abe538c52ab769550a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359309"
---
# <a name="closedcaptionsamistyle"></a>Closedcaption. samistyle

Die **samistyle** -Eigenschaft gibt den Beschriftungs Stil an oder ruft ihn ab.

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Eine Sami-Datei kann mehrere Format Definitionen enthalten. Sami-Stile werden zwischen den Tags und in der Sami <STYLE> - </STYLE> Datei definiert. Ein Stil wird mit einer Text Zeichenfolge mit vorangestelltem \# Zeichen definiert. Beispiel:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



Gibt einen Stil an, der eine bestimmte Schriftart erzeugt.

Wenn kein Sami-Format angegeben ist, wird standardmäßig das erste Format verwendet, das in der Sami-Datei definiert ist.

**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird ein HTML-SELECT-Element erstellt, das *closedcaption* verwendet. **Samistyle** , um die Darstellung des geschlossenen Beschriftungs Texts zu ändern. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCMode  NAME = "CCMode"  LANGUAGE = "JScript"

       /* Change the text style when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMIStyle = CCMode.value;
        ">

       /* Fill the SELECT list with options, set the default to Strong. */
        <OPTION VALUE = "Normal">Normal
        <OPTION VALUE = "Small">Small 
        <OPTION VALUE = "Big Bold Italic" SELECTED>Strong
</SELECT>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Closedcaption-Objekt**](closedcaption-object.md)
</dt> </dl>

 

 






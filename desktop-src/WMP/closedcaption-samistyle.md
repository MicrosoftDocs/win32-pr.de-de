---
title: ClosedCaption.SAMIStyle
description: Die SAMIStyle-Eigenschaft gibt den Untertitelstil an oder ruft diese ab.
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- ClosedCaption.SAMIStyle Windows Media Player
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
ms.openlocfilehash: 6bd45977e3d433239e74aee21def913b640fad12
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882178"
---
# <a name="closedcaptionsamistyle"></a>ClosedCaption.SAMIStyle

Die **SAMIStyle-Eigenschaft** gibt den Untertitelstil an oder ruft diese ab.

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**

## <a name="remarks"></a>Hinweise

Eine SAMI-Datei kann mehrere Formatformatdefinitionen enthalten. SAMI-Stile werden zwischen &lt; style und tags in der &gt; </STYLE> SAMI-Datei definiert. Ein Stil wird mit einer Textzeichenfolge definiert, der ein Zeichen \# voran steht. Beispiel:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



Dies gibt einen Stil an, der eine bestimmte Schriftart erzeugt.

Wenn kein SAMI-Stil angegeben ist, wird standardmäßig der erste in der SAMI-Datei definierte Stil verwendet.

**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.

## <a name="examples"></a>Beispiele

Im folgenden JScript wird ein HTML SELECT-Element erstellt, das *closedCaption verwendet.* **SAMIStyle,** um die Darstellung des Untertiteltexts zu ändern. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption-Objekt**](closedcaption-object.md)
</dt> </dl>

 

 






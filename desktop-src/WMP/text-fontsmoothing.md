---
title: Text. fontermoothing
description: Mit dem Attribut "FontSmoothing" wird ein Wert angegeben oder abgerufen, der angibt, ob die Schriftart Glättung aktiviert ist.
ms.assetid: bd6f0468-285e-44b3-a5e8-361744c5ce4a
keywords:
- Text. FON-moothing-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.fontSmoothing
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcdf285572b4edda0f514cb3519b6953f9e94677
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373623"
---
# <a name="textfontsmoothing"></a>Text. fontermoothing

Mit dem Attribut " **FontSmoothing** " wird ein Wert angegeben oder abgerufen, der angibt, ob die Schriftart Glättung aktiviert ist.

``` syntax
        elementID.fontSmoothing
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                          |
|-------|--------------------------------------|
| true  | Die Schriftart Glättung ist aktiviert.           |
| false | Standard. Die Schriftart Glättung ist deaktiviert. |



 

## <a name="remarks"></a>Bemerkungen

Die Schriftart Glättung verwendet das Antialiasing-Feature des Betriebssystems. Wenn die Schriftart Glättung aktiviert ist und das Betriebssystem Antialiasing unterstützt, versucht Windows Media Player, den Text zu glätten. Nicht alle Schriftarten unterstützen Antialiasing. Windows Media Player 10 verwendet die Windows XP ClearType Anti-Aliasing-Methode.

-   **Warnung** Die Schriftart Glättung über eine transparente Farbe kann bewirken, dass die transparente Farbe in die Zeichen hinein mischt. Es wird nicht empfohlen, dass Sie " **fonensmoothing** " verwenden, wenn der Text über eine Transparenz angezeigt wird.

Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Text-Element**](text-element.md)
</dt> </dl>

 

 






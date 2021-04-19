---
title: Text. WordWrap
description: Mit dem WordWrap-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob der Zeilenumbruch aktiviert oder deaktiviert ist.
ms.assetid: 3bb127d8-42f1-4167-986a-d41690cb5647
keywords:
- Text. WordWrap-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2b4d030a7e9efdda1bc7503ae3bf8eb5985401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372688"
---
# <a name="textwordwrap"></a>Text. WordWrap

Mit dem **WordWrap** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob der Zeilenumbruch aktiviert oder deaktiviert ist.

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | Der Zeilenumbruch ist aktiviert.                                                                             |
| false | Standard. Der Zeilenumbruch ist deaktiviert. Wenn der Text nicht in das Steuerelement passt, wird der Text abgeschnitten. |



 

## <a name="remarks"></a>Bemerkungen

Das Text Steuerelement teilt Wörter nicht voneinander ab. Wenn ein Wort über die Breite des Steuer Elements hinausgeht, wird das Wort Wrap verwendet, um das Wort in die nächste Zeile zu verschieben. Wenn ein einzelnes Wort länger als die Steuerelement Breite ist, wird dieses Wort abgeschnitten und belegt eine einzelne Zeile.

Wenn das **Width** -Attribut nicht angegeben wird, wird **WordWrap** ignoriert, und die Größe des Text Steuer Elements wird geändert, anstatt den Text zu umschließen.

Wenn an bestimmten Orten Zeilenumbrüche gewünscht werden, müssen Sie explizit mit "  &\# 13;" oder "r" in einem Wert angegeben werden \\ . Wenn das letztere Formular verwendet wird, wenn der Wert direkt angegeben wird, muss der Zeichenfolge "JScript:" vorangestellt werden, und der tatsächliche Wert muss in einfache Anführungszeichen eingeschlossen werden, wie unten dargestellt. Dies ist nicht erforderlich, wenn der Wert innerhalb eines Ereignis Handlers dynamisch festgelegt wird.

Wenn **WordWrap** auf true festgelegt ist **und die** QuickInfo nicht angegeben ist, wird in der QuickInfo der vollständige Text des **value** -Attributs angezeigt. Wenn keine QuickInfo erwünscht ist, **legen Sie** die QuickInfo auf "" (leere Zeichenfolge) fest.

## <a name="examples"></a>Beispiele


```C++
<THEME>
  <VIEW>
    <TEXT
      width = "50"
      height = "200"
      wordWrap = "true"
      backgroundColor = "blue"
      foregroundColor = "white"
      value = "This is a test.&#13;&#13;It is only a test."
    />
    <TEXT
      width = "50"
      height = "200"
      left = "100"
      wordWrap = "true"
      backgroundColor = "green"
      foregroundColor = "white"
      value = "JScript:'This is a test.\r\rIt is only a test.'"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambientattribute. Width**](ambientattributes-width.md)
</dt> <dt>

[**Text-Element**](text-element.md)
</dt> <dt>

[**Text. ToolTip**](text-tooltip.md)
</dt> <dt>

[**Text. Value**](text-value.md)
</dt> </dl>

 

 






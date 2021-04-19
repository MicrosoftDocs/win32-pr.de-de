---
title: Text. fontface
description: Das fontface-Attribut gibt die Schriftart für das Text Steuerelement an oder ruft Sie ab.
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- Text. fontface-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183b25547e456cb90cac4d2137354679e13d8a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369119"
---
# <a name="textfontface"></a>Text. fontface

Das **fontface** -Attribut gibt die Schriftart für das Text Steuerelement an oder ruft Sie ab.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann der Name einer beliebigen gültigen Schriftart sein, die unter Windows verfügbar ist. Das Installieren von Schriftarten wird von Windows Media Player nicht unterstützt. Wählen Sie also eine Schriftart aus, die Sie auf dem vorgesehenen System kennen.

Wenn die angegebene **fontface** nicht auf dem System des Benutzers verfügbar ist, wird das Text Steuerelement standardmäßig auf die Schriftart des Windows-Systems festgelegt.

Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Text-Element**](text-element.md)
</dt> <dt>

[**Text. FontSize**](text-fontsize.md)
</dt> </dl>

 

 






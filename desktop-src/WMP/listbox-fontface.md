---
title: ListBox. fontface
description: Das fontface-Attribut gibt die Schriftart für das Listenfeld-Steuerelement an oder ruft diese ab.
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- ListBox. fontface-Fenster Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c03c367001b307dd8bd5059ec7e3f4a0b364e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373750"
---
# <a name="listboxfontface"></a>ListBox. fontface

Das **fontface** -Attribut gibt die Schriftart für das Listenfeld-Steuerelement an oder ruft diese ab.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann der Name einer beliebigen gültigen Schriftart sein, die in Windows verfügbar ist. Das Installieren von Schriftarten wird von Windows Media Player nicht unterstützt. Wählen Sie also eine Schriftart aus, die Sie auf dem vorgesehenen System kennen.

Wenn die angegebene **fontface** nicht auf dem System des Benutzers verfügbar ist, wird im Listenfeld-Steuerelement standardmäßig die Schriftart des Windows-Systems angezeigt. Der Standardwert für englischsprachige Systeme ist "Tahoma". Bei internationalen Systemen wird der Standardwert aus einer Ressourcen Datei geladen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ListBox-Element**](listbox-element.md)
</dt> <dt>

[**ListBox. FontSize**](listbox-fontsize.md)
</dt> <dt>

[**ListBox. FontStyle**](listbox-fontstyle.md)
</dt> </dl>

 

 






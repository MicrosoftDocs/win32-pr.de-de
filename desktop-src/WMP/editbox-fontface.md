---
title: EditBox. fontface
description: Das fontface-Attribut gibt die Schriftart für Text im Bearbeitungsfeld-Steuerelement an oder ruft diese ab.
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- EditBox. fontface-Fenster Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362064"
---
# <a name="editboxfontface"></a>EditBox. fontface

Das **fontface** -Attribut gibt die Schriftart für Text im Bearbeitungsfeld-Steuerelement an oder ruft diese ab.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann der Name einer beliebigen gültigen Schriftart sein, die in Windows verfügbar ist. Das Installieren von Schriftarten wird von Windows Media Player nicht unterstützt. Wählen Sie also eine Schriftart aus, die Sie auf dem vorgesehenen System kennen.

Wenn die angegebene **fontface** nicht auf dem System des Benutzers verfügbar ist, wird für das Steuerelement "Bearbeitungsfeld" standardmäßig die Schriftart des Windows-Systems verwendet. Der Standardwert für englischsprachige Systeme ist "Tahoma". Bei internationalen Systemen wird der Standardwert aus einer Ressourcen Datei geladen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EditBox-Element**](editbox-element.md)
</dt> <dt>

[**EditBox. FontSize**](editbox-fontsize.md)
</dt> <dt>

[**EditBox. FontStyle**](editbox-fontstyle.md)
</dt> </dl>

 

 






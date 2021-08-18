---
title: EDITBOX.fontFace
description: Das fontFace-Attribut gibt die Schriftart für Text im Bearbeitungsfeld-Steuerelement an oder ruft sie ab.
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- EDITBOX.fontFace-Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3994c9cef1f645dc9c1129876b9144471caf9f608f5911641b180deae437194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996860"
---
# <a name="editboxfontface"></a>EDITBOX.fontFace

Das **fontFace-Attribut** gibt die Schriftart für Text im Bearbeitungsfeld-Steuerelement an oder ruft sie ab.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**

## <a name="remarks"></a>Hinweise

Dieses Attribut kann der Name einer beliebigen gültigen Schriftart sein, die in der Windows. Windows Media Player die Installation von Schriftarten nicht unterstützt, wählen Sie daher eine Schriftart aus, von der Sie wissen, dass sie sich auf dem vorgesehenen System befingt.

Wenn das **angegebene fontFace-Steuerelement** auf dem System des Benutzers nicht verfügbar ist, verwendet das Bearbeitungsfeld-Steuerelement standardmäßig die Windows Systemschriftart. Der Standardwert für englischsprachige Systeme ist "Tahoma". Bei internationalen Systemen wird der Standardwert aus einer Ressourcendatei geladen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EDITBOX-Element**](editbox-element.md)
</dt> <dt>

[**EDITBOX.fontSize**](editbox-fontsize.md)
</dt> <dt>

[**EDITBOX.fontStyle**](editbox-fontstyle.md)
</dt> </dl>

 

 






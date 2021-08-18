---
title: TEXT.fontFace
description: Das fontFace-Attribut gibt die Schriftart für das Text-Steuerelement an oder ruft sie ab.
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- TEXT.fontFace Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b1044d01ac3ca6a8cc4f1212232bfcc630eb73831f90eb7fd5f423f5dc38d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118357"
---
# <a name="textfontface"></a>TEXT.fontFace

Das **fontFace-Attribut** gibt die Schriftart für das Text-Steuerelement an oder ruft sie ab.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff.

## <a name="remarks"></a>Hinweise

Dieses Attribut kann der Name einer beliebigen gültigen Schriftart sein, die auf Windows verfügbar ist. Windows Media Player die Installation von Schriftarten nicht unterstützt, wählen Sie daher eine Schriftart aus, von der Sie wissen, dass sie sich auf dem vorgesehenen System befingt.

Wenn das angegebene **fontFace** auf dem System des Benutzers nicht verfügbar ist, wird für das Text-Steuerelement standardmäßig die Windows Systemschriftart verwendet.

Ein Beispiel, das veranschaulicht, wie die Attribute des **TEXT-Elements** verwendet werden, finden Sie im [Value-Attribut.](text-value.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TEXT-Element**](text-element.md)
</dt> <dt>

[**TEXT.fontSize**](text-fontsize.md)
</dt> </dl>

 

 






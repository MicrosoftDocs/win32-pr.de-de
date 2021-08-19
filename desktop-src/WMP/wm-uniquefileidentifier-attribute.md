---
title: WM/UniqueFileIdentifier-Attribut
description: Das WM/UniqueFileIdentifier-Attribut ist eine Zeichenfolge, die das Element eindeutig identifiziert.
ms.assetid: 8196fc38-05dc-4c9e-98cb-1e160ce28a9a
keywords:
- WM/UniqueFileIdentifier-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- WM/UniqueFileIdentifier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf29b5f4a0c2bf6e2642ce13f190a4734a2fb4ff395481b1ba93bc5feeb6db89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930816"
---
# <a name="wmuniquefileidentifier-attribute"></a>WM/UniqueFileIdentifier-Attribut

Das **WM/UniqueFileIdentifier-Attribut** ist eine Zeichenfolge, die das Element eindeutig identifiziert.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [CD-Wiedergabelisten](cd-playlist-attributes.md)
-   [CD-Spuren](cd-track-attributes.md)
-   [Häufig verwendete Windows Mediendateiattribute](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird sowohl in der Bibliothek (oder im Cache) als auch in der digitalen Mediendatei gespeichert.

**UniqueFileIdentifier** ist ein Alias für dieses Attribut.

Die Windows Media Format SDK-Konstante für dieses Attribut lautet g \_ wszWMUniqueFileIdentifier.

Verwenden Sie die [Media.isReadOnlyItem-Methode,](media-isreadonlyitem.md) um zu bestimmen, ob Sie den Wert dieses Attributs ändern können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> </dl>

 

 






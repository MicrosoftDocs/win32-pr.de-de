---
title: AverageLevel-Attribut
description: Das AverageLevel-Attribut ist ein 16-Bit-Amplitudenwert, der die durchschnittliche Volumeebene angibt.
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- AverageLevel-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e169b1e2d63e6f8215515acc852d431ff13ccd513924e4c2a237b16c17dacfc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582745"
---
# <a name="averagelevel-attribute"></a>AverageLevel-Attribut

Das **AverageLevel-Attribut** ist ein 16-Bit-Amplitudenwert, der die durchschnittliche Volumeebene angibt.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Mediendateien](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.

Windows Media Player legt diesen Wert in einer der folgenden Instanzen fest:

-   Nach dem Löschen einer Datei.
-   Nachdem eine Datei wiedergegeben wurde (wenn die Automatische Volume leveling-Erweiterung aktiviert ist).

Die Windows Media Format SDK-Konstante für dieses Attribut ist g \_ wszAverageLevel.

Verwenden Sie die [Media.isReadOnlyItem-Methode,](media-isreadonlyitem.md) um zu bestimmen, ob Sie den Wert dieses Attributs ändern können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> </dl>

 

 






---
title: WM/Anbieterattribut
description: Das WM/Provider-Attribut ist der Name des Anbieters der Attributwerte.
ms.assetid: 358651d3-5bcd-4a03-a9aa-a33745d0323a
keywords:
- WM-/Anbieterattribut-Windows Media Player
topic_type:
- apiref
api_name:
- WM/Provider
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7fa8312d095151145cfe33a139def23e20082aec2cd1d5f1c3344b9b565dfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735370"
---
# <a name="wmprovider-attribute"></a>WM/Anbieterattribut

Das **WM/Provider-Attribut** ist der Name des Anbieters der Attributwerte.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [CD-Wiedergabelisten](cd-playlist-attributes.md)
-   [CD-Spuren](cd-track-attributes.md)
-   [Häufig verwendete Windows Mediendateiattribute](commonly-used-windows-media-file-attributes.md)
-   [Funkelemente](radio-item-attributes.md)
-   [Videoelemente](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird sowohl in der Bibliothek (oder im Cache) als auch in der digitalen Mediendatei gespeichert.

**MetadataSource** ist ein Alias für dieses Attribut.

Die Windows Media Format SDK-Konstante für dieses Attribut ist g \_ wszWMProvider.

Verwenden Sie die [Media.isReadOnlyItem-Methode,](media-isreadonlyitem.md) um zu bestimmen, ob Sie den Wert dieses Attributs ändern können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher (Das Fotoelement wird nur in Windows Media Player 10 oder höher unterstützt)<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> </dl>

 

 






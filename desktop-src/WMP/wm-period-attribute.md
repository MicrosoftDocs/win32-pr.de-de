---
title: WM/period-Attribut
description: Das WM/period-Attribut ist die Gültigkeitsdauer des Inhalts.
ms.assetid: fb154ef7-c8bc-4468-8f3f-4b716291fd0a
keywords:
- WM/period-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/Period
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895d528780b8dc0f51f9072a0ca0a2cfb7095104
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352882"
---
# <a name="wmperiod-attribute"></a>WM/period-Attribut

Das **WM/period-** Attribut ist die Gültigkeitsdauer des Inhalts.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [CD-Spuren](cd-track-attributes.md)
-   [Häufig verwendete Windows Media-Dateiattribute](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist sowohl in der Bibliothek (oder im Cache) als auch in der digitalen Mediendatei gespeichert.

**Period** ist ein Alias für dieses Attribut.

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmperiod.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 






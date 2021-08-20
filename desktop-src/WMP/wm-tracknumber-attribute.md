---
title: WM/TrackNumber-Attribut
description: Das WM/TrackNumber-Attribut ist die Titelnummer des Elements auf dem Album, auf dem es ursprünglich veröffentlicht wurde.
ms.assetid: d1fc5bac-c440-470f-be5c-5aca74aee99e
keywords:
- WM/TrackNumber-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be4820ee1f8bf582705b00b6fa7d2ba37869d67835e69d5b9fd339c41bc0ce18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930826"
---
# <a name="wmtracknumber-attribute"></a>WM/TrackNumber-Attribut

Das **WM/TrackNumber-Attribut** ist die Titelnummer des Elements auf dem Album, auf dem es ursprünglich veröffentlicht wurde.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Mediendateiattribute](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.

Titelnummern für ein Album beginnen bei 1.

**OriginalIndex** und **OriginalIndexLeft** sind Aliase für dieses Attribut.

Die Windows Media Format SDK-Konstante für dieses Attribut ist g \_ wszWMTrackNumber.

Um zu bestimmen, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media.isReadOnlyItem-Methode.](media-isreadonlyitem.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributreferenz**](attribute-reference.md)
</dt> </dl>

 

 






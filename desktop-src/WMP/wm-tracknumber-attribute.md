---
title: WM/tracknumber-Attribut
description: Das WM/tracknumber-Attribut ist die Nachverfolgung des Elements auf dem Album, auf dem es ursprünglich veröffentlicht wurde.
ms.assetid: d1fc5bac-c440-470f-be5c-5aca74aee99e
keywords:
- WM/tracknumber-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd9adf3a939a5087ee270e8bef4d4d510b678ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373832"
---
# <a name="wmtracknumber-attribute"></a>WM/tracknumber-Attribut

Das **WM/tracknumber-** Attribut ist die Nachverfolgung des Elements auf dem Album, auf dem es ursprünglich veröffentlicht wurde.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Media-Dateiattribute](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.

Nachverfolgen von Zahlen für einen Album Start bei 1.

**Originalindex** und **originalindexleft** sind Aliase für dieses Attribut.

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmtracknumber.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 






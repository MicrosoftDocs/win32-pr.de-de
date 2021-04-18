---
title: Synchronisierungs Attribute
description: Die Attribute Sync01 through Sync16 sind Zeichen folgen Darstellungen von 32-Bit-Werten, die von Windows Media Player beim Synchronisieren von Wiedergabelisten mit einem von bis zu 16 tragbaren Geräten verwendet werden.
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- Synchronisierungs Attribute (Windows Media Player)
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af26ae563a38efcc40b0bcd319c5fc62b4776dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364607"
---
# <a name="sync-attributes"></a>Synchronisierungs Attribute

Die Attribute **Sync01** through **Sync16** sind Zeichen folgen Darstellungen von 32-Bit-Werten, die von Windows Media Player beim Synchronisieren von Wiedergabelisten mit einem von bis zu 16 tragbaren Geräten verwendet werden.

## <a name="applies-to"></a>Gilt für

-   [Wiedergabelisten](playlist-attributes-ref.md)

## <a name="remarks"></a>Bemerkungen

Diese Attribute sind Lese-/Schreibzugriff. Der Wert 0 (null) gibt an, dass Windows Media Player die Wiedergabeliste nicht mit dem zugeordneten Gerät synchronisieren soll. Ein Wert größer als 0 (null) gibt eine Synchronisierungs Priorität für die angegebene Wiedergabeliste an.

Basierend auf der Benutzereingabe legt Windows Media Player dieses Attribut für jede der Wiedergabelisten in der Bibliothek fest. Wenn Windows Media Player versucht, eine Wiedergabeliste mit einem tragbaren Gerät zu synchronisieren, wird jede Wiedergabeliste überprüft, um die Werte für die **Sync**_xx_ -Attribute zu vergleichen, die die Geräte Partnerschaft darstellen. Wiedergabelisten, die niedrigere **Sync**_xx_ -Werte aufweisen, erhalten eine höhere Synchronisierungs Priorität.

Die Bibliothek kann z. b. die folgenden vier Wiedergabelisten und die entsprechenden **Sync**_xx_ -Werte enthalten:



| Wiedergabelisten Name | Sync01-Wert |
|---------------|--------------|
| "Gymmusic. wpl"  | 0x0000000d   |
| "Relax. wpl"     | 0x00000020   |
| Drivehome. wpl | 0x00000001   |
| Nogo. wpl      | 0x00000000   |



 

Wenn Windows Media Player das dem-Attribut zugeordnete Gerät synchronisiert, werden die Wiedergabelisten in der folgenden Reihenfolge synchronisiert:

1.  Drivehome. wpl
2.  "Gymmusic. wpl"
3.  "Relax. wpl"

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> <dt>

[**Auflisten von Synchronisierungs Wiedergabelisten**](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 






---
title: Synchronisierungsattribute
description: Die Attribute Sync01 bis Sync16 sind Zeichenfolgendarstellungen von 32-Bit-Werten, die Windows Media Player beim Synchronisieren von Wiedergabelisten mit einem von bis zu 16 portablen Geräten verwendet.
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- Synchronisierungsattribute Windows Media Player
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e720598b17db6b073524d80afc8f39dd6e6f87e777246b5bdb60294b161fa1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134753"
---
# <a name="sync-attributes"></a>Synchronisierungsattribute

Die Attribute **Sync01** bis **Sync16** sind Zeichenfolgendarstellungen von 32-Bit-Werten, die Windows Media Player beim Synchronisieren von Wiedergabelisten mit einem von bis zu 16 portablen Geräten verwendet.

## <a name="applies-to"></a>Gilt für

-   [Wiedergabelisten](playlist-attributes-ref.md)

## <a name="remarks"></a>Hinweise

Dies sind Lese-/Schreibattribute. Der Wert 0 gibt an, dass Windows Media Player die Wiedergabeliste nicht mit dem zugeordneten Gerät synchronisieren soll. Ein Wert größer als 0 (null) gibt eine Synchronisierungspriorität für die angegebene Wiedergabeliste an.

Basierend auf Benutzereingaben legt Windows Media Player dieses Attribut für jede Wiedergabeliste in der Bibliothek fest. Wenn Windows Media Player versucht, eine Wiedergabeliste mit einem portablen Gerät zu synchronisieren, überprüft sie jede Wiedergabeliste, um die Werte für die **Sync XX-Attribute** zu vergleichen, die die Gerätepartnerschaft darstellen. Wiedergabelisten mit niedrigeren **Sync XX-Werten** erhalten eine höhere Synchronisierungspriorität.

Beispielsweise kann die Bibliothek die folgenden vier Wiedergabelisten und die entsprechenden **Sync**_XX-Werte_ enthalten:



| Wiedergabelistenname | Sync01-Wert |
|---------------|--------------|
| WpL.WpL  | 0x0000000D   |
| Locker.WPL     | 0x00000020   |
| DriveHome.WPL | 0x00000001   |
| NoGo.WPL      | 0x00000000   |



 

Wenn Windows Media Player das dem Attribut zugeordnete Gerät synchronisiert, werden die Wiedergabelisten in der folgenden Reihenfolge synchronisiert:

1.  DriveHome.WPL
2.  WpL.WpL
3.  Locker.WPL

Verwenden Sie die [Media.isReadOnlyItem-Methode,](media-isreadonlyitem.md) um zu bestimmen, ob Sie den Wert dieses Attributs ändern können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> <dt>

[**Auflisten von Synchronisierungswiedergabelisten**](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 






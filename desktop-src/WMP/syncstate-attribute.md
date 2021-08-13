---
title: SyncState-Attribut
description: Das SyncState-Attribut ist eine Zeichenfolgendarstellung eines 32-Bit-Werts, den Windows Media Player verwendet, wenn Wiedergabelisten mit portablen Geräten synchronisiert werden.
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- SyncState-Windows Media Player
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7712a6e3bb0a01f4a713af114f91ebdcb302ef172c77e1cb64b8746f9ae0dcf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414860"
---
# <a name="syncstate-attribute"></a>SyncState-Attribut

Das **SyncState-Attribut** ist eine Zeichenfolgendarstellung eines 32-Bit-Werts, den Windows Media Player verwendet, wenn Wiedergabelisten mit portablen Geräten synchronisiert werden.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Andere Elemente](other-item-attributes.md)
-   [Fotoelemente](photo-item-attributes.md)
-   [Videoelemente](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut besteht aus 16 2-Bit-Werten, von denen jeder den Synchronisierungsstatus eines portablen Geräts angibt. Das wichtigste Bit (MSB) dieses 32-Bit-Werts entspricht Gerät 16. Das am wenigsten signifikante Bit (LSB) entspricht Gerät 1.

Der MSB jedes 2-Bit-Werts gibt an, Windows Media Player Inhalt mit dem entsprechenden Gerät synchronisiert wurde. Der Wert 1 gibt an, dass dies der Fehler war. Der Wert 0 gibt an, dass dies nicht der Fehler war.

Wenn der MSB 0 ist, gibt der LSB an, warum die Synchronisierung fehlgeschlagen ist. Der Wert 1 in der LSB gibt an, dass nicht genügend freier Speicherplatz für den Inhalt vorhanden war. Der Wert 0 in der LSB gibt an, dass eine Synchronisierung aus einem anderen Grund verhindert wurde.

Gehen Sie wie folgt vor, um den Synchronisierungsstatus eines bestimmten Geräts abzurufen:

1.  Rufen **Sie IWMPSyncDevice::get \_ status auf,** um zu bestimmen, ob ein bestimmtes Gerät synchronisiert ist.
2.  Wenn es synchronisiert ist, rufen Sie **IWMPSyncDevice::get \_ partnershipIndex** auf, um den Index des Bitpaars des Geräts im **SyncState-Attribut** abzurufen.
3.  Maskieren Sie mit diesem Index  das entsprechende Bitpaar des SyncState-Attributs, und untersuchen Sie das Ergebnis, um den Synchronisierungsstatus der Wiedergabeliste mit dem Gerät zu bestimmen.

Um zu bestimmen, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media.isReadOnlyItem-Methode.](media-isreadonlyitem.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Attributreferenz**](attribute-reference.md)
</dt> <dt>

[**Bestimmen des Wiedergabelistensynchronisierungsstatus**](determining-playlist-synchronization-state.md)
</dt> <dt>

[**IWMPSyncDevice::get \_ partnershipIndex**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[**IWMPSyncDevice::get \_ status**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 






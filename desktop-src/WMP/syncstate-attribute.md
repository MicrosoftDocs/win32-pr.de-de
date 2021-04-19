---
title: SyncState-Attribut
description: Das SyncState-Attribut ist eine Zeichen folgen Darstellung eines 32-Bit-Werts, der von Windows Media Player beim Synchronisieren von Wiedergabelisten mit tragbaren Geräten verwendet wird.
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- SyncState-Attribut (Windows Media Player)
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a948f6c649d548b375ccb676134177b0273c85c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373650"
---
# <a name="syncstate-attribute"></a>SyncState-Attribut

Das **SyncState** -Attribut ist eine Zeichen folgen Darstellung eines 32-Bit-Werts, der von Windows Media Player beim Synchronisieren von Wiedergabelisten mit tragbaren Geräten verwendet wird.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Andere Elemente](other-item-attributes.md)
-   [Foto Elemente](photo-item-attributes.md)
-   [Video Elemente](video-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut besteht aus 16 2-Bit-Werten, von denen jeder den Synchronisierungs Status eines tragbaren Geräts angibt. Das signifikanteste Bit (MSB) dieses 32-Bit-Werts entspricht Gerät 16. Das unwichtigste Bit (LSB) entspricht Gerät 1.

Der MSB-Wert jedes 2-Bit-Werts gibt an, ob Windows den Inhalt mit dem entsprechenden Gerät synchronisiert Media Player. Der Wert 1 gibt an, dass dies geschehen ist. Der Wert 0 gibt an, dass dies nicht der Fall war.

Wenn MSB den Wert 0 hat, gibt der LSB an, warum die Synchronisierung fehlgeschlagen ist. Der Wert 1 in der LSB gibt an, dass nicht genügend freier Speicherplatz für den Inhalt vorhanden war. Der Wert 0 in der LSB gibt an, dass eine Synchronisierung durch einen anderen Grund verhindert wurde.

Gehen Sie folgendermaßen vor, um den Synchronisierungs Status eines bestimmten Geräts abzurufen:

1.  Rufen Sie **iwmpsyncdevice:: get \_ Status** auf, um zu bestimmen, ob ein bestimmtes Gerät synchronisiert ist.
2.  Wenn Sie synchronisiert ist, rufen Sie **iwmpsyncdevice:: get \_ partnershipindex** auf, um den Index des bitpaars des Geräts im **SyncState** -Attribut abzurufen.
3.  Maskieren Sie mit diesem Index das entsprechende bitpaar des **SyncState** -Attributs, und untersuchen Sie das Ergebnis, um den Synchronisierungs Status der Wiedergabeliste mit dem Gerät zu bestimmen.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> <dt>

[**Status der Wiedergabelisten Synchronisierung**](determining-playlist-synchronization-state.md)
</dt> <dt>

[**Iwmpsyncdevice:: get \_ Partner shipindex**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[**Iwmpsyncdevice:: get- \_ Status**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 






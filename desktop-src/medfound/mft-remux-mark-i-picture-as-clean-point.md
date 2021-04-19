---
description: Gibt an, ob die e. 264-Video-REMUX-MFT I-Bilder als Clean Point markieren soll, um eine bessere Suchfunktion zu erzielen. Dadurch haben Sie die Möglichkeit, für Suchvorgänge in nicht konformen abschließenden MP4-Dateien Beschädigungen zu beschädigen.
ms.assetid: BB521E13-40A4-4643-B071-76B8CBC62074
title: MFT_REMUX_MARK_I_PICTURE_AS_CLEAN_POINT-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c9fe8398507f6d7af5d0e4bf45a36a4454f220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360183"
---
# <a name="mft_remux_mark_i_picture_as_clean_point-attribute"></a>MFT \_ REMUX \_ Mark \_ I \_ Bild \_ als \_ Clean \_ Point-Attribut

Gibt an, ob die e. 264-Video-REMUX-MFT I-Bilder als Clean Point markieren soll, um eine bessere Suchfunktion zu erzielen. Dadurch haben Sie die Möglichkeit, für Suchvorgänge in nicht konformen abschließenden MP4-Dateien Beschädigungen zu beschädigen.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Das saubere Punkt Bild sollte per Definition komprimierte IDR-Bilder sein.

Dies wird nicht empfohlen, um MP4-Dateien aufzuzeichnen oder erneut zu verarbeiten, es sei denn, eine solche Übung besteht darin, einige zwischen Pseudo-MP4-Dateien für die Videobearbeitung zu entwickeln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>"MF Transform. idl"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





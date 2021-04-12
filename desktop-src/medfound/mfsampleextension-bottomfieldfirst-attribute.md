---
description: Gibt die Feld Dominanz für einen verschachtelten Videorahmen an.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: MFSampleExtension_BottomFieldFirst-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e608160c92fa53e8cde6adee1831d6c3e8789bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344868"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a>MF Sample Extension \_ bottomfieldfirst-Attribut

Gibt die Feld Dominanz für einen verschachtelten Videorahmen an. Dieses Attribut gilt für Medien Beispiele.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Bemerkungen

Wenn der Videorahmen Zeilen Sprung enthält und das Beispiel zwei verschachtelte Felder enthält, gibt dieses Attribut an, welches Feld zuerst angezeigt wird. **True** gibt an, dass das untere Feld das erste Mal ist. **False** gibt an, dass das oberste Feld zuerst ist.

Wenn der Frame Zeilen Sprung ist und das Beispiel ein einzelnes Feld enthält, gibt dieses Attribut an, welches Feld das Beispiel enthält. **True** gibt an, dass das Beispiel das untere Feld enthält. Wenn der Wert **false** ist, enthält das Beispiel das oberste Feld.

Wenn der Frame progressiv ist, beschreibt dieses Attribut, wie die Felder angeordnet werden sollen, wenn die Ausgabe mit Zeilen Sprung versehen wird. **True** gibt an, dass das untere Feld zuerst ausgegeben werden soll. Wenn **false**, sollte das oberste Feld zuerst ausgegeben werden.

Wenn dieses Attribut nicht festgelegt wird, beschreibt der Medientyp die Feld Dominanz.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Beispiel Attribute](sample-attributes.md)
</dt> <dt>

[Medien Beispiele](media-samples.md)
</dt> <dt>

[Video-Interlacing](video-interlacing.md)
</dt> </dl>

 

 





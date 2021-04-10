---
description: Gibt an, ob das erste Feld in einem Zeilen Sprung Rahmen wiederholt werden soll. Dieses Attribut gilt für Medien Beispiele.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: MFSampleExtension_RepeatFirstField-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af10157c280a3e48ed8f415529534fc97fd5cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130520"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a>MF Sample Extension \_ repeatfirstfield-Attribut

Gibt an, ob das erste Feld in einem Zeilen Sprung Rahmen wiederholt werden soll. Dieses Attribut gilt für Medien Beispiele.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Bemerkungen

Wenn der Wert **false** ist oder das-Attribut nicht festgelegt ist, wird das erste Feld nicht wiederholt. Wenn der Wert **true** ist, wird das erste Feld wiederholt. Der Wert **true** ist nur gültig, wenn die folgenden Bedingungen zutreffen:

-   Der Medientyp ist gemischt und progressiv. (Das Attribut " [**MF \_ MT \_ Interlace \_ Mode**](mf-mt-interlace-mode-attribute.md) " für den Medientyp ist " **MF videointerlace \_ mixedinterlaceorprogressive**").
-   Der Frame ist progressiv, und das [**\_ interschnür Attribut "mfsampleextension**](mfsampleextension-interlaced-attribute.md) " im Beispiel ist " **true**".
-   Das Attribut " [**MF SampleExtension \_ bottomfieldfirst**](mfsampleextension-bottomfieldfirst-attribute.md) " ist für das Beispiel festgelegt. Der Wert kann " **true** " oder " **false**" sein. Die Reihenfolge der Felder wird durch dieses Attribut bestimmt.

Dieses Attribut wird für 3:2 Pulldown verwendet. In der folgenden Tabelle wird die Reihenfolge angezeigt, in der Felder angezeigt werden.



| MF Sample Extension \_ repeatfirstfield | MF Sample Extension \_ bottomfieldfirst | Feld Reihenfolge         |
|-------------------------------------|-------------------------------------|---------------------|
| **TRUE**                            | **TRUE**                            | Niedriger, oberer, niedriger |
| **TRUE**                            | **FALSE**                           | Upper, Lower, Upper |
| **FALSE**                           | **TRUE**                            | Niedriger, oberer        |
| **FALSE**                           | **FALSE**                           | Obere, untere        |



 

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

 

 





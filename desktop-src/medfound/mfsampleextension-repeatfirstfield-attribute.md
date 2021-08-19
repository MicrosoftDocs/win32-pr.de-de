---
description: Gibt an, ob das erste Feld in einem Verschachtelungsrahmen wiederholt werden soll. Dieses Attribut gilt für Medienbeispiele.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: MFSampleExtension_RepeatFirstField -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0668e37e6a6958615c83f98c4b6b87eb170b115cf0549f3944a43b21c5b65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872420"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a>MFSampleExtension \_ RepeatFirstField-Attribut

Gibt an, ob das erste Feld in einem Verschachtelungsrahmen wiederholt werden soll. Dieses Attribut gilt für Medienbeispiele.

## <a name="data-type"></a>Datentyp

**BOOL als** **UINT32 gespeichert**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**VERERBUNGSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Hinweise

Wenn der Wert **FALSE ist oder** das Attribut nicht festgelegt ist, wird das erste Feld nicht wiederholt. Wenn der Wert **TRUE ist,** wird das erste Feld wiederholt. Der Wert **TRUE** ist nur gültig, wenn die folgenden Bedingungen erfüllt sind:

-   Der Medientyp ist gemischt und progressiv. (Das [**MF \_ MT \_ INTERLACE MODE-Attributattribut \_**](mf-mt-interlace-mode-attribute.md) für den Medientyp ist **MFVideoInterlace \_ MixedInterlaceOrProgressive**.)
-   Der Frame ist progressiv, und das [**MFSampleExtension \_ Interlaced-Attribut**](mfsampleextension-interlaced-attribute.md) im Beispiel ist **TRUE.**
-   Das [**\_ BottomFieldFirst-Attribut MFSampleExtension**](mfsampleextension-bottomfieldfirst-attribute.md) wird im Beispiel festgelegt. Der Wert kann **TRUE oder** **FALSE sein.** Die Reihenfolge der Felder wird durch dieses Attribut bestimmt.

Dieses Attribut wird für den 3:2-Pulldown verwendet. Die folgende Tabelle zeigt die Reihenfolge, in der Felder angezeigt werden.



| MFSampleExtension \_ RepeatFirstField | MFSampleExtension \_ BottomFieldFirst | Feld reihenfolge         |
|-------------------------------------|-------------------------------------|---------------------|
| **TRUE**                            | **TRUE**                            | Lower, upper, lower |
| **TRUE**                            | **FALSE**                           | Upper, lower, upper |
| **FALSE**                           | **TRUE**                            | Lower, upper        |
| **FALSE**                           | **FALSE**                           | Upper, lower        |



 

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Beispielattribute](sample-attributes.md)
</dt> <dt>

[Medienbeispiele](media-samples.md)
</dt> <dt>

[Video Interlacing](video-interlacing.md)
</dt> </dl>

 

 





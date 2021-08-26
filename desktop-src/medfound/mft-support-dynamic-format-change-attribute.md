---
description: Gibt an, ob eine Media Foundation Transform (MFT) dynamische Formatänderungen unterstützt.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d9bfd2185006975cf128cc60f2b774eba6ba74229b3e290c743c4cde3930
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012610"
---
# <a name="mft_support_dynamic_format_change-attribute"></a>MFT \_ SUPPORT DYNAMIC FORMAT \_ \_ \_ CHANGE-Attribut

Gibt an, ob eine Media Foundation Transform (MFT) dynamische Formatänderungen unterstützt.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Dieses Attribut kann die folgenden Werte haben.



| Wert     | BESCHREIBUNG                                                            |
|-----------|------------------------------------------------------------------------|
| **TRUE**  | Der Client kann das Eingabeformat während des Streamings ändern.               |
| **FALSE** | Der MFT muss entleert werden, bevor der Client das Eingabeformat ändern kann. |



 

Um dieses Attribut zu erhalten, rufen Sie [**zuerst DIETRANSFORM::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) auf, um den globalen Attributspeicher für MFT zu erhalten. Rufen Sie [**dann DIE ATTRIBUTEs::GetUINT32 auf,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) um den Attributwert zu erhalten.

Wenn [**GetAttributes fehlschlägt**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) oder das Attribut nicht vorhanden ist, ist der Standardwert **FALSE.**

[Asynchrone MFTs](asynchronous-mfts.md) müssen den Wert **TRUE zurückgeben.**

Weitere Informationen finden Sie unter [Behandeln von Streamänderungen.](handling-stream-changes.md)

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

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**VORRÜBERSETZUNGTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 





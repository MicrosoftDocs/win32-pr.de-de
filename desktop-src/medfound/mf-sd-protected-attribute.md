---
description: Gibt an, ob ein Stream geschützten Inhalt enthält.
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: MF_SD_PROTECTED-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ae6cf92b3ada6309de7e92a722db38c88ce94a8af88aa6cc0176f738ff194b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474050"
---
# <a name="mf_sd_protected-attribute"></a>MF \_ SD \_ PROTECTED-Attribut

Gibt an, ob ein Stream geschützten Inhalt enthält.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Streamdeskriptoren. Wenn der Wert des Attributs **TRUE** ist, enthält der Stream geschützten Inhalt. Wenn der Wert **FALSE** ist oder das Attribut nicht festgelegt ist, enthält der Stream klaren Inhalt.

Anstatt jeden Stream für dieses Attribut zu überprüfen, können Sie einen Präsentationsdeskriptor an die [**MFRequireProtectedEnvironment-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) übergeben. Diese Funktion testet, ob der Präsentationsdeskriptor geschützte Streams enthält.

Eine Medienquelle sollte dieses Attribut im Streamdeskriptor festlegen, wenn der Inhalt den geschützten Medienpfad (Protected Media Path, PMP) erfordert.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="examples"></a>Beispiele


```
// This function returns TRUE if the stream contains protected 
// content. You can also call the MFRequireProtectedEnvironment 
// function to test whether a presentation contains any streams
// with protected content.

BOOL StreamHasProtectedContent(IMFStreamDescriptor *pSD)
{
    return MFGetAttributeUINT32(pSD, MF_SD_PROTECTED, FALSE);
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**ÜBERSCHREIBENStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Streamdeskriptorattribute](stream-descriptor-attributes.md)
</dt> </dl>

 

 





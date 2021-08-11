---
description: Enthält den Klassenbezeichner (CLSID) einer Media Foundation Transformierung (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: MFT_TRANSFORM_CLSID_Attribute -Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0122b783d8b321aa2a5c7788a589e19625b6a2bde8e37b0b659b0a1192f8c7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240198"
---
# <a name="mft_transform_clsid_attribute-attribute"></a>MFT \_ TRANSFORM \_ CLSID-Attributattribut \_

Enthält den Klassenbezeichner (CLSID) einer Media Foundation Transformierung (MFT).

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetGUID auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetGUID auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird für die VON der [**MFTEnumEx-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) zurückgegebenen [**ATTRIBUTEActivate-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) festgelegt.

Dieses Attribut wird intern vom Aktivierungsobjekt verwendet, wenn es den MFT erstellt. Anwendungen sollten diese CLSID nicht direkt zum Erstellen des MFT verwenden, da das Aktivierungsobjekt möglicherweise die MFT initialisieren muss. Um eine Instanz von MFT zu erstellen, rufen Sie daher FÜR das Aktivierungsobjekt [**DIEACTIVate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) auf.

Beachten Sie, [**dass sich die MFTEnumEx-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) in dieser Hinsicht anders verhält als die [**MFTEnum-Funktion.**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) Die **MFTEnum-Funktion** gibt CLSIDs zurück, die die Anwendung an die **CoCreateInstance-Funktion übergibt.** Die **MFTEnumEx-Funktion** gibt Aktivierungsobjekte anstelle von CLSIDs zurück.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 





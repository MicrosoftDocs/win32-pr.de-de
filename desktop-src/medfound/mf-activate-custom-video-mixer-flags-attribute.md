---
description: Gibt an, wie ein benutzerdefinierter Mixer für den erweiterten Videorenderer (EVR) erstellt wird.
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd536328bf454a70b35376aca3b7c6a0cea9ec7e0e2408a05cd6d0e8da0854ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957090"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a>MF \_ ACTIVATE CUSTOM VIDEO MIXER \_ \_ \_ \_ FLAGS-Attribut

Gibt an, wie ein benutzerdefinierter Mixer für den erweiterten Videorenderer (EVR) erstellt wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Sie können dieses Attribut für den [**POINTERActivate-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) festlegen, der von der [**MFCreateVideoRendererActivate-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) abgerufen wurde. Der Wert dieses Attributs ist ein bitweises **OR** der folgenden Werte.



| Wert                                      | Beschreibung                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ ACTIVATE \_ CUSTOM \_ MIXER \_ ALLOWFAIL** | Wenn die [**MIXERActivate::ActivateObject-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) den benutzerdefinierten Mixer der Anwendung nicht erstellen kann, wird stattdessen der EVR-Standardmixer verwendet. Wenn beim Erstellen des benutzerdefinierten Mixers ein Fehler beim [**OBJECTACTIVATE-Objekt**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) auftritt, schlägt die **ActivateObject-Methode** standardmäßig fehl. |



 

Anwendungen können das [**\_ \_ \_ \_ \_ CLSID-Attribut MF ACTIVATE CUSTOM VIDEO MIXER**](mf-activate-custom-video-mixer-clsid-attribute.md) verwenden, um einen benutzerdefinierten Mixer für die EVR anzugeben.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Erweiterte Videorendererattribute](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Aktivierungsobjekte](activation-objects.md)
</dt> </dl>

 

 





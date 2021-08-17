---
description: Enthält Flags zum Konfigurieren des Audiorenderers.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1146ce4e363dca63819badd96abcd9d9e91051419df3b5007c237a002bb39d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105006"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a>\_ \_ FLAGS-Attribut des MF-AUDIORENDERERATTRIBUTS \_ \_

Enthält Flags zum Konfigurieren des Audiorenderers.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein bitweises **OR** der folgenden Flags.



| Wert                                                   | Beschreibung                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ MF-AUDIORENDERERATTRIBUTFLAGS \_ \_ \_ PROZESSÜBERGREIFEND** | Der Audiorenderer verwendet eine prozessübergreifende Audiositzung. Mit diesem Flag können Audiorenderer in mehreren Prozessen die gleiche Audiositzung gemeinsam mit dem zugeordneten Volume und den Richtliniensteuerelementen verwenden.<br/> Wenn dieses Flag nicht festgelegt ist, kann die Audiositzung nicht von Audiorenderern in anderen Prozessen freigegeben werden.<br/> |
| **\_ \_ MF-AUDIORENDERERATTRIBUT \_ \_ KENNZEICHNET \_ NOPERSIST**    | Die Windows-Audiositzungs-API (WASAPI) wird die Eigenschaften für diese Audiositzung, z. B. das Sitzungsvolumen, nicht beibehalten.<br/> Wenn dieses Flag nicht festgelegt ist, werden die Audiositzungseigenschaften von WASAPI beibehalten.<br/>                                                                                                       |



 

Sie können dieses Attribut verwenden, um den Audiorenderer zu konfigurieren. Die Verwendung hängt davon ab, welche Funktion Sie aufrufen, um den Audiorenderer zu erstellen:

-   [**MFCreateAudioRenderer:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)Legen Sie dieses Attribut mithilfe des IM *pAudioAttributes-Parameters angegebenen INTERFACEAttributes-Schnittstellenzeigers* fest. [](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**MFCreateAudioRendererActivate: Legen**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)Sie dieses Attribut mithilfe des [**IMTActivate-Schnittstellenzeigers**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) fest, der im *ppActivate-Parameter abgerufen* wurde. Legen Sie das -Attribut fest, bevor [**SIE DENKActivate::ActivateObject aufrufen.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attribute des Audiorenderers](audio-renderer-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Streamingaudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 





---
description: Gibt die Audiorichtlinienklasse für den Audiorenderer an.
ms.assetid: 80b028f5-7756-4bb8-b5e3-ebc8343e168c
title: MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5830a3deeb32ca6a3f766bad1858a803948b7e2c07a36f1f1e3222d00ba6199a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104996"
---
# <a name="mf_audio_renderer_attribute_session_id-attribute"></a>\_ \_ SITZUNGS-ID-Attribut des \_ MF-AUDIORENDERERS \_ \_

Gibt die Audiorichtlinienklasse für den Audiorenderer an.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Hinweise

Dieses Attribut ordnet den Audiorenderer einer Audiorichtlinienklasse zu. Jede Richtlinienklasse verfügt über ein eigenes Volume und eine eigene Richtliniensteuerung. Wenn dieses Attribut nicht festgelegt ist, wird die neue SAR der Standardaudiositzung der Anwendung beitreten. Weitere Informationen finden Sie unter [**IAudioClient::Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) in der Core-Audio-API-Dokumentation.

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

[**ATTRIBUTEs::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**ATTRIBUTEs::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Streamingaudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 

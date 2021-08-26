---
description: Gibt den Bezeichner für das Audioendpunktgerät an.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1dd99a42442342e25c748e12f8af84a03f2322b8c3dd24bb915b50b57952d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941130"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a>MF \_ AUDIO \_ RENDERER ATTRIBUTE ENDPOINT \_ \_ \_ ID-Attribut

Gibt den Bezeichner für das Audioendpunktgerät an.

## <a name="data-type"></a>Datentyp

Breitzeichenfolge

## <a name="remarks"></a>Hinweise

Sie können dieses Attribut verwenden, um den Audiorenderer zu konfigurieren. Die Verwendung hängt davon ab, welche Funktion Sie aufrufen, um den Audiorenderer zu erstellen:

-   [**MFCreateAudioRenderer:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)Legen Sie dieses Attribut mithilfe des IM *pAudioAttributes-Parameter* [**angegebenen SCHNITTSTELLENzeigers "POINTERAttributes"**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) fest.
-   [**MFCreateAudioRendererActivate:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)Legen Sie dieses Attribut mithilfe des IM *ppActivate-Parameter* abgerufenen SCHNITTSTELLENzeigers [**VONACTIVATE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) fest. Legen Sie das -Attribut fest, bevor Sie [**DIE AKTIONACTIVATE::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)aufrufen.

Ein Audioendpunktgerät ist ein Hardwaregerät, das sich an einem Ende eines Audiodatenpfads befindet, z. B. einem Lautsprecher oder einem Lautsprecher. Verwenden Sie die folgenden Kernaudio-APIs, um die Audioendpunkt-ID abzurufen:

-   Verwenden Sie die [**IMMDeviceEnumerator-Schnittstelle,**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) um die Geräte auf dem System aufzulisten.
-   Rufen Sie [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) auf, um den Bezeichner für das Gerät abzurufen.

Weitere Informationen finden Sie in der Dokumentation zur [Core Audio-API.](../coreaudio/core-audio-apis-in-windows-vista.md) Wenn dieses Attribut nicht festgelegt ist, verwendet der Audiorenderer das Standardendpunktgerät.

Wenn dieses Attribut festgelegt ist, legen Sie das [**MF \_ AUDIO \_ RENDERER ATTRIBUTE ENDPOINT \_ \_ \_ ROLE-Attribut**](mf-audio-renderer-attribute-endpoint-role-attribute.md) nicht fest. Wenn beide Attribute festgelegt sind, tritt beim Erstellen des Audiorenderers ein Fehler auf.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audiorendererattribute](audio-renderer-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**ATTRIBUTEAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[StreamingAudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 

---
description: Gibt den Bezeichner für das audioendpunkt-Gerät an.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042f59baf4812c177358acca6badb2422914afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344598"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a>\_ \_ \_ \_ Attribut Endpunkt- \_ ID für MF-audiorenderer

Gibt den Bezeichner für das audioendpunkt-Gerät an.

## <a name="data-type"></a>Datentyp

Breitzeichenfolge

## <a name="remarks"></a>Bemerkungen

Sie können dieses Attribut verwenden, um den audiorenderer zu konfigurieren. Die Verwendung hängt von der Funktion ab, die Sie zum Erstellen des audiorenderers aufzurufen:

-   [**MF | ateaudiorenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Legen Sie dieses Attribut mit dem im *paudioattribute* -Parameter angegebenen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstellen Zeiger fest.
-   [**Mfkreateaudiorendereraktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Legen Sie dieses Attribut mit dem [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstellen Zeiger fest, der im *ppaktivierungs* -Parameter abgerufen wurde. Legen Sie das-Attribut vor dem Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)fest.

Bei einem audioendpunktgerät handelt es sich um ein Hardware Gerät, das sich an einem Ende eines audiodatenpfads befindet, z. b. ein Telefon oder ein Redner. Verwenden Sie zum Abrufen des audioendpunktbezeichners die folgenden kernaudioapis:

-   Verwenden Sie die [**immdeviceenumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle, um die Geräte auf dem System aufzuzählen.
-   Bitten Sie [**immdevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) , um den Bezeichner für das Gerät abzurufen.

Weitere Informationen finden Sie in der Dokumentation zur [kernton-](../coreaudio/core-audio-apis-in-windows-vista.md) API. Wenn dieses Attribut nicht festgelegt ist, verwendet der audiorenderer das standardend Punkt Gerät.

Wenn dieses Attribut festgelegt ist, legen Sie das Attribut für die [**\_ \_ \_ \_ Endpunkt \_ Rolle für das MF-audiorenderer-Attribut**](mf-audio-renderer-attribute-endpoint-role-attribute.md) nicht fest. Wenn beide Attribute festgelegt sind, tritt ein Fehler auf, wenn der audiorenderer erstellt wird.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audiorendererattribute](audio-renderer-attributes.md)
</dt> <dt>

[**Imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**Imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[Streamingaudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 

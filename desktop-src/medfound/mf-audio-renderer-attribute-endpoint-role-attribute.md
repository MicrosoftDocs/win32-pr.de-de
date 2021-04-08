---
description: Gibt die audioendpunktrolle für den audiorenderer an.
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1b6599ffc97cfa9c7fc2b6a75f4ed4ae7c2c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960094"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a>Attribut für die \_ \_ \_ \_ Endpunkt Rolle " \_ MF-audiorenderer"

Gibt die audioendpunktrolle für den audiorenderer an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Sie können dieses Attribut verwenden, um den audiorenderer zu konfigurieren. Die Verwendung hängt von der Funktion ab, die Sie zum Erstellen des audiorenderers aufzurufen:

-   [**MF | ateaudiorenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Legen Sie dieses Attribut mit dem im *paudioattribute* -Parameter angegebenen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstellen Zeiger fest.
-   [**Mfkreateaudiorendereraktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Legen Sie dieses Attribut mit dem [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstellen Zeiger fest, der im *ppaktivierungs* -Parameter abgerufen wurde. Legen Sie das-Attribut vor dem Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)fest.

Bei einem audioendpunktgerät handelt es sich um ein Hardware Gerät, das sich an einem Ende eines audiodatenpfads befindet, z. b. ein Telefon oder ein Redner.

Wenn dieses Attribut festgelegt ist, verwendet der audiorenderer das Standardaudiogerät für die angegebene Rolle. Der Wert dieses Attributs ist ein Member der **erole** -Enumeration, der in der Header Datei mmdeviceapi. h definiert ist. Weitere Informationen finden Sie in der Dokumentation zur kernton-API. Wenn dieses Attribut nicht festgelegt ist, verwendet der audiorenderer das standardend Punkt Gerät.

Wenn dieses Attribut festgelegt ist, legen Sie das [**Attribut \_ Endpunkt-ID für das MF- \_ audiorenderer \_ Attribut \_ \_**](mf-audio-renderer-attribute-endpoint-id-attribute.md) nicht fest. Wenn beide Attribute festgelegt sind, tritt ein Fehler auf, wenn der audiorenderer erstellt wird.

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

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Streamingaudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 





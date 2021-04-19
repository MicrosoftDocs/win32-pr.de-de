---
description: Enthält Flags, um den audiorenderer zu konfigurieren.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17d4b5a51384ebcd180643e0a07601d25e5fb5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350551"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a>Attribut \_ Flags-Attribut für MF- \_ audiorenderer \_ \_

Enthält Flags, um den audiorenderer zu konfigurieren.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein bitweises **or** der folgenden Flags.



| Wert                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **der MF \_ - \_ audiorendererattributflags \_ \_ \_ CrossProcess** | Der audiorenderer verwendet eine prozessübergreifende Audiositzung. Mit diesem Flag können audiorenderer in mehreren Prozessen dieselbe Audiositzung gemeinsam mit den zugehörigen Volumes und Richtlinien Steuerelementen verwenden.<br/> Wenn dieses Flag nicht festgelegt ist, kann die Audiositzung nicht von audiorenderatoren in anderen Prozessen gemeinsam genutzt werden.<br/> |
| **MF \_ - \_ \_ audiorendererattributflags \_ \_ nopersist**    | Die Windows-audiositzungs-API (WASAPI) speichert die Eigenschaften dieser Audiositzung (z. b. das Sitzungs Volume) nicht.<br/> Wenn dieses Flag nicht festgelegt ist, werden die Eigenschaften der Audiositzung von WASAPI persistent gespeichert.<br/>                                                                                                       |



 

Sie können dieses Attribut verwenden, um den audiorenderer zu konfigurieren. Die Verwendung hängt von der Funktion ab, die Sie zum Erstellen des audiorenderers aufzurufen:

-   [**MF | ateaudiorenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Legen Sie dieses Attribut mit dem im *paudioattribute* -Parameter angegebenen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstellen Zeiger fest.
-   [**Mfkreateaudiorendereraktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Legen Sie dieses Attribut mit dem [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstellen Zeiger fest, der im *ppaktivierungs* -Parameter abgerufen wurde. Legen Sie das-Attribut vor dem Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)fest.

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

 

 





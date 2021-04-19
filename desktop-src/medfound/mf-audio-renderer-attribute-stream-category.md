---
description: Gibt die audiostreamkategorie für den streamingaudiorenderer (SAR) an.
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd96c219e43f85c516a5f862e2a978724328a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359973"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a>\_Kategorie-Attribut für das MF- \_ audiorenderattribut \_ \_ Stream \_

Gibt die audiostreamkategorie für den [streamingaudiorenderer](streaming-audio-renderer.md) (SAR) an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Sie können dieses Attribut verwenden, um den audiorenderer zu konfigurieren. Die Verwendung hängt von der Funktion ab, die Sie zum Erstellen des audiorenderers aufgerufen haben.



| Funktion                                                               | Festlegen des Attributs                                                                                                                                                                       |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Mskreateaudiorenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)                 | Verwenden Sie den [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger, der im *paudioattribute* -Parameter angegeben ist.                                                                                          |
| [**MF | ateaudiorendereraktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) | Verwenden Sie den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger, der im *ppaktivierungs* -Parameter zurückgegeben wird. Legen Sie das-Attribut vor dem Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)fest. |



 

Der Wert des-Attributs ist ein Member der [**\_ \_ Kategorie-**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) Enumeration des Audiostreams. Der Audiodienst verwendet die Kategorie Stream, um Audiorichtlinien zu ermitteln, wenn mehrere Anwendungen gleichzeitig Audiodaten abspielen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

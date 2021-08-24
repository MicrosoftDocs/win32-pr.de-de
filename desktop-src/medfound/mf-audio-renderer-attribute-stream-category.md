---
description: Gibt die Audiostreamkategorie für den StreamingAudiorenderer (SAR) an.
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4acb6bd0f40d3c6fb3caa6b4dce8801f8fa60d31222265d5dca6ff5a132444e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714880"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a>MF \_ AUDIO \_ RENDERER ATTRIBUTE STREAM \_ \_ \_ CATEGORY-Attribut

Gibt die Audiostreamkategorie für den [StreamingAudiorenderer](streaming-audio-renderer.md) (SAR) an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Sie können dieses Attribut verwenden, um den Audiorenderer zu konfigurieren. Die Verwendung hängt davon ab, welche Funktion Sie aufrufen, um den Audiorenderer zu erstellen.



| Funktion                                                               | Festlegen des Attributs                                                                                                                                                                       |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)                 | Verwenden Sie den IM *pAudioAttributes-Parameter angegebenen* [**POINTERAttributes-Zeiger.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)                                                                                          |
| [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) | Verwenden Sie den IM *ppActivate-Parameter* zurückgegebenen [**POINTERACTIVATE-Zeiger.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) Legen Sie das -Attribut fest, bevor Sie [**DIE AKTIONACTIVATE::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)aufrufen. |



 

Der Wert des Attributs ist ein Member der [**AUDIO \_ STREAM \_ CATEGORY-Enumeration.**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) Der Audiodienst verwendet die Streamkategorie, um Audiorichtlinien zu bestimmen, wenn mehrere Anwendungen Gleichzeitig Audio wiedergeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

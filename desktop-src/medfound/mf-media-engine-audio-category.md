---
description: Gibt die Kategorie des Audiodatenstroms an.
ms.assetid: 0F2DB9A7-64ED-4952-BCB3-F2B15BA37D2A
title: MF_MEDIA_ENGINE_AUDIO_CATEGORY-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22cd3795886b78afae03ba4b592d4657857f76b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961131"
---
# <a name="mf_media_engine_audio_category-attribute"></a>\_ \_ \_ Audiokategorierungsattribut der MF-Medien-Engine \_

Gibt die Kategorie des Audiodatenstroms an.

## <a name="data-type"></a>Datentyp

**[**\_ \_ audiostreamkategorie**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category)**

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Member der Kategorie-Enumeration des [**\_ Audiostreams \_**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) .

Dieses Attribut wird mit der [**imfmediaengineclassfactory:: forateinstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) -Methode verwendet, um die Medien-Engine zu initialisieren. Das-Attribut ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MF mediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

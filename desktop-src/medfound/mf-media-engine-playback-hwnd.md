---
description: Legt ein Handle für ein Videowiedergabe Fenster für die Medien-Engine fest.
ms.assetid: 63889D81-12C5-47C1-B52A-6358E68830C3
title: MF_MEDIA_ENGINE_PLAYBACK_HWND-Attribut (MF mediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6a9d38d40b04b32244f48289d3334199a7e035
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961126"
---
# <a name="mf_media_engine_playback_hwnd-attribute"></a>Der MF- \_ Medien- \_ Engine-Wiedergabe- \_ \_ HWND

Legt ein Handle für ein Videowiedergabe Fenster für die Medien-Engine fest.

## <a name="data-type"></a>Datentyp

**HWND** als **UINT64** gespeichert

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird mit der [**imfmediaengineclassfactory:: forateinstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) -Methode verwendet, um die Medien-Engine zu initialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>MF mediaengine. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





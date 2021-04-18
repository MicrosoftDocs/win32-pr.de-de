---
description: Gibt eine MMCSS-Klasse (Multimedia Class Scheduler Service) für audioverarbeitungsthreads im Quell-oder senkenwriter an.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: MF_READWRITE_MMCSS_CLASS_AUDIO-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa35db710c6b72c103855fa2c0a9f169f49c4511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368149"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a>MF \_ \_ -Attribut der MMCSS \_ -Klasse für die \_ Audioerstellung

Gibt eine MMCSS-Klasse ( [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) ) für audioverarbeitungsthreads im Quell-oder senkenwriter an.

## <a name="data-type"></a>Datentyp

**LPWSTR**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.

## <a name="remarks"></a>Bemerkungen

Legen Sie dieses Attribut optional fest, wenn Sie eine Instanz des [Quell](source-reader.md) -oder [Senke Writers](sink-writer.md)erstellen. Der Wert des-Attributs muss ein gültiger MMCSS-Klassenname sein.

Wenn dieses Attribut festgelegt ist, registriert der Quell-oder sendenden Writer seine audioverarbeitungsthreads bei der angegebenen MMCSS-Klasse. Das MMCSS stellt sicher, dass die Datenverarbeitung im Quell-oder sendenden Writer Vorrang vor anderen System Tasks hat.

Wenn Sie die Basis Priorität für audiothreads angeben möchten, legen Sie das [audioattribut für die MF \_ -Read Write \_ MMCSS \_ \_ -Priorität](mf-readwrite-mmcss-priority-audio.md) fest. Wenn dieses Attribut nicht festgelegt ist, ist die Basis Priorität für audiothreads 0 (null).

Dieses Attribut überschreibt das MF-Attribut der Klasse "read [ \_ Write \_ MMCSS \_ ](mf-readwrite-mmcss-class.md) " für audioverarbeitungsthreads. Wenn keines der Attribute festgelegt ist, werden audiothreads nicht bei MCSS registriert.

Bei den meisten Anwendungen ist das Audiomaterial für den Benutzer deutlich deutlicher als das Video-und somit weniger akzeptabel. Aus diesem Grund sollte eine Anwendung in der Regel die MF-Klasse "read \_ Write \_ MMCSS \_ Class" \_ auf eine MMCSS-Klasse mit höherer Priorität festlegen als die "MF-Klasse" read [ \_ Write \_ MMCSS \_ ](mf-readwrite-mmcss-class.md)". Dadurch wird sichergestellt, dass die Audioverarbeitung höhere Priorität hat als andere Tasks.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>"Mfreadwrite. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

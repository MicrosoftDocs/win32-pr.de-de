---
description: Gibt eine MMCSS-Klasse (Multimedia Class Scheduler Service) für Die Audioverarbeitung von Threads im Quellleser oder Senkenwriter an.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: MF_READWRITE_MMCSS_CLASS_AUDIO Attribut (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f416c22619c0777ef244e6566328154bf7a7336587fc73a3f29626fcdaa1c462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119345280"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a>MF \_ READWRITE \_ MMCSS \_ CLASS \_ AUDIO-Attribut

Gibt eine [MMCSS-Klasse (Multimedia Class Scheduler Service)](../procthread/multimedia-class-scheduler-service.md) für Die Audioverarbeitung von Threads im Quellleser oder Senkenwriter an.

## <a name="data-type"></a>Datentyp

**Lpwstr**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)auf.

Um dieses Attribut festzulegen, rufen Sie [**DIE ATTRIBUTEAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)auf.

## <a name="remarks"></a>Hinweise

Legen Sie dieses Attribut optional fest, wenn Sie eine Instanz des [Quelllesers](source-reader.md) oder [des Senkenwriters](sink-writer.md)erstellen. Der Wert des Attributs muss ein gültiger MMCSS-Klassenname sein.

Wenn dieses Attribut festgelegt ist, registriert der Quelllese- oder Senkenwriter seine Audioverarbeitungsthreads bei der angegebenen MMCSS-Klasse. MmCSS stellt sicher, dass die Datenverarbeitung im Quelllese- oder Senkenwriter Vorrang vor anderen Systemaufgaben hat.

Um die Basispriorität für Audiothreads anzugeben, legen Sie das [MF \_ READWRITE \_ MMCSS \_ PRIORITY \_ AUDIO-Attribut](mf-readwrite-mmcss-priority-audio.md) fest. Wenn dieses Attribut nicht festgelegt ist, ist die Basispriorität für Audiothreads 0 (null).

Dieses Attribut überschreibt das [MF \_ READWRITE \_ MMCSS \_ CLASS-Attribut](mf-readwrite-mmcss-class.md) für Audioverarbeitungsthreads. Wenn kein Attribut festgelegt ist, werden Audiothreads nicht bei MCSS registriert.

Für die meisten Anwendungen ist die Audiowiedergabe für den Benutzer deutlich erkennbarer als die Videowiedergabe und daher weniger akzeptabel. Aus diesem Grund sollte eine Anwendung MF READWRITE MMCSS CLASS AUDIO in der Regel \_ \_ auf eine \_ \_ MMCSS-Klasse mit höherer Priorität als [MF \_ READWRITE \_ MMCSS \_ CLASS](mf-readwrite-mmcss-class.md)festlegen. Dadurch wird sichergestellt, dass die Audioverarbeitung eine höhere Priorität als andere Aufgaben erhält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

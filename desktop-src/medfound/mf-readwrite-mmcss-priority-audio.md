---
description: Legt die Basis Priorität für die audioverarbeitungsthreads fest, die vom Quell-und senkwriter erstellt werden.
ms.assetid: C0E3A472-959F-4F74-8906-03630DE4CB8C
title: MF_READWRITE_MMCSS_PRIORITY_AUDIO-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c33f3e4cab26a448c3b5a28c6f3cfe631a7c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372887"
---
# <a name="mf_readwrite_mmcss_priority_audio-attribute"></a>MF \_ \_ -audioattribut für die MMCSS \_ \_ -Priorität

Legt die Basis Priorität für die audioverarbeitungsthreads fest, die vom Quell-und senkwriter erstellt werden.

## <a name="data-type"></a>Datentyp

**Int32** als **UInt32** gespeichert

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Legen Sie dieses Attribut optional fest, wenn Sie eine Instanz des [Quell](source-reader.md) -oder [Senke Writers](sink-writer.md)erstellen. Wenn Sie dieses Attribut festlegen, legen Sie auch [das \_ audioattribut der MF \_ \_ \_ -Klasse "Read Write MMCSS Class](mf-readwrite-mmcss-class-audio.md) " fest. Andernfalls wird dieses Attribut ignoriert.

Wenn der Quell-oder senkenwriter audioverarbeitungsthreads beim [Multimedia Class Scheduler-Dienst](../procthread/multimedia-class-scheduler-service.md)registriert, gibt der Wert dieses Attributs die Basis Thread Priorität an. Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert 0 (null).

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

 

 

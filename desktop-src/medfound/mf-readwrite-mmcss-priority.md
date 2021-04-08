---
description: Legt die Basis Thread Priorität für den Quell-oder senderwriter fest.
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: MF_READWRITE_MMCSS_PRIORITY-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7b83485b49e6ae584a38024e180f37c878d27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050459"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a>MF- \_ Attribut zum Lesen von \_ MMCSS- \_ Priorität

Legt die Basis Thread Priorität für den Quell-oder senderwriter fest.

## <a name="data-type"></a>Datentyp

**Int32** als **UInt32** gespeichert

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Legen Sie dieses Attribut optional fest, wenn Sie eine Instanz des [Quell](source-reader.md) -oder [Senke Writers](sink-writer.md)erstellen. Wenn Sie dieses Attribut festlegen, legen Sie auch das MF-Attribut der Klasse "read [ \_ Write \_ MMCSS \_ Class](mf-readwrite-mmcss-class.md) " fest. Andernfalls wird dieses Attribut ignoriert.

Wenn der Quell-oder senkenwriter Threads beim [Multimedia Class Scheduler-Dienst](../procthread/multimedia-class-scheduler-service.md)registriert, gibt der Wert dieses Attributs die Basis Thread Priorität an. Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert 0 (null).

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

 

 

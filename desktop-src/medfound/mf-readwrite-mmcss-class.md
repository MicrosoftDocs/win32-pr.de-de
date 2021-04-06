---
description: Gibt eine MMCSS-Klasse (Multimedia Class Scheduler Service) für den Quell Reader oder den senkenwriter an.
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: MF_READWRITE_MMCSS_CLASS-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759078"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a>MF- \_ \_ Attribut der MMCSS- \_ Klasse "Read Write"

Gibt eine MMCSS-Klasse ( [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) ) für den Quell Reader oder den senkenwriter an.

## <a name="data-type"></a>Datentyp

**LPWSTR**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.

## <a name="remarks"></a>Bemerkungen

Legen Sie dieses Attribut optional fest, wenn Sie eine Instanz des [Quell](source-reader.md) -oder [Senke Writers](sink-writer.md)erstellen. Der Wert des-Attributs muss ein gültiger MMCSS-Klassenname sein.

Wenn dieses Attribut festgelegt ist, registriert der Quell-oder sendenden Writer alle zugehörigen Threads bei der angegebenen MMCSS-Klasse. Das MMCSS stellt sicher, dass die Datenverarbeitung im Quell-oder sendenden Writer Vorrang vor anderen System Tasks hat.

Um die Basis Priorität anzugeben, legen Sie das MF-Attribut "read [ \_ Write \_ MMCSS \_ Priority](mf-readwrite-mmcss-priority.md) " fest. Wenn dieses Attribut nicht festgelegt ist, ist die Basis Priorität 0 (null).

Bei audioverarbeitungsthreads überschreibt das audioattribut für die MF-Klasse "read [ \_ Write \_ MMCSS \_ Class \_ ](mf-readwrite-mmcss-class-audio.md) " (falls festgelegt) dieses Attribut.

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

 

 

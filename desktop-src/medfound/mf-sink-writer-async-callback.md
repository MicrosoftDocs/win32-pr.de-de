---
description: Enthält einen Zeiger auf die Anwendungs Rückruf Schnittstelle für den Senke-Writer.
ms.assetid: 22df1fa0-469d-4501-aaf0-a0379b7ed096
title: MF_SINK_WRITER_ASYNC_CALLBACK-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f11bed051df9107ca3a2247b6c3d0cf2058224c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759570"
---
# <a name="mf_sink_writer_async_callback-attribute"></a>\_ \_ \_ Async- \_ Rückruf Attribut für das MF-Sink-Writer

Enthält einen Zeiger auf die Rückruf Schnittstelle der Anwendung für den Senke-Writer.

## <a name="data-type"></a>Datentyp

**[**Imbsinkschreiterrückruf**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) \** _ als " _*IUnknown \** " gespeichert_

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Zeiger auf die [**imfsinkschreitercallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) -Schnittstelle der Anwendung.

Verwenden Sie dieses Attribut mit den folgenden Funktionen:

-   [**Mfkreatesinkschreiterfrommediasink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MF | atesinkschreiterfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"Mfreadwrite. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Senkenwriter-Attribute](sink-writer-attributes.md)
</dt> </dl>

 

 





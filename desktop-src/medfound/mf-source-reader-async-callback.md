---
description: Enthält einen Zeiger auf die Anwendungs Rückruf Schnittstelle für den Quell Reader.
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: MF_SOURCE_READER_ASYNC_CALLBACK-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66542a155fbb6fa3e56958733626b1d0b750ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216876"
---
# <a name="mf_source_reader_async_callback-attribute"></a>\_ \_ \_ Async- \_ Rückruf Attribut des MF-Quell Readers

Enthält einen Zeiger auf die Rückruf Schnittstelle der Anwendung für den [Quell Reader](source-reader.md).

## <a name="data-type"></a>Datentyp

**IMF sourcereadercallback \** _ als " _*IUnknown \** " gespeichert_

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Zeiger auf die [**imfsourcereadercallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) -Schnittstelle der Anwendung.

Verwenden Sie dieses Attribut mit den folgenden Funktionen:

-   [**MF | atesourcereaderfromb-testream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**Mfkreatesourcereaderfrommediasource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MF | atesourcereaderfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

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

[Quell Leser](source-reader.md)
</dt> <dt>

[Attribute des Quell Readers](source-reader-attributes.md)
</dt> </dl>

 

 





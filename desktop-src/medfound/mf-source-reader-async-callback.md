---
description: Enthält einen Zeiger auf die Anwendungsrückrufschnittstelle für den Quellleser.
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: MF_SOURCE_READER_ASYNC_CALLBACK-Attribut (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af4dedfcdcb426eb62a0ae14bec3fd75232c9a871d0bad10194860305c687fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605155"
---
# <a name="mf_source_reader_async_callback-attribute"></a>MF \_ SOURCE \_ READER \_ ASYNC \_ CALLBACK-Attribut

Enthält einen Zeiger auf die Rückrufschnittstelle der Anwendung für den [Quellleser.](source-reader.md)

## <a name="data-type"></a>Datentyp

**ÜBERLAGERUNGSourceReaderCallback \* *_ gespeichert als _* IUnknown\***

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUnknown auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)

Um dieses Attribut festzulegen, rufen Sie [**DIE ATTRIBUTEAttributes::SetUnknown auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein Zeiger auf die [**POINTERSourceReaderCallback-Schnittstelle**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) der Anwendung.

Verwenden Sie dieses Attribut mit den folgenden Funktionen:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Quellleser](source-reader.md)
</dt> <dt>

[Quellleseattribute](source-reader-attributes.md)
</dt> </dl>

 

 





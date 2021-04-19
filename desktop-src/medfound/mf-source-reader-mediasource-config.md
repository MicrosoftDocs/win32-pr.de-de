---
description: Enthält Konfigurations Eigenschaften für den Quell Reader.
ms.assetid: f7e5ef6a-5fc3-4f39-acc0-61ce79030211
title: MF_SOURCE_READER_MEDIASOURCE_CONFIG-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f36b2a09810dd1c2563033ea65643f1dabcb3f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106370349"
---
# <a name="mf_source_reader_mediasource_config-attribute"></a>MF- \_ Quell \_ Leser \_ MediaSource \_ config-Attribut

Enthält Konfigurations Eigenschaften für den [Quell Reader](source-reader.md).

## <a name="data-type"></a>Datentyp

**IPropertyStore \* *_ gespeichert als _* IUnknown\***

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Zeiger auf die **IPropertyStore** -Schnittstelle eines Eigenschaften Stores. Sie können dieses Attribut verwenden, um Konfigurations Eigenschaften an die Medienquelle zu übergeben.

Verwenden Sie dieses Attribut mit den folgenden Funktionen:

-   [**MF | atesourcereaderfromb-testream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MF | atesourcereaderfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Intern übergibt der Quell Reader den **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

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

 

 





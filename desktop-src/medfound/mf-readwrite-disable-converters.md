---
description: Aktiviert oder deaktiviert Formatkonvertierungen durch den Quell-oder senkenwriter.
ms.assetid: 282b70c3-c81c-47dd-bfa2-7e77138ccb91
title: MF_READWRITE_DISABLE_CONVERTERS-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8532c45ca3aeb272fa6b6ef422e0d82e40bd3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218238"
---
# <a name="mf_readwrite_disable_converters-attribute"></a>MF- \_ /Schreib-deaktivierte \_ \_ Konverter

Aktiviert oder deaktiviert Formatkonvertierungen durch den Quell-oder senkenwriter.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Standardmäßig können der Quell-und der senkenwriter einige Formatkonvertierungen für unkomprimierte Audiodaten und Videostreams ausführen. Um dieses Verhalten zu deaktivieren, legen Sie dieses Attribut auf " **true** " fest, wenn Sie den Quell-oder senderwriter erstellen.

Verwenden Sie dieses Attribut mit den folgenden Funktionen:

-   [**MF | atesourcereaderfromb-testream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**Mfkreatesourcereaderfrommediasource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MF | atesourcereaderfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
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
</dt> <dt>

[Attribute des Quell Readers](source-reader-attributes.md)
</dt> </dl>

 

 





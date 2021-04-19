---
description: Gibt an, ob ein Byte Strom Handler einen Bytestream verwenden kann, der zum Schreiben durch einen anderen Thread geöffnet ist.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46a3402585cbce9c1d1464ceb9fb161527673c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356864"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a>MF \_ bytestreamhandler \_ akzeptiert \_ Freigabe- \_ Schreib Attribute

Gibt an, ob ein Byte Strom Handler einen Bytestream verwenden kann, der zum Schreiben durch einen anderen Thread geöffnet ist.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Bytestreamhandler können dieses Attribut unterstützen. Um das Attribut zu erhalten oder festzulegen, Fragen Sie zuerst den bytestreamhandler für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle ab. Anschließend wird [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) oder [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) aufgerufen.

Wenn dieses Attribut **true** ist, bedeutet dies, dass der Byte Datenstrom Handler aus einem Stream lesen kann, während ein anderer Thread in denselben Stream schreibt. Wenn ein Stream zum Schreiben durch einen anderen Thread geöffnet wird, gibt die [**imfbytestream:: getfunktionalitäten**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) -Methode das **mfbytestream-freigabeflag für die \_ Freigabe \_** zurück.

Dieses Attribut wirkt sich auf die Quell Auflösung aus. Wenn für einen Bytestream das **\_ \_ kennschreibflag für die mfbytestream-Freigabe** festgelegt ist, übergibt der [quellresolver](source-resolver.md) diesen Stream nicht an einen Byte Datenstrom-Handler, es sei denn, der Handler hat den MF \_ bytestreamhandler \_ akzeptiert das \_ \_ Attribut für Freigabe Schreibzugriff auf **true**

Das **MF Bytestream- \_ Freigabe \_ Schreib** Flag ist ein Hinweis darauf, dass sich die Länge des Streams ändern kann, während der Handler aus ihm liest.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Schema Handler und Byte-Stream Handler](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 





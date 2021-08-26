---
description: Gibt an, ob ein Bytestreamhandler einen Bytestream verwenden kann, der zum Schreiben durch einen anderen Thread geöffnet wird.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ea9b6cf1d126fca44066e7d3292227ecf0ce01f3419b377b6d66b67845f990
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941030"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a>MF \_ BYTESTREAMHANDLER \_ AKZEPTIERT SHARE \_ \_ WRITE-Attribut

Gibt an, ob ein Bytestreamhandler einen Bytestream verwenden kann, der zum Schreiben durch einen anderen Thread geöffnet wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Bytestreamhandler können dieses Attribut unterstützen. Um das Attribut zu erhalten oder fest zu legen, fragen Sie zunächst den Bytestreamhandler für die [**BENUTZERDEFINIERTEAttributes-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) ab. Rufen Sie [**dann DIE ATTRIBUTEattribute::GetUINT32 oder**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) DIE ATTRIBUTE [**auf::SetUINT32.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

Wenn dieses Attribut **TRUE ist,** bedeutet dies, dass der Bytestreamhandler aus einem Stream lesen kann, während ein anderer Thread in den gleichen Stream schreibt. Wenn ein Stream für das Schreiben durch einen anderen Thread geöffnet wird, gibt die [**METHODE THREADSByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) das **MFBYTESTREAM \_ SHARE \_ WRITE-Flag** zurück.

Dieses Attribut wirkt sich auf die Quellauflösung aus. Wenn für einen Bytestream das **MFBYTESTREAM \_ SHARE \_ WRITE-Flag** festgelegt ist, über gibt der Quellre [resolver](source-resolver.md) diesen Stream nicht an einen Bytestreamhandler weiter, es sei denn, für den Handler ist das MF \_ BYTESTREAMHANDLER ACCEPTS SHARE WRITE-Attribut auf \_ \_ \_ **TRUE** festgelegt.

Das **MFBYTESTREAM \_ SHARE \_ WRITE-Flag** ist ein Hinweis darauf, dass sich die Länge des Streams ändern kann, während der Handler daraus liest.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Schemahandler und Byte-Stream Handler](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 





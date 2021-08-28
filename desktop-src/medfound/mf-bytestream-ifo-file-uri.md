---
description: 'Enthält die URL der VOM HTTP-Server im HTTP-Header angegebenen IFO-Datei (DVD-Informationen) &\# 0034; Pragma: ifoFileURI.dlna.org&\# 0034;.'
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: MF_BYTESTREAM_IFO_FILE_URI Attribut (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4349f3319a875f428921b0a99aefa61e49340c240a87260c1132abcc7c45f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723470"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a>MF \_ BYTESTREAM \_ IFO \_ \_ FILE-URI-Attribut

Enthält die URL der IFO-Datei (DVD Information), die vom HTTP-Server im HTTP-Header "Pragma: ifoFileURI.dlna.org" angegeben wird.

## <a name="data-type"></a>Datentyp

**Lpwstr**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)auf.

Um dieses Attribut festzulegen, rufen Sie [**DIE ATTRIBUTEAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)auf.

## <a name="applies-to"></a>Gilt für:

[**GIGABYTEByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>Hinweise

Der HTTP-Bytestream durchsucht den HTTP-Header nach der Zeichenfolge "ifoFileURI.dlna.org". Wenn die Zeichenfolge gefunden wird, wird sie in dieses Attribut im Bytestream kopiert.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                                           |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Bytestreamattribute](byte-stream-attributes.md)
</dt> <dt>

[**GIGABYTEByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 





---
description: 'Enthält die URL der vom HTTP-Server im HTTP-Header angegebenen Datei vom HTTP-Server (DVD-Informationen), &\# 0034; Pragma: ifoFileURI.DLNA.org&\# 0034;.'
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: MF_BYTESTREAM_IFO_FILE_URI-Attribut (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c80e015b68272b073c442b4064c80a6787b811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349106"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a>\_Datenstrom- \_ URI- \_ \_ Attribut für MF-Bytestream

Enthält die URL der vom HTTP-Server im HTTP-Header angegebenen-Datei ("Pragma: ifoFileURI.DLNA.org").

## <a name="data-type"></a>Datentyp

**LPWSTR**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.

## <a name="applies-to"></a>Gilt für:

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>Bemerkungen

Der http-Bytestream durchsucht den HTTP-Header nach der Zeichenfolge "ifoFileURI.DLNA.org". Wenn die Zeichenfolge gefunden wird, wird Sie in dieses Attribut im Bytestream kopiert.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                                           |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Byte Datenstrom Attribute](byte-stream-attributes.md)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 





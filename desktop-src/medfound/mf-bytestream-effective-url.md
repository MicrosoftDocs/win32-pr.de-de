---
description: Ruft die effektive URL eines Bytestreams ab.
ms.assetid: 0A83CFC0-7EAA-464B-BA39-50DF220AF683
title: MF_BYTESTREAM_EFFECTIVE_URL-Attribut (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95e01238f04c30f72d55f940b3f3105863247ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368126"
---
# <a name="mf_bytestream_effective_url-attribute"></a>Effektive MF- \_ Bytestream- \_ URL- \_ Attribut

Ruft die effektive URL eines Bytestreams ab.

## <a name="data-type"></a>Datentyp

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.

## <a name="applies-to"></a>Gilt für:

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>Bemerkungen

Die effektive URL kann sich von der ursprünglichen URL unterscheiden, wenn die ursprüngliche URL zusätzliche Informationen enthält, z. b. Such Zeichenfolgen oder Anker, oder wenn die Anforderung umgeleitet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfobjects. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Byte Datenstrom Attribute](byte-stream-attributes.md)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 





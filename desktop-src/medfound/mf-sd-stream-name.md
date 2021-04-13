---
description: Enthält den Namen eines Streams.
ms.assetid: 80235820-761f-4deb-9bf6-82ef402b3ee4
title: MF_SD_STREAM_NAME-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734c2d20390ba1a450a40c03054b4c67c5c0409a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349119"
---
# <a name="mf_sd_stream_name-attribute"></a>\_SD-SD-Stream- \_ \_ Namensattribut

Enthält den Namen eines Streams.

## <a name="data-type"></a>Datentyp

**WCHAR \** _

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.

## <a name="applies-to"></a>Gilt für:

[**IMF-Deskriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a>Bemerkungen

Mit der AVI-Medienquelle wird dieses Attribut festgelegt, wenn die AVI-Datei ein "" "" ein "-Segment enthält.

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

[Streamdeskriptorattribute](stream-descriptor-attributes.md)
</dt> </dl>

 

 





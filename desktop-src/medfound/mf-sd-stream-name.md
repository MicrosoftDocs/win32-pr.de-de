---
description: Enthält den Namen eines Streams.
ms.assetid: 80235820-761f-4deb-9bf6-82ef402b3ee4
title: MF_SD_STREAM_NAME -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312ca788b03c3bef075c2c51d06df921d258e7372c091c5ccb43ec248444fcfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474055"
---
# <a name="mf_sd_stream_name-attribute"></a>MF \_ SD \_ STREAM \_ NAME-Attribut

Enthält den Namen eines Streams.

## <a name="data-type"></a>Datentyp

**Wchar\***

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DEN ATTRIBUTEAttributes::GetString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)

Rufen Sie ZUM Festlegen dieses [**Attributs DEN WERTATTRIBUTEs::SetString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)

## <a name="applies-to"></a>Gilt für:

[**JAVASCRIPTStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a>Hinweise

Die AVI-Medienquelle legt dieses Attribut fest, wenn die AVI-Datei einen "strn"-Block enthält.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Streamdeskriptorattribute](stream-descriptor-attributes.md)
</dt> </dl>

 

 





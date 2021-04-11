---
description: Enthält den ursprünglichen Codec FourCC für einen Videostream.
ms.assetid: 2e6ef198-5754-4ded-9fe3-61edd0742a17
title: MF_MT_ORIGINAL_4CC-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b374ba3ef74cb98925edcc5d809e1fd5e0b7fbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960412"
---
# <a name="mf_mt_original_4cc-attribute"></a>MF \_ MT \_ ursprüngliches \_ 4CC-Attribut

Enthält den ursprünglichen Codec FourCC für einen Videostream.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Bemerkungen

Abhängig von der Quelldatei kann die AVI-Medienquelle dieses Attribut auf den Medientypen festlegen, die es anbietet.

Eine AVI-Datei enthält einen Streamheader für jeden Stream in der Datei. Die AVI-Medienquelle übersetzt den Datenstrom Header in einen Medientyp. Für komprimierte Videostreams enthält der Stream-Header ein FourCC, das den Videocodec identifiziert. In den meisten Fällen konvertiert die AVI-Medienquelle diesen FourCC direkt in eine Untertyp-GUID, wie im Thema [Video Untertyp-GUIDs](video-subtype-guids.md)beschrieben. In einigen Fällen wird das ursprüngliche FourCC jedoch einem anderen FourCC zugeordnet, das Äquivalent ist. Wenn dies der Fall ist, speichert die Medienquelle den ursprünglichen FourCC im Medientyp, wobei das MF \_ MT \_ Original \_ 4CC-Attribut verwendet wird.

Die FourCC-Zuordnungen werden in der Registrierung unter folgendem Schlüssel gespeichert:

**HKEY \_ Klassen- \_ root** \\ **mediafoundations** \\ **MapVideo4cc**

Jeder Eintrag ist ein **DWORD** -Wert. Der Name des Eintrags ist die hexadezimale Darstellung des FourCC ohne das Präfix "0x" und das erste Zeichen, das zuerst in der Zeichenfolge angezeigt wird. Der FourCC-Code "abcd" würde z. b. als "61626364" angezeigt werden. Der Wert des Eintrags ist der entsprechende FourCC-Code.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 





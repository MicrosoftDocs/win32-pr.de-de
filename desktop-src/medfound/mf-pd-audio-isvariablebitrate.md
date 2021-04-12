---
description: Gibt an, ob die Audiodatenströme in einer Präsentation eine Variable Bitrate aufweisen.
ms.assetid: 2bd7eee1-5a93-4bde-8b58-80b6395a094e
title: MF_PD_AUDIO_ISVARIABLEBITRATE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a34d3dd64f9100050dc9aae37e811d00c9d58af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216879"
---
# <a name="mf_pd_audio_isvariablebitrate-attribute"></a>MF \_ PD \_ - \_ audioattribut "isvariablebitrate"

Gibt an, ob die Audiodatenströme in einer Präsentation eine Variable Bitrate aufweisen.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Bemerkungen

Dies ist ein optionales Attribut für Präsentations Deskriptoren. Wenn das Attribut **true** (ungleich null) ist, enthält die Präsentation mindestens einen Audiostream mit variabler Bitrate (VBR). Wenn das Attribut **false** ist, haben alle Audiostreams eine Konstante Bitrate.

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

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> </dl>

 

 





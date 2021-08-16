---
description: Profilflags, die die Streameinstellungen für die Transcodierungstopologie definieren. Die Flags werden in der MF \_ TRANSCODE \_ ADJUST PROFILE \_ \_ FLAGS-Enumeration definiert.
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: MF_TRANSCODE_ADJUST_PROFILE -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb25f4df47d281ddb0e359d98e8a411cb3abb365b479388e9b7ae107e786703c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739468"
---
# <a name="mf_transcode_adjust_profile-attribute"></a>MF \_ TRANSCODE \_ ADJUST \_ PROFILE-Attribut

Profilflags, die die Streameinstellungen für die Transcodierungstopologie definieren. Die Flags werden in der [**MF \_ TRANSCODE \_ ADJUST PROFILE \_ \_ FLAGS-Enumeration**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) definiert.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Eine Anwendung kann dieses Attribut auf Containerebene für das Transcodierungsprofil festlegen. Wenn dieses Attribut festgelegt ist, ändert die [**MFCreateTranscodeTopology-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) die Streamattribute während der Topologieerbauung abhängig vom angegebenen Flag. Wenn die Anwendung beispielsweise das **FLAG MF \_ TRANSCODE ADJUST PROFILE \_ \_ \_ DEFAULT** angibt, werden die von der Anwendung angegebenen Streameinstellungen zum Erstellen des Profils verwendet.

Für den Videostream wird die Bildfrequenz basierend auf der Medienquelle aktualisiert. Wenn die Anwendung den Interlaced-Modus nicht an gibt, wird das Profil standardmäßig so aktualisiert, dass progressive Frames verwendet werden.

Wenn die Anwendung das **MF \_ TRANSCODE \_ ADJUST PROFILE USE SOURCE \_ \_ \_ \_ ATTRIBUTES-Flag** angibt, werden fehlende Streamattribute aus der Eingabemedienquelle in die Streameinstellungen im Transcodeprofil kopiert.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transcodierungs-API](transcode-api.md)
</dt> <dt>

[**CODIERUNGTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 





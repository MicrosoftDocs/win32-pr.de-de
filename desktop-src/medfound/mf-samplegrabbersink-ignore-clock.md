---
description: Gibt an, ob die Stichprobengrabsenke die Präsentationsuhr verwendet, um Stichproben zu planen.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: MF_SAMPLEGRABBERSINK_IGNORE_CLOCK -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d757b02a060b4e598ff42d3bd8b9ad7f38af41143c807647aa6f2b8528677cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474423"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a>MF \_ SAMPLEGRABBERSINK \_ IGNORE \_ CLOCK-Attribut

Gibt an, ob die Stichprobengrabsenke die Präsentationsuhr verwendet, um Stichproben zu planen.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Sie können dieses Attribut für das Aktivierungsobjekt festlegen, das von der [**MFCreateSampleGrabberSinkActivate-Funktion erstellt**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) wurde. Legen Sie das -Attribut fest, bevor [**Sie die METHODE VERWERTERAktivieren::ActivateObject für**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) das Aktivierungsobjekt aufrufen.

Wenn die Sample-Grabber-Senke ein Beispiel empfängt, wartet sie standardmäßig bis zur Präsentationszeit des Beispiels, um den Rückruf der Anwendung aufrufen. Wenn das MF SAMPLEGRABBERSINK IGNORE CLOCK-Attribut ungleich 0 (null) ist, ignoriert die \_ \_ Sample-Grabber-Senke die Präsentationsuhr und ruft den Rückruf auf, sobald die einzelnen Stichproben empfangen \_ werden.

Empfohlene Verwendung:

-   Wenn Sie Beispiele so schnell wie möglich verarbeiten möchten, legen Sie dieses Attribut auf **TRUE fest.**
-   Wenn sie möchten, dass die Aufrufe der Rückrufmethode mit der Uhr synchronisiert werden, legen Sie dieses Attribut entweder nicht fest, oder legen Sie es auf **FALSE fest.** Sie können Stichproben etwas vor der Uhr erhalten, während sie noch synchronisiert bleiben, indem Sie das [**MF \_ SAMPLEGRABBERSINK \_ SAMPLE TIME \_ \_ OFFSET-Attribut**](mf-samplegrabbersink-sample-time-offset-attribute.md) festlegen.

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

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 





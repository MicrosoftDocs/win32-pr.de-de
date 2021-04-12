---
description: Legt die maximale Anzahl nicht verarbeiteter Beispiele fest, die für die Verarbeitung im Audiopfad der Daten Satz Senke gepuffert werden können.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442e9b5eca3354e87b8e36b55a3c6cb92ec6f131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344579"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a>Daten \_ \_ Satz \ \_ \_ \_ \_ Maximales \_ nicht verarbeitetes \_ Samples-Attribut der MF-Erfassung

Legt die maximale Anzahl nicht verarbeiteter Beispiele fest, die für die Verarbeitung im Audiopfad der Daten Satz Senke gepuffert werden können.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für die Aufzeichnungs-Engine zu konfigurieren, fügen Sie es dem *pattributes* -Parameter hinzu, wenn Sie [**imfcaptureengine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)aufrufen.

Der Höchstwert für dieses Attribut ist 100.

Nachdem der Datensatz die maximale Anzahl nicht verarbeiteter Stichproben gepuffert hat, die durch die MF \_ -Erfassungs \_ -Engine aufgezeichnet wurde, die \_ \_ \_ \_ \_ nicht verarbeiteten \_ Beispiele enthält, wird die Framerate durch Verwerfen von Beispielen gelöscht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>"MF"-Engine. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attribute der Aufzeichnungs-Engine](capture-engine-attributes.md)
</dt> <dt>

[**IMF captureengine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 





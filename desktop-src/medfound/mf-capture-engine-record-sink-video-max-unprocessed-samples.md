---
description: Legt die maximale Anzahl nicht verarbeiteter Beispiele fest, die für die Verarbeitung im Video Pfad der Daten Satz Senke gepuffert werden können.
ms.assetid: B3B5C547-1F06-45B1-BFCB-513AD7B6A9B6
title: MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f5e297ddb5f06e71fe05a95df73aa205a7889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863595"
---
# <a name="mf_capture_engine_record_sink_video_max_unprocessed_samples-attribute"></a>\_ \_ \_ Daten Satz-Sink \_ - \_ Video \_ \_ \_ für die MF-Erfassung-Video

Legt die maximale Anzahl nicht verarbeiteter Beispiele fest, die für die Verarbeitung im Video Pfad der Daten Satz Senke gepuffert werden können.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für die Aufzeichnungs-Engine zu konfigurieren, fügen Sie es dem *pattributes* -Parameter hinzu, wenn Sie [**imfcaptureengine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)aufrufen.

Der Maximalwert für dieses Attribut ist 17.

Nachdem der Datensatz die maximale Anzahl nicht verarbeiteter Stichproben gepuffert hat, die von der MF-Aufzeichnungs- \_ \_ Engine- \_ Daten Satz- \_ \_ senkenvideo \_ Max \_ . nicht verarbeitete Beispiele angegeben wurde \_ , wird die Frame Rate durch Verwerfen von

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

 

 





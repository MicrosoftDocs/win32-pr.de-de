---
description: Legt die maximale Anzahl von verarbeiteten Stichproben fest, die im Video Pfad der Daten Satz Senke gepuffert werden können.
ms.assetid: 5AFA197E-5A7F-402E-A62B-4F624A5DD917
title: MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_PROCESSED_SAMPLES-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70c3840f449cebb6579b2c1df5f330379ba30655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752456"
---
# <a name="mf_capture_engine_record_sink_video_max_processed_samples-attribute"></a>\_ \_ \_ Daten Satz-Sink-Video Daten Satz- \_ Sink- \_ Video \_ \_ \_

Legt die maximale Anzahl von verarbeiteten Stichproben fest, die im Video Pfad der Daten Satz Senke gepuffert werden können.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für die Aufzeichnungs-Engine zu konfigurieren, fügen Sie es dem *pattributes* -Parameter hinzu, wenn Sie [**imfcaptureengine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)aufrufen.

Der Maximalwert für dieses Attribut ist 17.

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

 

 





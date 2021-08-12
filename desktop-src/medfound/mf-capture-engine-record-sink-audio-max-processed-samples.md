---
description: Legt die maximale Anzahl verarbeiteter Stichproben fest, die im Audiopfad der Aufzeichnungssenke gepuffert werden können.
ms.assetid: 216886DB-B206-4944-925A-C2106331F1CB
title: MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_PROCESSED_SAMPLES Attribut (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b4478ebecfc873c612e8deb0106cba5462e77cd56d5d818b03d74e88679c8b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245038"
---
# <a name="mf_capture_engine_record_sink_audio_max_processed_samples-attribute"></a>MF \_ CAPTURE ENGINE RECORD SINK AUDIO MAX PROCESSED \_ \_ \_ \_ \_ \_ \_ SAMPLES-Attribut

Legt die maximale Anzahl verarbeiteter Stichproben fest, die im Audiopfad der Aufzeichnungssenke gepuffert werden können.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Um dieses Attribut für die Erfassungs-Engine zu konfigurieren, fügen Sie es dem *pAttributes-Parameter* hinzu, wenn Sie [**DENCAPtureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)aufrufen.

Der Höchstwert für dieses Attribut ist 100.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attribute der Erfassungs-Engine](capture-engine-attributes.md)
</dt> <dt>

[**ADRPaturEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 





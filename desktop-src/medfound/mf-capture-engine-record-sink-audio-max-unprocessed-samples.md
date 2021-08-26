---
description: Legt die maximale Anzahl von nicht verarbeiteten Stichproben fest, die für die Verarbeitung im Audiopfad der Aufzeichnungssenke gepuffert werden können.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES -Attribut (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5f6d2a2bcd592d5a6991028af90af008a827940903084054933558ed7088c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060830"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a>MF \_ CAPTURE ENGINE RECORD SINK AUDIO MAX \_ \_ \_ \_ \_ \_ UNPROCESSED \_ SAMPLES attribute

Legt die maximale Anzahl von nicht verarbeiteten Stichproben fest, die für die Verarbeitung im Audiopfad der Aufzeichnungssenke gepuffert werden können.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Hinweise

Um dieses Attribut in der Erfassungs-Engine zu konfigurieren, fügen Sie es dem *pAttributes-Parameter* hinzu, wenn Sie [**DIECAPtureEngine::Initialize aufrufen.**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)

Der Höchstwert für dieses Attribut ist 100.

Sobald der Datensatz die maximale Anzahl von nicht verarbeiteten Stichproben gepuffert hat, die von MF CAPTURE ENGINE RECORD SINK AUDIO MAX UNPROCESSED SAMPLES angegeben wird, wird die Framerate durch Löschen von Stichproben \_ \_ \_ \_ \_ \_ \_ \_ gepuffert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capture Engine-Attribute](capture-engine-attributes.md)
</dt> <dt>

[**INITIALIZECaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 





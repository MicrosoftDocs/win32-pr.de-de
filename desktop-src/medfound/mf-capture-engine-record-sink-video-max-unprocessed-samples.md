---
description: Legt die maximale Anzahl von nicht verarbeiteten Stichproben fest, die für die Verarbeitung im Videopfad der Aufzeichnungssenke gepuffert werden können.
ms.assetid: B3B5C547-1F06-45B1-BFCB-513AD7B6A9B6
title: MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES-Attribut (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f776dd795103fccf81da4c739b767131a03bf83245c3c79e724274dcb52dc0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956820"
---
# <a name="mf_capture_engine_record_sink_video_max_unprocessed_samples-attribute"></a>MF \_ CAPTURE ENGINE RECORD SINK VIDEO MAX \_ \_ \_ \_ \_ \_ UNPROCESSED \_ SAMPLES ATTRIBUTE

Legt die maximale Anzahl von nicht verarbeiteten Stichproben fest, die für die Verarbeitung im Videopfad der Aufzeichnungssenke gepuffert werden können.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Hinweise

Um dieses Attribut für die Erfassungs-Engine zu konfigurieren, fügen Sie es dem *pAttributes-Parameter* hinzu, wenn Sie [**DENCAPtureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)aufrufen.

Der Höchstwert für dieses Attribut ist 17.

Sobald der Datensatz die maximale Anzahl nicht verarbeiteter Stichproben gepuffert hat, die von MF \_ CAPTURE ENGINE RECORD SINK VIDEO MAX \_ \_ \_ \_ UNPROCESSED SAMPLES angegeben \_ \_ \_ wird, sinkt die Bildrate durch Löschen von Stichproben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attribute der Erfassungs-Engine](capture-engine-attributes.md)
</dt> <dt>

[**ADRPaturEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 





---
description: Die folgenden Attribute können verwendet werden, um die Erfassungs-Engine zu konfigurieren.
ms.assetid: C153F0AD-4E8B-41DA-B7FB-8D10AC20D22E
title: Attribute der Erfassungs-Engine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e79d0410407d12b46c0577615088f0f925b8558169d02140486b9fdc8fb303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959150"
---
# <a name="capture-engine-attributes"></a>Attribute der Erfassungs-Engine

Die folgenden Attribute können verwendet werden, um die Erfassungs-Engine zu konfigurieren.

Die folgenden Attribute beziehen sich auf Erfassungsgeräte:



| attribute                                                                                                                              | Beschreibung                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [MF \_ CAPTURE \_ ENGINE \_ CAMERA \_ STREAM \_ BLOCKED](mf-capture-engine-camera-stream-blocked.md)                                            | Signalisiert, dass die Videoaufnahme vom Treiber blockiert wird.                                                         |
| [MF \_ CAPTURE \_ ENGINE \_ CAMERA \_ STREAM \_ UNBLOCKED](mf-capture-engine-camera-stream-unblocked.md)                                        | Signalisiert, dass die Videoaufnahme wiederhergestellt wird, nachdem sie blockiert wurde.                                                        |
| [MF \_ CAPTURE \_ ENGINE \_ D3D \_ MANAGER](mf-capture-engine-d3d-manager.md)                                                                 | Legt einen Zeiger auf die DXGI-Geräte-Manager auf der Erfassungs-Engine fest.                                                   |
| [MF \_ CAPTURE \_ ENGINE \_ DECODER \_ MFT \_ FIELDOFUSE \_ UNLOCK \_ ATTRIBUTE](mf-capture-engine-decoder-mft-fieldofuse-unlock-attribute.md)      | Ermöglicht der Erfassungs-Engine die Verwendung eines Decoders mit Verwendungseinschränkungen.                                    |
| [MF \_ CAPTURE \_ ENGINE \_ DISABLE \_ DXVA](mf-capture-engine-disable-dxva.md)                                                               | Gibt an, ob die Erfassungs-Engine DirectX Video Acceleration (DXVA) für die Videodecodierung verwendet.                    |
| [MF \_ CAPTURE \_ DISABLE \_ HARDWARE \_ TRANSFORMS](mf-capture-engine-disable-hardware-transforms.md)                                        | Deaktiviert die Verwendung hardwarebasierter Media Foundation Transformationen (MFTs) in der Erfassungs-Engine.                       |
| [MF \_ CAPTURE \_ ENGINE \_ ENABLE \_ CAMERA \_ STREAMSTATE \_ NOTIFICATION](mf-capture-engine-enable-camera-streamstate-notification.md)         | Gibt an, ob Streamstatusbenachrichtigungen aktiviert werden sollen.                                                    |
| [MF \_ CAPTURE \_ ENGINE \_ ENCODER \_ MFT \_ FIELDOFUSE \_ UNLOCK \_ ATTRIBUTE](mf-capture-engine-encoder-mft-fieldofuse-unlock-attribute.md)      | Ermöglicht der Erfassungs-Engine die Verwendung eines Encoders, der Einschränkungen hinsichtlich der Verwendungsfelder aufnimmt.                                   |
| [MF \_ CAPTURE \_ ENGINE \_ EVENT \_ GENERATOR \_ GUID](mf-capture-engine-event-generator-guid.md)                                              | Identifiziert die Komponente, die ein Erfassungsereignis generiert hat.                                                           |
| [MF \_ CAPTURE \_ ENGINE \_ EVENT \_ STREAM \_ INDEX](mf-capture-engine-event-stream-index.md)                                                  | Gibt an, welcher Stream ein Erfassungsereignis generiert hat.                                                                 |
| [MF \_ CAPTURE \_ ENGINE \_ MEDIASOURCE \_ CONFIG](mf-capture-engine-mediasource-config.md)                                                   | Enthält Konfigurationseigenschaften für die Erfassungsquelle.                                                          |
| [MF \_ CAPTURE \_ ENGINE \_ RECORD \_ SINK \_ AUDIO \_ MAX \_ PROCESSED \_ SAMPLES](mf-capture-engine-record-sink-audio-max-processed-samples.md)     | Legt die maximale Anzahl verarbeiteter Stichproben fest, die im Audiopfad der Aufzeichnungssenke gepuffert werden können.                   |
| [MF \_ CAPTURE \_ ENGINE \_ RECORD \_ SINK \_ AUDIO \_ MAX \_ UNPROCESSED \_ SAMPLES](mf-capture-engine-record-sink-audio-max-unprocessed-samples.md) | Legt die maximale Anzahl von nicht verarbeiteten Stichproben fest, die für die Verarbeitung im Audiopfad der Aufzeichnungssenke gepuffert werden können. |
| [MF \_ CAPTURE \_ ENGINE \_ RECORD \_ SINK \_ VIDEO \_ MAX \_ PROCESSED \_ SAMPLES](mf-capture-engine-record-sink-video-max-processed-samples.md)     | Legt die maximale Anzahl verarbeiteter Stichproben fest, die im Videopfad der Aufzeichnungssenke gepuffert werden können.                   |
| [MF \_ CAPTURE \_ ENGINE \_ RECORD \_ SINK \_ VIDEO \_ MAX \_ UNPROCESSED \_ SAMPLES](mf-capture-engine-record-sink-video-max-unprocessed-samples.md) | Legt die maximale Anzahl von nicht verarbeiteten Stichproben fest, die für die Verarbeitung im Videopfad der Aufzeichnungssenke gepuffert werden können.  |
| [MF \_ CAPTURE \_ ENGINE \_ SINK \_ TYPE](/windows/desktop/api/mfcaptureengine/ne-mfcaptureengine-mf_capture_engine_sink_type)                                                                     | Gibt einen Typ der Erfassungssenke an.                                                                                  |
| [MF \_ CAPTURE \_ ENGINE \_ USE \_ AUDIO \_ DEVICE \_ ONLY](mf-capture-engine-use-audio-device-only.md)                                           | Gibt an, ob die Erfassungs-Engine Audio, aber kein Video erfasst.                                                 |
| [MF \_ CAPTURE \_ ENGINE \_ USE \_ VIDEO \_ DEVICE \_ ONLY](mf-capture-engine-use-video-device-only.md)                                           | Gibt an, ob die Erfassungs-Engine Videos, aber keine Audiodaten erfasst.                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[**ADRPaturEngine::Initialisieren**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




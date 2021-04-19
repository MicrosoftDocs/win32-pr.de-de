---
description: Die folgenden Attribute können verwendet werden, um die Aufzeichnungs-Engine zu konfigurieren.
ms.assetid: C153F0AD-4E8B-41DA-B7FB-8D10AC20D22E
title: Attribute der Aufzeichnungs-Engine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1340fa69f80d456a29331d303f313d41c31ee41
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "106350593"
---
# <a name="capture-engine-attributes"></a>Attribute der Aufzeichnungs-Engine

Die folgenden Attribute können verwendet werden, um die Aufzeichnungs-Engine zu konfigurieren.

Die folgenden Attribute beziehen sich auf Erfassungsgeräte:



| Attribut                                                                                                                              | BESCHREIBUNG                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Kameradaten Strom der MF- \_ Aufzeichnungs- \_ Engine \_ \_ \_ blockiert](mf-capture-engine-camera-stream-blocked.md)                                            | Signalisiert, dass die Video Erfassung durch den Treiber blockiert wird.                                                         |
| [der MF- \_ Erfassungs Modul- \_ Kameradaten Strom wurde \_ \_ \_ gesperrt](mf-capture-engine-camera-stream-unblocked.md)                                        | Signalisiert, dass die Video Erfassung nach dem blockieren wieder hergestellt wird.                                                        |
| [MF- \_ Erfassungs Modul \_ \_ D3D \_ Manager](mf-capture-engine-d3d-manager.md)                                                                 | Legt einen Zeiger auf den DXGI-Device Manager für die Aufzeichnungs-Engine fest.                                                   |
| [MF- \_ Erfassungs- \_ Engine- \_ Decoder \_ MFT \_ fieldofuse \_ Unlock- \_ Attribut](mf-capture-engine-decoder-mft-fieldofuse-unlock-attribute.md)      | Ermöglicht der Erfassungs-Engine die Verwendung eines Decoders mit Einschränkungen für das Feld.                                    |
| [Das MF- \_ Erfassungs Modul \_ \_ deaktiviert \_ DXVA](mf-capture-engine-disable-dxva.md)                                                               | Gibt an, ob die Aufzeichnungs-Engine die DirectX-Videobeschleunigung (DXVA) zum Decodieren von Videos verwendet.                    |
| [MF- \_ Erfassung \_ Deaktivieren von \_ Hardware \_ Transformationen](mf-capture-engine-disable-hardware-transforms.md)                                        | Deaktiviert die Verwendung von hardwarebasierten Media Foundation Transformationen (MFTs) in der Erfassungs-Engine.                       |
| [MF- \_ Erfassungs Modul \_ \_ enable \_ Camera \_ streamstate- \_ Benachrichtigung](mf-capture-engine-enable-camera-streamstate-notification.md)         | Gibt an, ob streamstatusbenachrichtigungen aktiviert werden sollen.                                                    |
| [MF- \_ Erfassungs- \_ Engine- \_ Encoder \_ MFT \_ fieldofuse \_ Unlock- \_ Attribut](mf-capture-engine-encoder-mft-fieldofuse-unlock-attribute.md)      | Ermöglicht der Erfassungs-Engine die Verwendung eines Encoders mit Einschränkungen für das Feld.                                   |
| [\_ \_ \_ Ereignis \_ Generator- \_ GUID der MF-Erfassungs-Engine](mf-capture-engine-event-generator-guid.md)                                              | Identifiziert die Komponente, die ein Aufzeichnungs Ereignis generiert hat.                                                           |
| [\_Ereignisdaten \_ Strom \_ - \_ \_ Index für die MF-Erfassung](mf-capture-engine-event-stream-index.md)                                                  | Gibt an, welcher Stream ein Aufzeichnungs Ereignis generiert hat.                                                                 |
| [\_ \_ \_ MediaSource-Konfiguration des MF-Erfassungs Moduls \_](mf-capture-engine-mediasource-config.md)                                                   | Enthält Konfigurations Eigenschaften für die Erfassungs Quelle.                                                          |
| [MF \_ -Erfassungs \_ -Engine Daten \_ Satz \_ -Senke für \_ \_ Maximale \_ Verarbeitung \_](mf-capture-engine-record-sink-audio-max-processed-samples.md)     | Legt die maximale Anzahl von verarbeiteten Stichproben fest, die im Audiopfad der Daten Satz Senke gepuffert werden können.                   |
| [MF \_ -Erfassungs \_ -Engine Daten \_ Satz \_ -Senke \_ \_ audiomaximale \_ unverarbeitete \_](mf-capture-engine-record-sink-audio-max-unprocessed-samples.md) | Legt die maximale Anzahl nicht verarbeiteter Beispiele fest, die für die Verarbeitung im Audiopfad der Daten Satz Senke gepuffert werden können. |
| [\_Daten Satz-Sink-Video zur Erfassung der \_ \_ Datensätze \_ \_ \_ \_ \_](mf-capture-engine-record-sink-video-max-processed-samples.md)     | Legt die maximale Anzahl von verarbeiteten Stichproben fest, die im Video Pfad der Daten Satz Senke gepuffert werden können.                   |
| [\_ \_ \_ Daten Satz-senkenvideo der MF-Erfassung max. \_ \_ \_ \_ nicht verarbeitete \_ Beispiele](mf-capture-engine-record-sink-video-max-unprocessed-samples.md) | Legt die maximale Anzahl nicht verarbeiteter Beispiele fest, die für die Verarbeitung im Video Pfad der Daten Satz Senke gepuffert werden können.  |
| [Typ der MF- \_ Erfassungs- \_ Engine \_ \_](/windows/desktop/api/mfcaptureengine/ne-mfcaptureengine-mf_capture_engine_sink_type)                                                                     | Gibt einen Typ von Aufzeichnungs Senke an.                                                                                  |
| [die \_ MF \_ -Erfassungs \_ -Engine verwendet \_ \_ nur Audiogeräte \_ .](mf-capture-engine-use-audio-device-only.md)                                           | Gibt an, ob die Aufzeichnungs-Engine Audiodaten erfasst, aber kein Video.                                                 |
| [die MF- \_ Erfassungs- \_ Engine \_ verwendet \_ \_ nur Video Geräte \_ .](mf-capture-engine-use-video-device-only.md)                                           | Gibt an, ob die Aufzeichnungs-Engine Videos, aber keine Audiodaten erfasst.                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[**IMF captureengine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




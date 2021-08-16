---
description: Wiederherstellen nach einem Invalid-Device Fehler (Räumlicher Sound)
title: Wiederherstellen nach einem Invalid-Device Fehler (Räumlicher Sound)
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 124d4a804c2f99c051fee50d1c8d819d794b87a5943c216951e0c72870de8c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406218"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a>Wiederherstellen nach einem Invalid-Device Fehler (Räumlicher Sound)

Viele der Methoden der Microsoft Spatial Audio-API, z. B. [ISpatialAudioClient,](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)und [ISpatialAudioObject,](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)geben Fehlercodes zurück, wenn das von der Clientanwendung verwendete Audioendpunktgerät ungültig wird oder das Renderingformat für räumliche Audiodaten auf dem Endpunkt geändert wird. Diese Fehlercodes geben an, dass das Endpunktgerät nicht angeschlossen wurde oder dass die Audiohardware oder die zugehörigen Hardwareressourcen neu konfiguriert, deaktiviert, entfernt, der räumliche Audiomodus geändert oder anderweitig für die Verwendung nicht verfügbar gemacht wurde. Häufig kann die Anwendung nach diesem Fehler wiederhergestellt werden.

Fehlercodes, die auf einen Fehler aufgrund eines ungültigen Geräts hinweisen, umfassen Folgendes:

- SPTLAUDCLNT_E_DESTROYED
- AUDCLNT_E_DEVICE_INVALIDATED
- AUDCLNT_E_RESOURCES_INVALIDATED
- AUDCLNT_E_UNSUPPORTED_FORMAT
- SPTLAUDCLNT_E_INTERNAL

## <a name="strategies-for-handling-invalid-device-errors"></a>Strategien zum Behandeln von Fehlern mit ungültigen Geräten

Die empfohlene Strategie für die Wiederherstellung nach einem Fehler aufgrund eines ungültigen Geräts hängt davon ab, ob die Anwendung basierend auf internen Anforderungen automatisch ein bestimmtes Gerät auswählt oder ob der Benutzer ein Gerät explizit aus einer Liste verfügbarer Geräte auswählen kann. 

### <a name="default-audio-device"></a>Standardaudiogerät

Wenn die Anwendung das Standardgerät automatisch auswählt, verwenden Sie die folgenden Schritte, um die Wiederherstellung zu erstellen.

1. Geben Sie [die ISpatialAudioObjectRenderStream-](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) und [ISpatialAudioClient-Schnittstelle](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) sowie alle anderen schnittstellen für räumliche Audioinhalte frei, die für das Rendering verwendet werden. 
1. Rufen [Sie IMMDeviceEnumerator::GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) auf, um das aktuelle Standardaudiogerät zu erhalten.
1. Versuchen Sie, **ISpatialAudioClient auf** dem Audiogerät zu aktivieren.
1. Aktivieren **Sie ISpatialAudioObjectRenderStream.** 

### <a name="specifically-selected-audio-device"></a>Speziell ausgewähltes Audiogerät

Wenn die Anwendung ein bestimmtes Audiogerät auswählt, verwenden Sie die folgenden Schritte zum Wiederherstellen.

1. Geben Sie die ISpatialAudioObjectRenderStream-Schnittstelle und alle anderen räumlichen Audioschnittstellen frei, die für das Rendering verwendet werden, geben Sie **jedoch nicht ISpatialAudioClient frei.**
1. Verwenden Sie die aktuelle **ISpatialAudioClient-Instanz,** um **ISpatialAudioObjectRenderStream zu aktivieren.**

Beachten Sie, dass für beide oben aufgeführten Strategien die gleichen Schritte auf Anwendungen angewendet werden können, die die [Schnittstellen ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) oder [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) verwenden. Ersetzen Sie **einfach ISpatialAudioObjectRenderStream** in den obigen Schritten durch die Metadaten- oder Hrtf-Schnittstellen.


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>
[Wiederherstellung nach einem Invalid-Device Fehler](recovering-from-an-invalid-device-error.md) 
 [Streamverwaltung](stream-management.md)
</dt> </dl>

 

 




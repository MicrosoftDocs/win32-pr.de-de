---
description: Wiederherstellen nach einem Invalid-Device Fehler (räumlicher Sound)
title: Wiederherstellen nach einem Invalid-Device Fehler (räumlicher Sound)
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 1ec4f040aff10f2d118b20c489e74d792c907113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127424"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a>Wiederherstellen nach einem Invalid-Device Fehler (räumlicher Sound)

Viele der Methoden der räumlichen Audio-API von Microsoft, wie z. b. [ispatialaudioclient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ispatialaudioobjectrenderstream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)und [ispatialaudioobject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), geben Fehlercodes zurück, wenn das audioendpunktgerät, das die Client Anwendung verwendet, ungültig wird oder das räumliche audiorenderingformat für den Endpunkt geändert wird. Diese Fehlercodes geben an, dass das Endpunkt Gerät getrennt wurde oder dass die Audiohardware oder die zugehörigen Hardware Ressourcen neu konfiguriert, deaktiviert, entfernt, der räumliche Audiomodus geändert oder anderweitig nicht zur Verwendung zur Verfügung gestellt wurde. Häufig kann die Anwendung nach diesem Fehler wieder hergestellt werden.

Fehlercodes, die auf einen ungültigen Gerätefehler hinweisen, sind folgende:

- SPTLAUDCLNT_E_DESTROYED
- AUDCLNT_E_DEVICE_INVALIDATED
- AUDCLNT_E_RESOURCES_INVALIDATED
- AUDCLNT_E_UNSUPPORTED_FORMAT
- SPTLAUDCLNT_E_INTERNAL

## <a name="strategies-for-handling-invalid-device-errors"></a>Strategien für die Behandlung von Fehlern bei ungültigen Geräten

Die empfohlene Strategie für die Wiederherstellung nach einem Fehler aufgrund eines ungültigen Geräts hängt davon ab, ob die Anwendung automatisch ein bestimmtes Gerät basierend auf internen Anforderungen auswählt oder ob der Benutzer ein Gerät explizit aus einer Liste der verfügbaren Geräte auswählen kann. 

### <a name="default-audio-device"></a>Standardaudiogerät

Wenn die Anwendung automatisch das Standardgerät auswählt, führen Sie die folgenden Schritte aus, um die Wiederherstellung auszuführen.

1. Geben Sie die Schnittstelle [ispatialaudioobjectrenderstream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) und [ispatialaudioclient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) sowie alle anderen räumlichen Audioschnittstellen, die zum Rendern verwendet werden, frei. 
1. Bitten Sie [immdeviceenumerator:: getdefaultaudioendpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) , um das aktuelle Standardaudiogerät abzurufen.
1. Versuchen Sie, **ispatialaudioclient** auf dem Audiogerät zu aktivieren.
1. Aktivieren Sie **ispatialaudioobjectrenderstream**. 

### <a name="specifically-selected-audio-device"></a>Speziell ausgewähltes Audiogerät

Wenn die Anwendung ein bestimmtes Audiogerät auswählt, führen Sie die folgenden Schritte aus, um die Wiederherstellung auszuführen.

1. Geben Sie die ispatialaudioobjectrenderstream-Schnittstelle und alle anderen räumlichen Audioschnittstellen, die zum Rendern verwendet werden, aber nicht " **ispatialaudioclient**" frei.
1. Verwenden Sie die aktuelle **ispatialaudioclient** -Instanz, um **ispatialaudioobjectrenderstream** zu aktivieren.

Beachten Sie, dass die gleichen Schritte für beide oben aufgeführten Strategien auf Anwendungen angewendet werden können, die die [ispatialaudioobjectrenderstreamformetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) -Schnittstelle oder die [ispatialaudioobjectrenderstreamforhrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) -Schnittstelle verwenden. Ersetzen Sie einfach **ispatialaudioobjectrenderstream** in den obigen Schritten durch die Metadaten oder die HRTF-Schnittstellen.


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>Wieder 
[herstellen nach einem Invalid-Device Fehler](recovering-from-an-invalid-device-error.md) 
 Daten [Strom Verwaltung](stream-management.md)
</dt> </dl>

 

 




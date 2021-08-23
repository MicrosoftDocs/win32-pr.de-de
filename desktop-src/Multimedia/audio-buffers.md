---
title: Audiopuffer
description: Audiopuffer
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- WM_CAP_GET_SEQUENCE_SETUP-Nachricht
- capCaptureGetSetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP-Nachricht
- capCaptureSetSetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7993e3dc89abda520c0f1c5bda90f3eb209aca31e36071a304af01fb420d821e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692100"
---
# <a name="audio-buffers"></a>Audiopuffer

Sie können den Audioteil eines Erfassungsvorgang auf drei Arten steuern:

-   Schließen Sie Audiodaten in den Erfassungsvorgang ein, oder schließen Sie sie aus.
-   Fordern Sie eine bestimmte Anzahl von Audiopuffern an.
-   Fordern Sie an, dass Audiopuffer eine bestimmte Größe haben.

Sie können die Einstellungen für Audiopuffer mithilfe der [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-get-sequence-setup.md) (oder des [**Makros capCaptureGetSetup)**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) abrufen. Der **fCaptureAudio-Member** der [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) gibt an, ob Audiodaten in den Erfassungsvorgang eingeschlossen oder davon ausgeschlossen werden. Die aktuell angeforderte Anzahl von Audiopuffern wird im **wNumAudioRequested-Element** gespeichert, und die aktuelle Audiopuffergröße wird im **dwAudioBufferSize-Element** gespeichert. Sie können angeben, ob audio capture enthalten sein soll, die Größe und Anzahl von Audiopuffern angeben, indem Sie diese Member aktualisieren, und die aktualisierte **CAPTUREPARMS-Struktur** mithilfe der [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-set-sequence-setup.md) (oder des [**capCaptureSetSetup-Makros)**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) an das Erfassungsfenster senden.

Standardmäßig ist Audio im Erfassungsvorgang enthalten, und vier Audiopuffer werden zugeordnet. Der Standardwert von **fCaptureAudio ist** **TRUE.** Die Standardpuffergröße (der Wert **von dwAudioBufferSize)** kann 0,5 Sekunden Audiodaten oder 10.000 enthalten, je nach Größe.

 

 





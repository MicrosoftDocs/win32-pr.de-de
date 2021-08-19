---
title: MCIERR-Rückgabewerte
description: MCIERR-Rückgabewerte
ms.assetid: 61f7b128-b4f7-4385-9daf-e2bc9fb36e24
keywords:
- Windows multimedia,MCIERR-Rückgabewerte
- Multimedia,MCIERR-Rückgabewerte
- Multimediareferenz, MCIERR-Rückgabewerte
- Referenz für Multimedia,MCIERR-Rückgabewerte
- MCIERR-Rückgabewerte,About
- mciSendCommand-Funktion
- mciSendString-Funktion
- Windows multimedia,errors
- multimedia,errors
- Multimediareferenz,Fehler
- Referenz für Multimedia,Fehler
- Media Control Interface (MCI), MCIERR-Rückgabewerte
- MCI (Media Control Interface), MCIERR-Rückgabewerte
- Referenz für MCI,MCIERR-Rückgabewerte
- MCI-Referenz, MCIERR-Rückgabewerte
- Media Control Interface (MCI), Fehler
- MCI (Media Control Interface), Fehler
- Referenz für MCI, Fehler
- MCI-Referenz,Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fc8426b264f68d7a6ab793e365d529774c931e72d89536b40b22592728a2ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783410"
---
# <a name="mcierr-return-values"></a>MCIERR-Rückgabewerte

Die [**Funktionen mciSendCommand**](/previous-versions//dd757160(v=vs.85)) und [**mciSendString**](/previous-versions//dd757161(v=vs.85)) geben null zurück, wenn sie erfolgreich sind. Andernfalls geben sie einen **DWORD-Wert** zurück, der einen der folgenden Fehlerwerte im unteren Wort enthält.

-   [Allgemeine MCI-Fehler](general-mci-errors.md)
-   [mciSendString-Fehler](mcisendstring-errors.md)
-   [Digital-Video-Fehler](digital-video-errors.md)
-   [Sequencer-Fehler](sequencer-errors.md)
-   [Waveform-Audio-Fehler](waveform-audio-errors.md)

Sie können eine Beschreibung einzelner Rückgabewerte abrufen, indem Sie die Rückgabewerte an die [**mciGetErrorString-Funktion**](/previous-versions//dd757158(v=vs.85)) übergeben.

 

 
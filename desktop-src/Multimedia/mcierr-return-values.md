---
title: Mcierr-Rückgabewerte
description: Mcierr-Rückgabewerte
ms.assetid: 61f7b128-b4f7-4385-9daf-e2bc9fb36e24
keywords:
- Windows-Multimedia, mcierr-Rückgabewerte
- Multimedia-, mcierr-Rückgabewerte
- Multimedia-Referenz, mcierr-Rückgabewerte
- Referenz für Multimedia-, mcierr-Rückgabewerte
- Mcierr-Rückgabewerte, Informationen zu
- mciSendCommand-Funktion
- mciSendString-Funktion
- Windows Multimedia, Fehler
- Multimedia, Fehler
- Multimedia-Referenz, Fehler
- Referenz für Multimedia, Fehler
- Medien Steuerungs Schnittstelle (MCI), mcierr-Rückgabewerte
- MCI (Media Control Interface), mcierr-Rückgabewerte
- Verweis für MCI, mcierr-Rückgabewerte
- MCI-Referenz, mcierr-Rückgabewerte
- Media Control Interface (MCI), Fehler
- MCI (Medien Steuerungs Schnittstelle), Fehler
- Referenz für MCI, Fehler
- MCI-Referenz, Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8912284b98b2aacb60905e3fef4dc32705a5656
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339064"
---
# <a name="mcierr-return-values"></a>Mcierr-Rückgabewerte

Die Funktionen " [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) " und " [**mciSendString**](/previous-versions//dd757161(v=vs.85)) " geben NULL zurück, wenn Sie erfolgreich sind. Andernfalls wird ein **DWORD** -Wert zurückgegeben, der einen der folgenden Fehler Werte im unteren Wort enthält.

-   [Allgemeine MCI-Fehler](general-mci-errors.md)
-   [mciSendString-Fehler](mcisendstring-errors.md)
-   [Digital-Video-Fehler](digital-video-errors.md)
-   [Sequencer-Fehler](sequencer-errors.md)
-   [Waveform-Audiofehler](waveform-audio-errors.md)

Sie können eine Beschreibung einzelner Rückgabewerte abrufen, indem Sie die Rückgabewerte an die [**mcigeterrorstring**](/previous-versions//dd757158(v=vs.85)) -Funktion übergeben.

 

 
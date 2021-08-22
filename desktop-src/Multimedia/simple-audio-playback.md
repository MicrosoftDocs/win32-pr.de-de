---
title: Einfache Audiowiedergabe
description: Einfache Audiowiedergabe
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- Multimediaaudio, Wellenform
- Audio, Wellenform
- Waveformaudio, einfache Wiedergabe
- MessageBeep-Funktion
- sndPlaySound-Funktion
- PlaySound-Funktion, einfache Wiedergabe
- Multimediaaudio, PlaySound-Funktion
- audio,PlaySound-Funktion
- Waveform-Audio, PlaySound-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6388f9800f93080e995ae537c2458a22da033ab2149b4bfca114c25025d97434
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688690"
---
# <a name="simple-audio-playback"></a>Einfache Audiowiedergabe

Sie können die folgenden Funktionen verwenden, um Waveform-Audio in Ihrer Anwendung in einem einzelnen Funktionsaufruf wiederzuspielen.



| Funktion                                                      | Beschreibung                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MessageBeep](/windows/win32/api/winuser/nf-winuser-messagebeep) | Gibt den Sound wieder, der einer angegebenen Systemwarnungsstufe entspricht.                                                 |
| [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))                          | Gibt den Sound wieder, der dem in der Registrierung eingegebenen Systemsound oder dem Inhalt der angegebenen Datei entspricht. |
| [**PlaySound**](/previous-versions//dd743680(v=vs.85))                                | Stellt alle Funktionen von [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) bereit und kann direkt auf Ressourcen zugreifen.           |



 

Die **MessageBeep-Funktion** ist ein Standardteil der Win32-API. da seine Funktionen sehr eingeschränkt sind und an anderer Stelle dokumentiert sind, wird dies hier nicht erläutert.

Die aufgeführten Funktionen unterstützen die folgenden Quellen für Wellenformaudio:

-   Waveform-Audiodateien, die Systemwarnungsebenen zugeordnet sind
-   Waveform-Audiodateien, die von Einträgen in der Registrierung angegeben werden
-   WAVE-Ressourcen im Arbeitsspeicher
-   Waveform-Audiodateien, die durch den Namen angegeben werden

Die Funktionen [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) und [**PlaySound**](/previous-versions//dd743680(v=vs.85)) laden eine gesamte Waveform-Audiodatei in den Arbeitsspeicher und begrenzen die Größe der Datei, die sie wiedergeben können. Verwenden Sie **sndPlaySound** und **PlaySound,** um waveform-audio-Dateien wiederzugeben, die klein sind – bis zu 100.000. Diese beiden Funktionen erfordern auch, dass die Sounddaten in einem Format vorliegen, das von einem der installierten Waveform-Audiotreiber, einschließlich des Wave-Mappers, wiedergegeben werden kann.

Verwenden Sie für größere Sounddateien die MCI-Dienste (Media Control Interface). Weitere Informationen finden Sie unter [MCI](mci.md).

 

 
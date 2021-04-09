---
title: Einfache Audiowiedergabe
description: Einfache Audiowiedergabe
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- Multimedia-Audiodatei, Wellenform
- Audiodaten, Wellenform
- Wellenform-Audiodatei, einfache Wiedergabe
- MessageBeep-Funktion
- SndPlaySound-Funktion
- PlaySound-Funktion, einfache Wiedergabe
- Multimedia-Audio, PlaySound-Funktion
- Audio, PlaySound-Funktion
- Wellenform-Audio, PlaySound-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256feded06de4ee92ee415f14bb08adc7fb4456e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948661"
---
# <a name="simple-audio-playback"></a>Einfache Audiowiedergabe

Sie können die folgenden Funktionen verwenden, um Wellenform-Audiodaten in der Anwendung in einem einzelnen Funktions aufzurufen wiederzugeben.



| Funktion                                                      | BESCHREIBUNG                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MessageBeep](/windows/win32/api/winuser/nf-winuser-messagebeep) | Gibt den Sound wieder, der einer angegebenen System Warnstufe entspricht.                                                 |
| [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))                          | Gibt den Sound wieder, der dem in der Registrierung eingegebenen System Sound oder dem Inhalt der angegebenen Datei entspricht. |
| [**PlaySound**](/previous-versions//dd743680(v=vs.85))                                | Bietet die gesamte Funktionalität von [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) und kann direkt auf Ressourcen zugreifen.           |



 

Die **MessageBeep** -Funktion ist ein Standard Teil der Win32-API. Da die Funktionen sehr eingeschränkt sind und an anderer Stelle dokumentiert werden, werden Sie hier nicht erläutert.

Die aufgeführten Funktionen unterstützen die folgenden Quellen der Wellenform-Audiodatei:

-   Waveform-Audiodateien, die System Warn Stufen zugeordnet sind
-   Waveform-Audiodateien, die durch Einträge in der Registrierung angegeben werden
-   In-Memory-Wellen Ressourcen
-   Waveform-Audiodateien, angegeben nach Name

Die Funktionen [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) und [**PlaySound**](/previous-versions//dd743680(v=vs.85)) laden eine gesamte Waveform-Audiodatei in den Arbeitsspeicher und schränken die Größe der Datei ein, die Sie wiedergeben können. Verwenden Sie **sndPlaySound** und **PlaySound** , um Waveform-Audiodateien wiederzugeben, die klein sind – bis zu 100 KB. Diese beiden Funktionen erfordern auch, dass die Audiodaten in einem Format vorliegen, das von einem der installierten Waveform-Audiotreiber (einschließlich der Wave-Mapper) abgespielt werden kann.

Verwenden Sie für größere Audiodateien die MCI-Dienste (Media Control Interface). Weitere Informationen finden Sie unter [MCI](mci.md).

 

 